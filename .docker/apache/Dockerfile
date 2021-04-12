FROM httpd:2.4.33-alpine

# Copy apache vhost file to proxy php requests to php-fpm container
COPY apache2.conf.dev /usr/local/apache2/conf/apache2.conf

RUN apk update && apk upgrade
RUN apk add --no-cache bash
RUN sed -i '/LoadModule rewrite_module/s/^#//g' /usr/local/apache2/conf/httpd.conf
RUN echo "Include /usr/local/apache2/conf/apache2.conf" >> /usr/local/apache2/conf/httpd.conf
