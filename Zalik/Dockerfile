FROM php:8.1.0-apache

RUN apt-get update && \
    apt-get install -y nodejs npm && \
    rm -rf /var/lib/apt/lists/*

COPY . /var/www/html/

RUN npm install moment

RUN npm install chartjs-adapter-moment

RUN chown -R www-data:www-data /var/www/html/

WORKDIR /var/www/html/

EXPOSE 80

CMD ["apache2-foreground"]
