## `friendica:apache`

```console
$ docker pull friendica@sha256:4008d510fd16a6c83f1958e2104598c9665404ad1d9f651f1ba172efadc1f722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `friendica:apache` - linux; amd64

```console
$ docker pull friendica@sha256:5ea7aef7bd0a8ab6abecc6e3db48fac27a31f1dd2655b80d7844c8887e3b0aae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.7 MB (215747348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ae08b31154846f1068a68659e1414d1a2aba031b6ed422336c490ed3a6729d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 01 Feb 2020 17:23:57 GMT
ADD file:003d2bac85e72555ed93f77a2b1d595a7fe51c4a9a2401496a82fc673a863fd6 in / 
# Sat, 01 Feb 2020 17:23:58 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:28:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 01 Feb 2020 20:28:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 01 Feb 2020 20:28:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 20:28:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 01 Feb 2020 20:28:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 01 Feb 2020 20:36:53 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 01 Feb 2020 20:36:53 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 01 Feb 2020 20:37:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 01 Feb 2020 20:37:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 01 Feb 2020 20:37:05 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 01 Feb 2020 20:37:06 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 01 Feb 2020 20:37:06 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 01 Feb 2020 20:37:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 01 Feb 2020 20:37:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 01 Feb 2020 20:37:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 01 Feb 2020 20:37:07 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Sat, 01 Feb 2020 20:37:07 GMT
ENV PHP_VERSION=7.3.14
# Sat, 01 Feb 2020 20:37:07 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.14.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.14.tar.xz.asc/from/this/mirror
# Sat, 01 Feb 2020 20:37:07 GMT
ENV PHP_SHA256=cc05dd373ca5d36652800762f65c10e828a17de35aaf246262e3efa99d00cdb0 PHP_MD5=
# Sat, 01 Feb 2020 20:37:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 01 Feb 2020 20:37:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 01 Feb 2020 20:40:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	sed -e 's/stretch/buster/g' /etc/apt/sources.list > /etc/apt/sources.list.d/buster.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libargon2*'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/argon2-buster; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Sat, 01 Feb 2020 20:40:55 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Sat, 01 Feb 2020 20:40:56 GMT
RUN docker-php-ext-enable sodium
# Sat, 01 Feb 2020 20:40:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 01 Feb 2020 20:40:56 GMT
STOPSIGNAL SIGWINCH
# Sat, 01 Feb 2020 20:40:56 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 01 Feb 2020 20:40:57 GMT
WORKDIR /var/www/html
# Sat, 01 Feb 2020 20:40:57 GMT
EXPOSE 80
# Sat, 01 Feb 2020 20:40:57 GMT
CMD ["apache2-foreground"]
# Sun, 02 Feb 2020 11:26:40 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         ssmtp     ;     rm -rf /var/lib/apt/lists/*;
# Sun, 02 Feb 2020 11:29:15 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mysql-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         	--with-libdir=lib/$debMultiarch/ 	;     docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.1.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so       | awk '/=>/ { print $3 }'       | sort -u       | xargs -r dpkg-query -S       | cut -d: -f1       | sort -u       | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 11:29:16 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Sun, 02 Feb 2020 11:29:16 GMT
VOLUME [/var/www/html]
# Sun, 02 Feb 2020 11:29:17 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Sun, 02 Feb 2020 11:29:17 GMT
ENV FRIENDICA_VERSION=2019.12
# Sun, 02 Feb 2020 11:29:17 GMT
ENV FRIENDICA_ADDONS=2019.12
# Sun, 02 Feb 2020 11:29:37 GMT
RUN set -ex;     curl -fsSL -o friendica.tar.gz         "https://github.com/friendica/friendica/archive/${FRIENDICA_VERSION}.tar.gz";     tar -xzf friendica.tar.gz -C /usr/src/;     rm friendica.tar.gz;     mv -f /usr/src/friendica-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;     curl -fsSL -o friendica_addons.tar.gz         "https://github.com/friendica/friendica-addons/archive/${FRIENDICA_ADDONS}.tar.gz";     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica_addons.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica_addons.tar.gz;     /usr/src/friendica/bin/composer.phar install --no-dev -d /usr/src/friendica;
# Sun, 02 Feb 2020 11:29:38 GMT
COPY multi:0a5bdeeeece27826a5344be9215b3de17c80ece34c27fd9cf4c61a0c7e730616 in / 
# Sun, 02 Feb 2020 11:29:38 GMT
COPY multi:ccf608c3083a2548ed80248e6308632e395ce7dfbcb83d73bfba22293ecd8ffd in /usr/src/friendica/config/ 
# Sun, 02 Feb 2020 11:29:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 02 Feb 2020 11:29:39 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:619014d83c026bca3d21f5eb42a629ac2dbe15bdb37b77f25fc1ac5fbada68e5`  
		Last Modified: Sat, 01 Feb 2020 17:29:01 GMT  
		Size: 22.5 MB (22524713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4714e5926d380fbc0d5b9510b81e8d0bf9898d0e3b1edc2b9624b1fa59af275`  
		Last Modified: Sat, 01 Feb 2020 21:49:28 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f2e17b3109b13e9d7167747d00d487fa5154a486854ed8ebaeb8192a96dcee`  
		Last Modified: Sat, 01 Feb 2020 21:49:57 GMT  
		Size: 67.4 MB (67447626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e8f49d6f5dcce54be64850fffd334ccf402c0f088f6dd18b2ecd26febe3f28`  
		Last Modified: Sat, 01 Feb 2020 21:49:27 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8f9d93b7a1c0ceff4632362182c5f8b15fa1eb828e307cb4488c8fa665366e`  
		Last Modified: Sat, 01 Feb 2020 21:50:10 GMT  
		Size: 17.1 MB (17125285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e7e4734c6ea3fda86973c852fcc0b78028674c726eefad84a43c5a4181bdea`  
		Last Modified: Sat, 01 Feb 2020 21:50:05 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a155d22afc0a899cd1526ef89bcc743c05035888a621acc2cb0641066f85d87`  
		Last Modified: Sat, 01 Feb 2020 21:50:05 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2db8bee0fcaca05f5fff59df8b7facef101ede851aa87ec772620fd305d64c1`  
		Last Modified: Sat, 01 Feb 2020 21:50:07 GMT  
		Size: 12.5 MB (12455269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1363dc77618eb29373723f273e3b4c812f343511d1db706e7792a9ff2ca0c0f`  
		Last Modified: Sat, 01 Feb 2020 21:50:04 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6228b7ca091c94913b85f319a8293656370f1df3082535e5ec7959bdabaec7`  
		Last Modified: Sat, 01 Feb 2020 21:50:09 GMT  
		Size: 13.8 MB (13824810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd9984fd7e7a7e1ef247a19971234891444335ae2c2dc395c4aae1fa16dd7b1`  
		Last Modified: Sat, 01 Feb 2020 21:50:04 GMT  
		Size: 2.2 KB (2240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb5bec6e1689935cbf66e2ff69d96bd47999e46a211602721adf80473097231`  
		Last Modified: Sat, 01 Feb 2020 21:50:04 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b40fa58bf07c00ef4e9a7ba58f5f3d98d8980896aef859959c7ab6c100acd3c`  
		Last Modified: Sat, 01 Feb 2020 21:50:04 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75770cd4fe68e4cf674215a8f27420fb5f8b0f97ec6a9bc9b77b320a7e96bbc0`  
		Last Modified: Sun, 02 Feb 2020 11:33:31 GMT  
		Size: 13.2 MB (13167593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5ab2494e110a82d02f8a2a61ae631641d0904045e7ada70849a399a1be7524`  
		Last Modified: Sun, 02 Feb 2020 11:33:31 GMT  
		Size: 11.6 MB (11649974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e71c4174e6f8101e579986e40ccba73437ddc34abd13f1d9d0be77e0962210b`  
		Last Modified: Sun, 02 Feb 2020 11:33:26 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0226cf6072fd3709b8c1f0d1070cb1374672ca8135e78e0698794f8128ba2f2e`  
		Last Modified: Sun, 02 Feb 2020 11:33:26 GMT  
		Size: 539.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2bf1bd76552229ab76416ed991dacf782a9b2c96d1fbf6b8430a0f3caabacf`  
		Last Modified: Sun, 02 Feb 2020 11:33:37 GMT  
		Size: 57.5 MB (57542418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7889720e3d32ca6e4fae5d77d7ad0358b60cd2bc9ff9f2d5d37483c01aedae`  
		Last Modified: Sun, 02 Feb 2020 11:33:26 GMT  
		Size: 2.2 KB (2180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2938a7a19ecd6aec4ba3826b8fd38e879f13de82fad38e789a4b617a94f0cd9d`  
		Last Modified: Sun, 02 Feb 2020 11:33:26 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:apache` - linux; arm variant v5

```console
$ docker pull friendica@sha256:5a9242cc3e4c0362172103348fd709412e28dc02da4ceeb154245796d0136a8e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.1 MB (202089629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423d6843eebcb78c64eb79eb4bf1309d45b0df4a45f12d5f478e982e043e4591`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:57 GMT
ADD file:f0d179649cbf50028b5ecd832961cc332fb524c2f12fda6c8060c3c258208be6 in / 
# Sat, 01 Feb 2020 16:53:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 21:27:35 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 01 Feb 2020 21:27:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 01 Feb 2020 21:28:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 21:28:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 01 Feb 2020 21:28:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 01 Feb 2020 21:32:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 01 Feb 2020 21:32:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 01 Feb 2020 21:33:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 01 Feb 2020 21:33:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 01 Feb 2020 21:33:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 01 Feb 2020 21:33:19 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 01 Feb 2020 21:33:19 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 01 Feb 2020 21:33:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 01 Feb 2020 21:33:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 01 Feb 2020 21:33:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 01 Feb 2020 21:33:22 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Sat, 01 Feb 2020 21:33:22 GMT
ENV PHP_VERSION=7.3.14
# Sat, 01 Feb 2020 21:33:23 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.14.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.14.tar.xz.asc/from/this/mirror
# Sat, 01 Feb 2020 21:33:24 GMT
ENV PHP_SHA256=cc05dd373ca5d36652800762f65c10e828a17de35aaf246262e3efa99d00cdb0 PHP_MD5=
# Sat, 01 Feb 2020 21:33:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 01 Feb 2020 21:33:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 01 Feb 2020 21:37:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	sed -e 's/stretch/buster/g' /etc/apt/sources.list > /etc/apt/sources.list.d/buster.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libargon2*'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/argon2-buster; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Sat, 01 Feb 2020 21:37:17 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Sat, 01 Feb 2020 21:37:20 GMT
RUN docker-php-ext-enable sodium
# Sat, 01 Feb 2020 21:37:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 01 Feb 2020 21:37:22 GMT
STOPSIGNAL SIGWINCH
# Sat, 01 Feb 2020 21:37:23 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 01 Feb 2020 21:37:24 GMT
WORKDIR /var/www/html
# Sat, 01 Feb 2020 21:37:24 GMT
EXPOSE 80
# Sat, 01 Feb 2020 21:37:25 GMT
CMD ["apache2-foreground"]
# Sun, 02 Feb 2020 06:32:02 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         ssmtp     ;     rm -rf /var/lib/apt/lists/*;
# Sun, 02 Feb 2020 06:37:52 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mysql-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         	--with-libdir=lib/$debMultiarch/ 	;     docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.1.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so       | awk '/=>/ { print $3 }'       | sort -u       | xargs -r dpkg-query -S       | cut -d: -f1       | sort -u       | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 06:37:54 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Sun, 02 Feb 2020 06:37:55 GMT
VOLUME [/var/www/html]
# Sun, 02 Feb 2020 06:37:57 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Sun, 02 Feb 2020 06:37:58 GMT
ENV FRIENDICA_VERSION=2019.12
# Sun, 02 Feb 2020 06:37:58 GMT
ENV FRIENDICA_ADDONS=2019.12
# Sun, 02 Feb 2020 06:38:34 GMT
RUN set -ex;     curl -fsSL -o friendica.tar.gz         "https://github.com/friendica/friendica/archive/${FRIENDICA_VERSION}.tar.gz";     tar -xzf friendica.tar.gz -C /usr/src/;     rm friendica.tar.gz;     mv -f /usr/src/friendica-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;     curl -fsSL -o friendica_addons.tar.gz         "https://github.com/friendica/friendica-addons/archive/${FRIENDICA_ADDONS}.tar.gz";     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica_addons.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica_addons.tar.gz;     /usr/src/friendica/bin/composer.phar install --no-dev -d /usr/src/friendica;
# Sun, 02 Feb 2020 06:38:39 GMT
COPY multi:0a5bdeeeece27826a5344be9215b3de17c80ece34c27fd9cf4c61a0c7e730616 in / 
# Sun, 02 Feb 2020 06:38:40 GMT
COPY multi:ccf608c3083a2548ed80248e6308632e395ce7dfbcb83d73bfba22293ecd8ffd in /usr/src/friendica/config/ 
# Sun, 02 Feb 2020 06:38:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 02 Feb 2020 06:38:42 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:03886a8604d1b5423798ee97917dcb9de4cfdfbb7c435a7988d5c5e69a78e3b7`  
		Last Modified: Sat, 01 Feb 2020 17:01:03 GMT  
		Size: 21.2 MB (21202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493128c5a45158748262a5ee18b5826ed3dad4487cdf3a6063f29cc01aeb8abc`  
		Last Modified: Sat, 01 Feb 2020 22:26:25 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc145558187669a4b301464c1406230733d983443f63c186d47c187dbe8559c3`  
		Last Modified: Sat, 01 Feb 2020 22:26:45 GMT  
		Size: 57.5 MB (57486069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fa73ea48d7826f97d650692d25d19ea152eb40e1c8c306b882f2589e95d3a1`  
		Last Modified: Sat, 01 Feb 2020 22:26:25 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e64023a3a6738a004cae4d2369c22cdba680605f89f70bd2311c2fcc829be6c`  
		Last Modified: Sat, 01 Feb 2020 22:27:01 GMT  
		Size: 16.6 MB (16644092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1d6d7f1db26c34f78a2c4b1d0415567c4d2ba1b6016f0fa893b891f1200b10`  
		Last Modified: Sat, 01 Feb 2020 22:26:56 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71f2505d276a30291c164b2247b00d165e66c0522b64ce7de07a4111be14473`  
		Last Modified: Sat, 01 Feb 2020 22:26:56 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fa73e798d30663e1828b4620b7916aaaec50d16ac5c12a2ac24457264f7ffc`  
		Last Modified: Sat, 01 Feb 2020 22:26:58 GMT  
		Size: 12.5 MB (12453136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b7a0e1b4e02248157b216e17743c512c7b0029f7e25bfd0fd0023fcff51099`  
		Last Modified: Sat, 01 Feb 2020 22:26:54 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0f57cd46b0e73d13c9c9b34ae2158d64d4a5d14c4efe0ef0d9c01dee596029`  
		Last Modified: Sat, 01 Feb 2020 22:26:59 GMT  
		Size: 13.1 MB (13094996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7be71d5a88cb7eaf96d0e9325d1b7e4bbbe3482e203ec62a2f5cf2a453abcb9`  
		Last Modified: Sat, 01 Feb 2020 22:26:54 GMT  
		Size: 2.2 KB (2241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec53e9073b002386e31c00317771f7fbd8549d996e911a2517cb4d9e6f96f779`  
		Last Modified: Sat, 01 Feb 2020 22:26:54 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac74c4d7efe559ed84d58859db61a6a90afc5005db8bec8b813b7bba98bd5127`  
		Last Modified: Sat, 01 Feb 2020 22:26:54 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735e7e51d32f43ddac037509e86a290b0e834903ea48f0d3b268687b0e3fa82a`  
		Last Modified: Sun, 02 Feb 2020 06:46:37 GMT  
		Size: 12.3 MB (12250528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b31054a2d37dea9f1a0496281ab2d12c4bb8a69bc220f273463e9bb30ed7b28`  
		Last Modified: Sun, 02 Feb 2020 06:46:37 GMT  
		Size: 11.4 MB (11405704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab450ad9ca67345d2fcca9f78f252fe9e514c4e41b8fa83479a5ef48d5417fa7`  
		Last Modified: Sun, 02 Feb 2020 06:46:31 GMT  
		Size: 596.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f763cf550d8d4accf893d22cab2a285e11f7435d147fde1cdd974e756c5e476`  
		Last Modified: Sun, 02 Feb 2020 06:46:31 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2dcf890913cb1a6acde95e6f9d9258aa1c85169696d753dd77bf1c92266d7c7`  
		Last Modified: Sun, 02 Feb 2020 06:46:47 GMT  
		Size: 57.5 MB (57542450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ddc0e9a14bf593634497f46fccfe65c2244dd1df0b212aa4192f20b92f3925`  
		Last Modified: Sun, 02 Feb 2020 06:46:31 GMT  
		Size: 2.2 KB (2180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2951d32957831770233bb6c68615ebde651e2608034547fa9e4f58379b328ab`  
		Last Modified: Sun, 02 Feb 2020 06:46:31 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:apache` - linux; arm variant v7

```console
$ docker pull friendica@sha256:3f3240a6bdafa39762b61766ae8a1bd73ef84305532adbd92862ee1e2e4dd6a8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194378246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d080291dd05d13e9dd8993f66ef782eb65b99c6094bd029ebeae572168d86ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 01:32:10 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sun, 02 Feb 2020 01:32:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sun, 02 Feb 2020 01:32:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 01:32:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sun, 02 Feb 2020 01:33:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sun, 02 Feb 2020 01:37:30 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sun, 02 Feb 2020 01:37:32 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sun, 02 Feb 2020 01:37:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sun, 02 Feb 2020 01:37:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sun, 02 Feb 2020 01:38:01 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sun, 02 Feb 2020 01:38:03 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sun, 02 Feb 2020 01:38:03 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sun, 02 Feb 2020 01:38:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 02 Feb 2020 01:38:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 02 Feb 2020 01:38:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sun, 02 Feb 2020 01:38:06 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 20 Feb 2020 21:45:58 GMT
ENV PHP_VERSION=7.3.15
# Thu, 20 Feb 2020 21:45:58 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.15.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.15.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:45:59 GMT
ENV PHP_SHA256=de7ae7cf3d1dbb2824975b26b32991dac2b732886ec22075b8c53b261b018166 PHP_MD5=
# Thu, 20 Feb 2020 21:46:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 20 Feb 2020 21:46:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:49:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	sed -e 's/stretch/buster/g' /etc/apt/sources.list > /etc/apt/sources.list.d/buster.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libargon2*'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/argon2-buster; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:49:28 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:49:31 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:49:32 GMT
STOPSIGNAL SIGWINCH
# Thu, 20 Feb 2020 21:49:33 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:49:34 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 21:49:35 GMT
EXPOSE 80
# Thu, 20 Feb 2020 21:49:37 GMT
CMD ["apache2-foreground"]
# Fri, 21 Feb 2020 00:05:09 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         ssmtp     ;     rm -rf /var/lib/apt/lists/*;
# Fri, 21 Feb 2020 00:10:26 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mysql-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         	--with-libdir=lib/$debMultiarch/ 	;     docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.1.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so       | awk '/=>/ { print $3 }'       | sort -u       | xargs -r dpkg-query -S       | cut -d: -f1       | sort -u       | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 00:10:32 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 21 Feb 2020 00:10:34 GMT
VOLUME [/var/www/html]
# Fri, 21 Feb 2020 00:10:36 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Fri, 21 Feb 2020 00:10:37 GMT
ENV FRIENDICA_VERSION=2019.12
# Fri, 21 Feb 2020 00:10:38 GMT
ENV FRIENDICA_ADDONS=2019.12
# Fri, 21 Feb 2020 00:11:13 GMT
RUN set -ex;     curl -fsSL -o friendica.tar.gz         "https://github.com/friendica/friendica/archive/${FRIENDICA_VERSION}.tar.gz";     tar -xzf friendica.tar.gz -C /usr/src/;     rm friendica.tar.gz;     mv -f /usr/src/friendica-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;     curl -fsSL -o friendica_addons.tar.gz         "https://github.com/friendica/friendica-addons/archive/${FRIENDICA_ADDONS}.tar.gz";     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica_addons.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica_addons.tar.gz;     /usr/src/friendica/bin/composer.phar install --no-dev -d /usr/src/friendica;
# Fri, 21 Feb 2020 00:11:16 GMT
COPY multi:0a5bdeeeece27826a5344be9215b3de17c80ece34c27fd9cf4c61a0c7e730616 in / 
# Fri, 21 Feb 2020 00:11:17 GMT
COPY multi:ccf608c3083a2548ed80248e6308632e395ce7dfbcb83d73bfba22293ecd8ffd in /usr/src/friendica/config/ 
# Fri, 21 Feb 2020 00:11:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Feb 2020 00:11:19 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099deb873b7e7fc11c23079642ad77d792b193531b444309c85f16e1c26397a1`  
		Last Modified: Sun, 02 Feb 2020 02:32:00 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afdae3edc22f44280cb0a7333e56ec454de70ead053a8eedad80241611aac2a4`  
		Last Modified: Sun, 02 Feb 2020 02:32:18 GMT  
		Size: 53.6 MB (53588725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffcfcd19002e317670fcee9266299ec0b23513ea8f531db4def36bdf05db462`  
		Last Modified: Sun, 02 Feb 2020 02:32:00 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f178a256ff88f86468140b0c714e9c7048200a5d0f3794f41e878108e45429bf`  
		Last Modified: Sun, 02 Feb 2020 02:32:34 GMT  
		Size: 16.2 MB (16159700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8281f85e331fec8605168d2cfebafcedc951e008990f3f8eb1d8622d911f62`  
		Last Modified: Sun, 02 Feb 2020 02:32:30 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fac594b79892eb5c02a28607dd00ac5dfb97ee66f618041212cdd6b182954cb`  
		Last Modified: Sun, 02 Feb 2020 02:32:30 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ef90b3e90dd468294c4764da2f3a1e97cc01cc010b36128778eeddfde7858d`  
		Last Modified: Thu, 20 Feb 2020 23:29:53 GMT  
		Size: 12.5 MB (12459359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f11790836f3a0167483367930e5f7d8ec6bb6c9cc3f94ed91690dd5bf2a17f`  
		Last Modified: Thu, 20 Feb 2020 23:29:49 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b13f724c21709f778761ca442de49bd901e79672bcbc0d147d3323c41e1ac3`  
		Last Modified: Thu, 20 Feb 2020 23:29:54 GMT  
		Size: 12.4 MB (12414244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c32b2c5464a0f4277b7f9679aa1ab359189f3b00663a50b6fb0fce1d009920`  
		Last Modified: Thu, 20 Feb 2020 23:29:50 GMT  
		Size: 2.2 KB (2238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b188d81eb61075300d52237c3e3cffe32078db57f0442e0d21e501cef812c5ac`  
		Last Modified: Thu, 20 Feb 2020 23:29:50 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98bcdd7c03cad6b590a450e9d82ff8f058c13aea012cc8334c3695c7268ceb3`  
		Last Modified: Thu, 20 Feb 2020 23:29:49 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f07b4b8ec1c62b3a7af0cede057f0303bec0259cf44f66c0351aa65cd71017`  
		Last Modified: Fri, 21 Feb 2020 00:23:25 GMT  
		Size: 11.1 MB (11143680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f678227de432efe63cb3b0f26b67a76fa7f317fc8a271cfde3c93268ce591b3e`  
		Last Modified: Fri, 21 Feb 2020 00:23:26 GMT  
		Size: 11.7 MB (11748728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9c698efb86c9e620051d63d9688263521d45e408689ba2ff689ca471a1bfcb`  
		Last Modified: Fri, 21 Feb 2020 00:23:20 GMT  
		Size: 597.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cc9e721a13e6482a7aeabbe6065f890ff8300176d79429d121364ba69df644`  
		Last Modified: Fri, 21 Feb 2020 00:23:20 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1af987a310d4308a9600adf5f2e41873fbab1ccf03048ad4594a3addbfa820f`  
		Last Modified: Fri, 21 Feb 2020 00:23:41 GMT  
		Size: 57.5 MB (57542378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3444b44995cd1588d895e1cf713ef4264ccc7b4a310ad356da8f99bfbf3d02`  
		Last Modified: Fri, 21 Feb 2020 00:23:20 GMT  
		Size: 2.2 KB (2180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb1f4d936aa6d506bbb2d88eb5350dfb802beb4d6555e3ec7030c530c0ed1fa`  
		Last Modified: Fri, 21 Feb 2020 00:23:20 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:apache` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:9ccc5faef4255f8dd6b045afcf907daf79e04c9f37e09510cef0b4e99569d5b9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.2 MB (200150650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69786fb97b2596ed7e8314284533c85e59b5e9e6f5c61373014066b0770a749`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 08:39:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sun, 02 Feb 2020 08:39:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sun, 02 Feb 2020 08:40:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 08:40:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sun, 02 Feb 2020 08:40:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sun, 02 Feb 2020 08:44:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sun, 02 Feb 2020 08:44:44 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sun, 02 Feb 2020 08:45:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sun, 02 Feb 2020 08:45:07 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sun, 02 Feb 2020 08:45:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sun, 02 Feb 2020 08:45:10 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sun, 02 Feb 2020 08:45:11 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sun, 02 Feb 2020 08:45:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 02 Feb 2020 08:45:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 02 Feb 2020 08:45:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sun, 02 Feb 2020 08:45:14 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Sun, 02 Feb 2020 08:45:15 GMT
ENV PHP_VERSION=7.3.14
# Sun, 02 Feb 2020 08:45:16 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.14.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.14.tar.xz.asc/from/this/mirror
# Sun, 02 Feb 2020 08:45:17 GMT
ENV PHP_SHA256=cc05dd373ca5d36652800762f65c10e828a17de35aaf246262e3efa99d00cdb0 PHP_MD5=
# Sun, 02 Feb 2020 08:45:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 08:45:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sun, 02 Feb 2020 08:48:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	sed -e 's/stretch/buster/g' /etc/apt/sources.list > /etc/apt/sources.list.d/buster.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libargon2*'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/argon2-buster; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Sun, 02 Feb 2020 08:48:56 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Sun, 02 Feb 2020 08:49:00 GMT
RUN docker-php-ext-enable sodium
# Sun, 02 Feb 2020 08:49:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sun, 02 Feb 2020 08:49:01 GMT
STOPSIGNAL SIGWINCH
# Sun, 02 Feb 2020 08:49:02 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sun, 02 Feb 2020 08:49:03 GMT
WORKDIR /var/www/html
# Sun, 02 Feb 2020 08:49:04 GMT
EXPOSE 80
# Sun, 02 Feb 2020 08:49:05 GMT
CMD ["apache2-foreground"]
# Sun, 02 Feb 2020 17:26:52 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         ssmtp     ;     rm -rf /var/lib/apt/lists/*;
# Sun, 02 Feb 2020 17:31:45 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mysql-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         	--with-libdir=lib/$debMultiarch/ 	;     docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.1.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so       | awk '/=>/ { print $3 }'       | sort -u       | xargs -r dpkg-query -S       | cut -d: -f1       | sort -u       | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 17:31:48 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Sun, 02 Feb 2020 17:31:49 GMT
VOLUME [/var/www/html]
# Sun, 02 Feb 2020 17:31:51 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Sun, 02 Feb 2020 17:31:52 GMT
ENV FRIENDICA_VERSION=2019.12
# Sun, 02 Feb 2020 17:31:52 GMT
ENV FRIENDICA_ADDONS=2019.12
# Sun, 02 Feb 2020 17:32:23 GMT
RUN set -ex;     curl -fsSL -o friendica.tar.gz         "https://github.com/friendica/friendica/archive/${FRIENDICA_VERSION}.tar.gz";     tar -xzf friendica.tar.gz -C /usr/src/;     rm friendica.tar.gz;     mv -f /usr/src/friendica-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;     curl -fsSL -o friendica_addons.tar.gz         "https://github.com/friendica/friendica-addons/archive/${FRIENDICA_ADDONS}.tar.gz";     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica_addons.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica_addons.tar.gz;     /usr/src/friendica/bin/composer.phar install --no-dev -d /usr/src/friendica;
# Sun, 02 Feb 2020 17:32:26 GMT
COPY multi:0a5bdeeeece27826a5344be9215b3de17c80ece34c27fd9cf4c61a0c7e730616 in / 
# Sun, 02 Feb 2020 17:32:27 GMT
COPY multi:ccf608c3083a2548ed80248e6308632e395ce7dfbcb83d73bfba22293ecd8ffd in /usr/src/friendica/config/ 
# Sun, 02 Feb 2020 17:32:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 02 Feb 2020 17:32:28 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08d60a9d7bf9f53306a002e82dd70a45df04ff49eedae934a49db14115823aa`  
		Last Modified: Sun, 02 Feb 2020 09:37:12 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123ad43560c05687c36c90e4a7a7aa587bb733cd6c945065c2884471e574bb49`  
		Last Modified: Sun, 02 Feb 2020 09:37:30 GMT  
		Size: 57.6 MB (57626705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050a324fb4e6684d47021c9b2cfa76645a39c6796e8dd6cc1e1f451a8f0a355`  
		Last Modified: Sun, 02 Feb 2020 09:37:12 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace95a2ea7e7f5b6055284ff34d46e155853fb99c02c3be5f961d969fbab2ebe`  
		Last Modified: Sun, 02 Feb 2020 09:37:46 GMT  
		Size: 16.7 MB (16707968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453c2dd119e83c8850410b065ee56827faa2f48a1d7e5de8e00334cb2dccfd96`  
		Last Modified: Sun, 02 Feb 2020 09:37:41 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9e7262ee64d89ac33942830cc4e904872fda1e0edb7b5eab7ec973527ec25a`  
		Last Modified: Sun, 02 Feb 2020 09:37:41 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637bec465acfca1180a400ac213eaf43cbe17f7d07eb5a0ca4d2e37787c0e608`  
		Last Modified: Sun, 02 Feb 2020 09:37:42 GMT  
		Size: 12.5 MB (12452948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bccf1718353e6246bbafaa141c2f2f517bce825a9975626c75cae0b5237bddb5`  
		Last Modified: Sun, 02 Feb 2020 09:37:39 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe63703f09785c4a9a177151b3c6da04518fc8c71677f75e64ae4c085f3c878`  
		Last Modified: Sun, 02 Feb 2020 09:37:44 GMT  
		Size: 12.9 MB (12885763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d3995e54e729e49194560c89e95f632ba4869d14e57da6d67e497679ed0f0f`  
		Last Modified: Sun, 02 Feb 2020 09:37:39 GMT  
		Size: 2.2 KB (2242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c0dc66b88b92e53a82193256e99e5364119c630b03e4073cbbc112e4549e653`  
		Last Modified: Sun, 02 Feb 2020 09:37:39 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0718f815fd80218f0027f4599830b24a7e9682fd90fc7af69a3e8cfe8908fb58`  
		Last Modified: Sun, 02 Feb 2020 09:37:39 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24585fe7abdc3a52e88a75d3ed1bcb150654e43b9269369a632a17513871bede`  
		Last Modified: Sun, 02 Feb 2020 17:39:27 GMT  
		Size: 11.9 MB (11913345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f210ece49e3072557544185bf38e211243fa4df9bb9721fcbd82e36fa8909ade`  
		Last Modified: Sun, 02 Feb 2020 17:39:27 GMT  
		Size: 10.6 MB (10625783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cf88d42b8145e7ad844ecc227abd76f448b27448d8843b7ebbfb45a7f3a3b4`  
		Last Modified: Sun, 02 Feb 2020 17:39:21 GMT  
		Size: 596.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1fd0be9add006d38692523e35795b654758a19292e8a5056b9198451de4abe`  
		Last Modified: Sun, 02 Feb 2020 17:39:21 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99a6b7e79fae7a2fa5ba59c9595b0bba569e76a1b9a3a6a4341392367e09708`  
		Last Modified: Sun, 02 Feb 2020 17:39:33 GMT  
		Size: 57.5 MB (57542470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53a6ff211ca99a2b00dd7398d1c4e194af003e45a3c6e86455541c1a2a25cfc`  
		Last Modified: Sun, 02 Feb 2020 17:39:21 GMT  
		Size: 2.2 KB (2180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea58792dc5700b2b7aa8d588eca701a3c785687341a77f96b5b52c890e5ad5f9`  
		Last Modified: Sun, 02 Feb 2020 17:39:22 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:apache` - linux; 386

```console
$ docker pull friendica@sha256:95e981933007c9872c254382e656ffefeb33ac43a6bc292bbbfcbcc4a9ee6a2a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.8 MB (222809255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acdc1c179f7b3a31083bb26335c94db7421f65c4331b423346169bb7b2d563fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 01 Feb 2020 16:42:07 GMT
ADD file:c9b4696be461d46d96c760441f34e219e229f90bc6946125b2f809218c3456ce in / 
# Sat, 01 Feb 2020 16:42:07 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 02:39:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sun, 02 Feb 2020 02:39:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sun, 02 Feb 2020 02:39:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 02:39:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sun, 02 Feb 2020 02:39:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sun, 02 Feb 2020 02:48:25 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sun, 02 Feb 2020 02:48:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sun, 02 Feb 2020 02:48:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sun, 02 Feb 2020 02:48:39 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sun, 02 Feb 2020 02:48:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sun, 02 Feb 2020 02:48:40 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sun, 02 Feb 2020 02:48:40 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sun, 02 Feb 2020 02:48:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 02 Feb 2020 02:48:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 02 Feb 2020 02:48:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sun, 02 Feb 2020 02:48:41 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Sun, 02 Feb 2020 02:48:41 GMT
ENV PHP_VERSION=7.3.14
# Sun, 02 Feb 2020 02:48:41 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.14.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.14.tar.xz.asc/from/this/mirror
# Sun, 02 Feb 2020 02:48:41 GMT
ENV PHP_SHA256=cc05dd373ca5d36652800762f65c10e828a17de35aaf246262e3efa99d00cdb0 PHP_MD5=
# Sun, 02 Feb 2020 02:48:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 02:48:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sun, 02 Feb 2020 02:54:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	sed -e 's/stretch/buster/g' /etc/apt/sources.list > /etc/apt/sources.list.d/buster.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libargon2*'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/argon2-buster; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Sun, 02 Feb 2020 02:54:44 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Sun, 02 Feb 2020 02:54:46 GMT
RUN docker-php-ext-enable sodium
# Sun, 02 Feb 2020 02:54:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sun, 02 Feb 2020 02:54:47 GMT
STOPSIGNAL SIGWINCH
# Sun, 02 Feb 2020 02:54:47 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sun, 02 Feb 2020 02:54:47 GMT
WORKDIR /var/www/html
# Sun, 02 Feb 2020 02:54:48 GMT
EXPOSE 80
# Sun, 02 Feb 2020 02:54:48 GMT
CMD ["apache2-foreground"]
# Sun, 02 Feb 2020 12:51:48 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         ssmtp     ;     rm -rf /var/lib/apt/lists/*;
# Sun, 02 Feb 2020 12:55:24 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mysql-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         	--with-libdir=lib/$debMultiarch/ 	;     docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.1.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so       | awk '/=>/ { print $3 }'       | sort -u       | xargs -r dpkg-query -S       | cut -d: -f1       | sort -u       | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 12:55:26 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Sun, 02 Feb 2020 12:55:26 GMT
VOLUME [/var/www/html]
# Sun, 02 Feb 2020 12:55:28 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Sun, 02 Feb 2020 12:55:28 GMT
ENV FRIENDICA_VERSION=2019.12
# Sun, 02 Feb 2020 12:55:28 GMT
ENV FRIENDICA_ADDONS=2019.12
# Sun, 02 Feb 2020 12:55:56 GMT
RUN set -ex;     curl -fsSL -o friendica.tar.gz         "https://github.com/friendica/friendica/archive/${FRIENDICA_VERSION}.tar.gz";     tar -xzf friendica.tar.gz -C /usr/src/;     rm friendica.tar.gz;     mv -f /usr/src/friendica-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;     curl -fsSL -o friendica_addons.tar.gz         "https://github.com/friendica/friendica-addons/archive/${FRIENDICA_ADDONS}.tar.gz";     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica_addons.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica_addons.tar.gz;     /usr/src/friendica/bin/composer.phar install --no-dev -d /usr/src/friendica;
# Sun, 02 Feb 2020 12:55:58 GMT
COPY multi:0a5bdeeeece27826a5344be9215b3de17c80ece34c27fd9cf4c61a0c7e730616 in / 
# Sun, 02 Feb 2020 12:55:59 GMT
COPY multi:ccf608c3083a2548ed80248e6308632e395ce7dfbcb83d73bfba22293ecd8ffd in /usr/src/friendica/config/ 
# Sun, 02 Feb 2020 12:55:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 02 Feb 2020 12:55:59 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4f51b031b74b1f7fab6310c197fd7534181ba2db1f0cec6686fb9e9a82abbb9c`  
		Last Modified: Sat, 01 Feb 2020 16:47:27 GMT  
		Size: 23.2 MB (23152156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82cdeebb6984db938584eda1b704692b62e6b396e5ff78b46145e1d89b25ee8`  
		Last Modified: Sun, 02 Feb 2020 04:21:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90369919eaf01ae5de522fca908064ce7dde2d7b1fd385c302e6e74d8973318`  
		Last Modified: Sun, 02 Feb 2020 04:22:10 GMT  
		Size: 71.5 MB (71523964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ffa35653c8b4f43e5eee2575903776eb1d8d25451588701a0f8e64d7946214`  
		Last Modified: Sun, 02 Feb 2020 04:21:40 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d28bd933072c96b8f69765254819ea2ac1201bd34c3b83961ec8f06bed366d6`  
		Last Modified: Sun, 02 Feb 2020 04:22:30 GMT  
		Size: 17.6 MB (17559463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76669ade1ec8fdc6724a4dcce40d44b6c66aa82562fac73af6ede965298f82c`  
		Last Modified: Sun, 02 Feb 2020 04:22:21 GMT  
		Size: 431.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785e55e653b5540110ccf0ea51d6ee068ae630becf4cb22d0d20546dda049393`  
		Last Modified: Sun, 02 Feb 2020 04:22:20 GMT  
		Size: 487.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e699dff50abb8b5be91dd08f28f5db1ac997c489f305b326a2094df92e6026`  
		Last Modified: Sun, 02 Feb 2020 04:22:24 GMT  
		Size: 12.5 MB (12454665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c558abc54eb1653a139d5ddf9d55edd20955e636240cd994b7c0146daa3aa506`  
		Last Modified: Sun, 02 Feb 2020 04:22:19 GMT  
		Size: 502.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b68d8910e422b9b0ad61b05b3d6b930d098f9b1ac1608064d94659eef23018`  
		Last Modified: Sun, 02 Feb 2020 04:22:30 GMT  
		Size: 14.1 MB (14141766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfc4cff8d8cf0a3cdd6fd56570f1c29c959c0b93a5f6401edbae5de34ab3cb0a`  
		Last Modified: Sun, 02 Feb 2020 04:22:19 GMT  
		Size: 2.2 KB (2238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3087c43b01d7a2ca0a359b6f025ac9cdae9748b57614f778ab58a481d2f57db9`  
		Last Modified: Sun, 02 Feb 2020 04:22:19 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481af0dbaf217bd656b66dca03f5ff53b72bce9e091a8aa54c666042dfd24909`  
		Last Modified: Sun, 02 Feb 2020 04:22:19 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9afbab5dd869cd78e378ce81652e1b1c5158a7f07682b29e8cd2c7313843985`  
		Last Modified: Sun, 02 Feb 2020 13:01:59 GMT  
		Size: 14.7 MB (14708574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3f1f2f8292f34f37cfd5e9ae25ca4e02f7512709bff7dd22895f58c69f80ff`  
		Last Modified: Sun, 02 Feb 2020 13:01:59 GMT  
		Size: 11.7 MB (11716612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adee90845ea3d718a0a42588647ab004fae863de29e393b69b1f08b7ee7cb2a7`  
		Last Modified: Sun, 02 Feb 2020 13:01:48 GMT  
		Size: 565.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13ddde562f6a47668e2f6dda9400624530b3fbc4698a311e7828accf1d829d7`  
		Last Modified: Sun, 02 Feb 2020 13:01:48 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff04d38567427170b66ee1c70ab65577791918bec418064bf807b83bb37e7e86`  
		Last Modified: Sun, 02 Feb 2020 13:02:12 GMT  
		Size: 57.5 MB (57542398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8723ddd955043a6c7e2645ca4ca6c72b13be92461343441b911922da69efbccc`  
		Last Modified: Sun, 02 Feb 2020 13:01:48 GMT  
		Size: 2.2 KB (2180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa9cf875c6beade855f86499703bfadc9cbc7e02422cbe9e9676709117594e9`  
		Last Modified: Sun, 02 Feb 2020 13:01:48 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:apache` - linux; ppc64le

```console
$ docker pull friendica@sha256:e9798a867deebe70541fc54b9f61c9841a6b26c1e713ca2390b5f15fac9ca597
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (210042832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814c4bdbca8797817fe962a1160fac0d28f1a06c97bf9ab16416161d8e61a726`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:8840e8b11ab671d52cc308dfcd68117cbff88d7e5e18e0628683d75699a7c131 in / 
# Sat, 01 Feb 2020 17:20:49 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 09:47:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sun, 02 Feb 2020 09:47:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sun, 02 Feb 2020 09:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 09:49:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sun, 02 Feb 2020 09:50:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sun, 02 Feb 2020 09:56:20 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sun, 02 Feb 2020 09:56:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sun, 02 Feb 2020 09:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sun, 02 Feb 2020 09:57:39 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sun, 02 Feb 2020 09:57:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sun, 02 Feb 2020 09:57:50 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sun, 02 Feb 2020 09:57:53 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sun, 02 Feb 2020 09:58:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 02 Feb 2020 09:58:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 02 Feb 2020 09:58:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sun, 02 Feb 2020 09:58:15 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Sun, 02 Feb 2020 09:58:18 GMT
ENV PHP_VERSION=7.3.14
# Sun, 02 Feb 2020 09:58:21 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.14.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.14.tar.xz.asc/from/this/mirror
# Sun, 02 Feb 2020 09:58:29 GMT
ENV PHP_SHA256=cc05dd373ca5d36652800762f65c10e828a17de35aaf246262e3efa99d00cdb0 PHP_MD5=
# Sun, 02 Feb 2020 09:59:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 09:59:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sun, 02 Feb 2020 10:04:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	sed -e 's/stretch/buster/g' /etc/apt/sources.list > /etc/apt/sources.list.d/buster.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libargon2*'; 		echo 'Pin: release n=buster'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/argon2-buster; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Sun, 02 Feb 2020 10:04:06 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Sun, 02 Feb 2020 10:04:17 GMT
RUN docker-php-ext-enable sodium
# Sun, 02 Feb 2020 10:04:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sun, 02 Feb 2020 10:04:28 GMT
STOPSIGNAL SIGWINCH
# Sun, 02 Feb 2020 10:04:29 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sun, 02 Feb 2020 10:04:37 GMT
WORKDIR /var/www/html
# Sun, 02 Feb 2020 10:04:42 GMT
EXPOSE 80
# Sun, 02 Feb 2020 10:04:48 GMT
CMD ["apache2-foreground"]
# Sun, 02 Feb 2020 18:47:18 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         ssmtp     ;     rm -rf /var/lib/apt/lists/*;
# Sun, 02 Feb 2020 18:56:51 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mysql-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         	--with-libdir=lib/$debMultiarch/ 	;     docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.1.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so       | awk '/=>/ { print $3 }'       | sort -u       | xargs -r dpkg-query -S       | cut -d: -f1       | sort -u       | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 18:56:57 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/sbin/sendmail -t -i";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Sun, 02 Feb 2020 18:57:00 GMT
VOLUME [/var/www/html]
# Sun, 02 Feb 2020 18:57:06 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Sun, 02 Feb 2020 18:57:09 GMT
ENV FRIENDICA_VERSION=2019.12
# Sun, 02 Feb 2020 18:57:14 GMT
ENV FRIENDICA_ADDONS=2019.12
# Sun, 02 Feb 2020 18:57:57 GMT
RUN set -ex;     curl -fsSL -o friendica.tar.gz         "https://github.com/friendica/friendica/archive/${FRIENDICA_VERSION}.tar.gz";     tar -xzf friendica.tar.gz -C /usr/src/;     rm friendica.tar.gz;     mv -f /usr/src/friendica-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;     curl -fsSL -o friendica_addons.tar.gz         "https://github.com/friendica/friendica-addons/archive/${FRIENDICA_ADDONS}.tar.gz";     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica_addons.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica_addons.tar.gz;     /usr/src/friendica/bin/composer.phar install --no-dev -d /usr/src/friendica;
# Sun, 02 Feb 2020 18:58:03 GMT
COPY multi:0a5bdeeeece27826a5344be9215b3de17c80ece34c27fd9cf4c61a0c7e730616 in / 
# Sun, 02 Feb 2020 18:58:05 GMT
COPY multi:ccf608c3083a2548ed80248e6308632e395ce7dfbcb83d73bfba22293ecd8ffd in /usr/src/friendica/config/ 
# Sun, 02 Feb 2020 18:58:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 02 Feb 2020 18:58:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4b12198d119cc40a2102fa8f986f1f3bc6f22967a421939f96b52470129050b9`  
		Last Modified: Sat, 01 Feb 2020 17:31:15 GMT  
		Size: 22.8 MB (22800759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c42cb6df476f11485125aede4e147b91667034e18c29f48b7ed498b4f390da0`  
		Last Modified: Sun, 02 Feb 2020 11:11:20 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddf9629003d9ffc23aab0afc7ee5d0bb952a2c9467b62546a8e7960064a67c4`  
		Last Modified: Sun, 02 Feb 2020 11:11:36 GMT  
		Size: 61.8 MB (61837503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55415420d1cf8f38d9d64e9445f2b42b19d2ea3fdb92a4f88a6572422595ad6d`  
		Last Modified: Sun, 02 Feb 2020 11:11:19 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096d7f0f3d645ddaa5d2dae8cfb7bc4d4c7cb3046b8191fd362ced50a6c55c2b`  
		Last Modified: Sun, 02 Feb 2020 11:12:02 GMT  
		Size: 17.3 MB (17340500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9973a40650efe8a24193d53cf0c43fe6ac6ed5087c91955ee48f58ca6f67b5c`  
		Last Modified: Sun, 02 Feb 2020 11:11:57 GMT  
		Size: 481.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d82f87cd588468cabe531dcdc11fcbcfcb4a7d5354bc5bada46882b23860fd`  
		Last Modified: Sun, 02 Feb 2020 11:11:57 GMT  
		Size: 518.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d1068d11a00ed2f80a0494b5f065ba9a879bfdaffd8d2987c4dcbc49111ec3`  
		Last Modified: Sun, 02 Feb 2020 11:11:58 GMT  
		Size: 12.5 MB (12453579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e7d91f9f70832e0b327512951b9a089b21732b74584950410bbaa9b6336d005`  
		Last Modified: Sun, 02 Feb 2020 11:11:52 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49fad912fe20ebb95a82fb837cc2fc1f0d8d8f7ac37cbdbaaef5a30eee49b03`  
		Last Modified: Sun, 02 Feb 2020 11:11:57 GMT  
		Size: 13.6 MB (13612914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b401f1bf20d90a3dfb171183b9d167b18f31a1f08d88828cc10b19bc091e3c19`  
		Last Modified: Sun, 02 Feb 2020 11:11:53 GMT  
		Size: 2.2 KB (2239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17933dd2ac121871cb8671f4724c9ff16fa2bd6a5f51b62e9144c5ec3f8e9189`  
		Last Modified: Sun, 02 Feb 2020 11:11:53 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2394a26982e9e10768f1aedfc10704e4277a428fb2c7aee6b607385dbc8405d9`  
		Last Modified: Sun, 02 Feb 2020 11:11:53 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297ff49e4dfc1d9e6ac72024dd221201b47378d100612118f10381ff8c3542f6`  
		Last Modified: Sun, 02 Feb 2020 19:09:29 GMT  
		Size: 13.1 MB (13080112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab905f2fa32e975a62d16c8423d8744751625ce6444ad37adb916b43800c484`  
		Last Modified: Sun, 02 Feb 2020 19:09:29 GMT  
		Size: 11.4 MB (11364983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b6f9b72838c5319e4962d75277f2bc94874813845c7ac8014556b5c46e60f0`  
		Last Modified: Sun, 02 Feb 2020 19:09:23 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c3d9c2d38a8fd659ac7bb2bda00e60cf97841a9600516e273ebf1e062efff8`  
		Last Modified: Sun, 02 Feb 2020 19:09:23 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c253147bbc461b420c89ac4c933e907eb68596d29fbd7751d4d2ecb4d7650b`  
		Last Modified: Sun, 02 Feb 2020 19:09:35 GMT  
		Size: 57.5 MB (57542665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722b2ca40486e67c658673e8b4bbd43bc95c4c45ddd76b381a0601faad0aebc1`  
		Last Modified: Sun, 02 Feb 2020 19:09:23 GMT  
		Size: 2.2 KB (2180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1435beee46ca59fdc1a5af37dca07c92e7995edced21c95af32287ea0ee9166a`  
		Last Modified: Sun, 02 Feb 2020 19:09:23 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
