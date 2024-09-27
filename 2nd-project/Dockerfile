# This is the docker file to build the docker image

FROM drupal

RUN apt update && apt install -y git && rm -rf /var/lib/apt/lists/*

WORKDIR /var/www/html/themes

RUN git clone https://git.drupalcode.org/project/bootstrap.git \
    && chown -R www-data:www-data bootstrap

WORKDIR /var/www/html
