FROM php:8.0-fpm-alpine

# algunas configuraciones para que funcione el contenedor
RUN apk add --no-cache curl bash git vim nano
RUN apk add --no-cache composer 
RUN docker-php-ext-install pdo pdo_mysql
RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli

# da permisos para editar los archivos en esta ruta del container
RUN chown -R www-data:www-data /var/www
RUN chmod 755 /var/www