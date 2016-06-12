# Docker nginx + php-fpm skeleton

This is a skeleton for docker compose with two containers, one running nginx stable version, and the other one running PHP-FPM 5.x

## Usage

Put your web application code into www folder and run `docker-compose up`. Or, if you have your application files stored somewhere else, adjust the path for volumes in docker-compose.yml

To install additional PHP extensions, edit docker-build/phpfpm/Dockerfile and add `RUN docker-php-ext-install -j$(nproc) mbstring` and rebuild the containers, either by running `docker-compose up --build` or `docker-compose build`.