FROM base
MAINTAINER Gustavo Soares <slotmg@protonmail.com>

ENV DEBIAN_FRONTEND noninteractive
ENV LC_ALL pt_BR

RUN wget -q https://packages.sury.org/php/apt.gpg -O- | apt-key add -					&& \
	echo "deb https://packages.sury.org/php/ buster main" > /etc/apt/sources.list.d/php.list

RUN apt-get update && apt-get install -q -y --no-install-recommends apache2 libapache2-mod-php7.3 php7.3-mysql php7.3-dom php7.3-gd php7.3-json php7.3-pdo php7.3-simplexml php7.3-tokenizer php7.3-xml	php7.3-xml php7.3-xmlreader php7.3-curl php7.3-exif php7.3-ftp php7.3-gd  php7.3-iconv php7.3-imagick php7.3-json  php7.3-mbstring php7.3-posix php7.3-sockets php7.3-tokenizer

RUN rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

EXPOSE 80

CMD ["apachectl", "-D", "FOREGROUND"]
