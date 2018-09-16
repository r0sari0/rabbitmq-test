FROM composer:latest
RUN docker-php-ext-install mbstring bcmath
RUN mkdir -p /app
RUN apk update && apk upgrade && apk add --no-cache bash git openssh
COPY ./ /app
WORKDIR /app
EXPOSE 8000
CMD umask 000 && composer install && php ./producer/index.php