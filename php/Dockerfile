FROM php:7.2-cli

RUN apt-get update && \
    apt-get install -y imagemagick

RUN mkdir -p /usr/src/myapp/

COPY main.php /usr/src/myapp/

WORKDIR /usr/src/myapp

CMD [ "php", "./main.php" ]
