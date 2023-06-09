## `drupal:9-php8.0-fpm-buster`

```console
$ docker pull drupal@sha256:d1f07fc7a0011db8506044b5e7f55f8763159b2e2e0d94a135b27f055e0385ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `drupal:9-php8.0-fpm-buster` - linux; amd64

```console
$ docker pull drupal@sha256:6c260a2f6fed2707f5817a9f054c2c902c4dce9deaa08336985980d89ac0d521
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168134448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17047bdef913c154e866cc71a666f3bbd26af2c1b5372b900597a62a4df8527`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 May 2023 01:20:37 GMT
ADD file:2058e04b33179527a56999678c1c62dfcf76944675afcd77b5163141fb025f8c in / 
# Tue, 23 May 2023 01:20:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 09:49:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 May 2023 09:49:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 May 2023 09:50:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 09:50:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 May 2023 09:50:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 May 2023 09:50:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:50:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:50:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 May 2023 10:41:54 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Fri, 09 Jun 2023 02:13:00 GMT
ENV PHP_VERSION=8.0.29
# Fri, 09 Jun 2023 02:13:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.29.tar.xz.asc
# Fri, 09 Jun 2023 02:13:00 GMT
ENV PHP_SHA256=14db2fbf26c07d0eb2c9fab25dbde7e27726a3e88452cca671f0896bbb683ca9
# Fri, 09 Jun 2023 02:13:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 09 Jun 2023 02:13:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 09 Jun 2023 02:22:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 09 Jun 2023 02:22:23 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 09 Jun 2023 02:22:24 GMT
RUN docker-php-ext-enable sodium
# Fri, 09 Jun 2023 02:22:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jun 2023 02:22:24 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 02:22:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 09 Jun 2023 02:22:24 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jun 2023 02:22:25 GMT
EXPOSE 9000
# Fri, 09 Jun 2023 02:22:25 GMT
CMD ["php-fpm"]
# Fri, 09 Jun 2023 03:35:16 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Jun 2023 03:35:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 09 Jun 2023 03:35:17 GMT
COPY file:24bf6e4ff958bf58ae126804a93affdbd6a0bf41615cc91af3f7538a88742dbd in /usr/local/bin/ 
# Fri, 09 Jun 2023 03:35:17 GMT
ENV DRUPAL_VERSION=9.5.9
# Fri, 09 Jun 2023 03:35:17 GMT
WORKDIR /opt/drupal
# Fri, 09 Jun 2023 03:35:27 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Fri, 09 Jun 2023 03:35:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:99bf4787315b60d97d860ac6d006b7835b2241a601e93c2da4af6ca554be8704`  
		Last Modified: Tue, 23 May 2023 01:24:47 GMT  
		Size: 27.1 MB (27138577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55ada1538ae196b25fb974bc489a28592c4e563e5a4a142019da8a502fe84de`  
		Last Modified: Tue, 23 May 2023 10:58:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1deafc62e11b7180330eb4bad22f026f77a0b73e54fcbc51c3d33a91a58ac6`  
		Last Modified: Tue, 23 May 2023 10:58:11 GMT  
		Size: 76.7 MB (76694428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a88ed5b391830f741f158fcfe5f6fc1fd3c12fd510b68e05634de91e8402ec0`  
		Last Modified: Tue, 23 May 2023 10:58:00 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62bb2418edfa9fc87282f927770f80257999233146380e3d39be6d3355dfdfb`  
		Last Modified: Fri, 09 Jun 2023 02:54:18 GMT  
		Size: 11.1 MB (11126772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388f9b7e388a352f4004cd049a5d4df05e28ebab73df7d61cc291510b4489ef3`  
		Last Modified: Fri, 09 Jun 2023 02:54:17 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63865d4d1e7eff0db976d121fa2d1eaf5c4bd8eef3ce8ec45d14acf07c2484f`  
		Last Modified: Fri, 09 Jun 2023 02:54:51 GMT  
		Size: 27.4 MB (27361539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96acd00935fa73576d84136a0c6cd2b9e0dc18839207fdb935695ef46bad6d27`  
		Last Modified: Fri, 09 Jun 2023 02:54:47 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802be4fdcd7f4a02eca8bfbd8edb0a2105499ec13a71ced431713d657a8cf53f`  
		Last Modified: Fri, 09 Jun 2023 02:54:47 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d5cea987919b211ea3ad45bc43bf78b784af0efd0d537c74de347ed5ac6372`  
		Last Modified: Fri, 09 Jun 2023 02:54:47 GMT  
		Size: 8.7 KB (8719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77bd1ffafb4e540b2c6bae6c6444a69b8b3222ba380df59155a2ed6403c55774`  
		Last Modified: Fri, 09 Jun 2023 03:53:23 GMT  
		Size: 2.2 MB (2223565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db3c48abb8108e8ccfbc910e4692cfe7b320d374ef266adeace659e8cb525b7`  
		Last Modified: Fri, 09 Jun 2023 03:53:22 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335767764067d128e3d3334b32c1ad6ad1e40174b6c13a348d7669ea00b30dad`  
		Last Modified: Fri, 09 Jun 2023 03:53:22 GMT  
		Size: 698.2 KB (698151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618fdb16dc7cac1e6365cb838a7acbf6b9d298235b052b21fa0efddddb4e6331`  
		Last Modified: Fri, 09 Jun 2023 03:53:22 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085de9ae8fae7097a956c9d87d17c4717867bb08da0cbd79e404dec388997258`  
		Last Modified: Fri, 09 Jun 2023 03:53:27 GMT  
		Size: 22.9 MB (22878544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-php8.0-fpm-buster` - linux; arm variant v7

```console
$ docker pull drupal@sha256:58a3125b71c506eed4804841da616752e12c5cab1f8dbb6470676442cbceb3b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141834446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d3cee34d84d3a5e71bc37b8b185acd122183302a90c445074c4e4f85b4afe6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 May 2023 00:58:17 GMT
ADD file:fc75413703cf08c1fc3b981ebbde07494b7ad8176aadd5f3a8fb891f0c48e7b9 in / 
# Tue, 23 May 2023 00:58:17 GMT
CMD ["bash"]
# Tue, 23 May 2023 07:08:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 May 2023 07:08:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 May 2023 07:08:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:08:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 May 2023 07:08:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 May 2023 07:09:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 07:09:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 07:09:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 May 2023 07:50:10 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Tue, 23 May 2023 07:50:10 GMT
ENV PHP_VERSION=8.0.28
# Tue, 23 May 2023 07:50:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.28.tar.xz.asc
# Tue, 23 May 2023 07:50:10 GMT
ENV PHP_SHA256=5e07278a1f315a67d36a676c01343ca2d4da5ec5bdb15d018e4248b3012bc0cd
# Tue, 23 May 2023 07:50:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 23 May 2023 07:50:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 23 May 2023 07:58:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 23 May 2023 07:58:36 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 23 May 2023 07:58:36 GMT
RUN docker-php-ext-enable sodium
# Tue, 23 May 2023 07:58:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 23 May 2023 07:58:37 GMT
WORKDIR /var/www/html
# Tue, 23 May 2023 07:58:37 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 23 May 2023 07:58:37 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 May 2023 07:58:37 GMT
EXPOSE 9000
# Tue, 23 May 2023 07:58:37 GMT
CMD ["php-fpm"]
# Tue, 23 May 2023 13:23:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 13:23:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 24 May 2023 23:22:25 GMT
COPY file:24bf6e4ff958bf58ae126804a93affdbd6a0bf41615cc91af3f7538a88742dbd in /usr/local/bin/ 
# Wed, 24 May 2023 23:22:25 GMT
ENV DRUPAL_VERSION=9.5.9
# Wed, 24 May 2023 23:22:25 GMT
WORKDIR /opt/drupal
# Wed, 24 May 2023 23:23:02 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Wed, 24 May 2023 23:23:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0265ca860f8350954d0667b45b48728e992970f63232c58e18fac59852acd8f2`  
		Last Modified: Tue, 23 May 2023 01:02:24 GMT  
		Size: 22.7 MB (22747412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f10be44c42d6f52275fb4bd6b7b823e71b5d1b0be9ea2185ea7bc5fc43d2e7`  
		Last Modified: Tue, 23 May 2023 08:05:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517eac767ab2d3e917293eebc32246985d11c0669208b3eb6f20b6e8762c734`  
		Last Modified: Tue, 23 May 2023 08:05:20 GMT  
		Size: 59.5 MB (59544070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4d3e7966887bf66ea9d17b8172aa32c6ce946bef167eba1bd57fb8a2f3093b`  
		Last Modified: Tue, 23 May 2023 08:05:10 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e71b3241d242a34d430f2faebdf00e6f085874445e63d85d218081022971ae`  
		Last Modified: Tue, 23 May 2023 08:10:44 GMT  
		Size: 11.1 MB (11122958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c9492b93cd9d245c8d1a232ef75be095823004bb9b1520825e2ef192773994`  
		Last Modified: Tue, 23 May 2023 08:10:44 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3066cb3e4d405e97fbabfc5fb384accde75d037d733d336af4b82532741a75c`  
		Last Modified: Tue, 23 May 2023 08:11:17 GMT  
		Size: 23.2 MB (23221979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae894812832d6648ba38542e1cebd634762408b0e3744f6e0cec6ce4402035b`  
		Last Modified: Tue, 23 May 2023 08:11:13 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c00db7360403797530c04b847749218fc6dab6ba15e1d23dbe24e9f5acf307e`  
		Last Modified: Tue, 23 May 2023 08:11:13 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09fc593dfc2bf5d697a091bcc5597f540822aaa8f81f8c3247a41b6137acb6dd`  
		Last Modified: Tue, 23 May 2023 08:11:13 GMT  
		Size: 8.7 KB (8720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ce104f3e140fddd508d49b26fafcdaa96fc86252f26c58402be83c0db3c981`  
		Last Modified: Tue, 23 May 2023 13:38:32 GMT  
		Size: 1.6 MB (1608702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40c6607dac5e6eabe9319c6edc3a6a6327ef1c87f41c29f4f347ec95be18c56`  
		Last Modified: Tue, 23 May 2023 13:38:31 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0381d2d8ae378d21bc5ab5203ae422b1062d1107946a56e8d38d6073c5aed971`  
		Last Modified: Wed, 24 May 2023 23:43:54 GMT  
		Size: 698.1 KB (698148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057455a2483a3a11d85b449dd16d182f2fd7b6f4adfc856546ae9cb86a35fa86`  
		Last Modified: Wed, 24 May 2023 23:43:53 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047274b8851b17f65ed54baee26a5c7c4de98e8768b616ca2c285b8dfec2cc99`  
		Last Modified: Wed, 24 May 2023 23:44:09 GMT  
		Size: 22.9 MB (22878309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-php8.0-fpm-buster` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:37f5b346d25f60e0eaaf84106edbe4ce00acfeebcf98ca267467209347734a15
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157784516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d805fd4eb60c591a8deb20c5b391d3fdb0be1173380bf81b9bd466c02b1ef18b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 May 2023 00:43:28 GMT
ADD file:55a469039df0bf0e94ef7cd2d6fd355ad0c69e0e23e7921194445dd1fe281e3b in / 
# Tue, 23 May 2023 00:43:28 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:23:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 May 2023 04:23:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 May 2023 04:23:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:23:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 May 2023 04:23:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 May 2023 04:23:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 04:23:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 04:23:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 May 2023 05:11:31 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Tue, 23 May 2023 05:11:31 GMT
ENV PHP_VERSION=8.0.28
# Tue, 23 May 2023 05:11:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.28.tar.xz.asc
# Tue, 23 May 2023 05:11:31 GMT
ENV PHP_SHA256=5e07278a1f315a67d36a676c01343ca2d4da5ec5bdb15d018e4248b3012bc0cd
# Tue, 23 May 2023 05:11:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 23 May 2023 05:11:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 23 May 2023 05:18:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 23 May 2023 05:18:16 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 23 May 2023 05:18:17 GMT
RUN docker-php-ext-enable sodium
# Tue, 23 May 2023 05:18:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 23 May 2023 05:18:17 GMT
WORKDIR /var/www/html
# Tue, 23 May 2023 05:18:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 23 May 2023 05:18:17 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 May 2023 05:18:17 GMT
EXPOSE 9000
# Tue, 23 May 2023 05:18:18 GMT
CMD ["php-fpm"]
# Tue, 23 May 2023 11:13:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 11:13:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 24 May 2023 23:19:18 GMT
COPY file:24bf6e4ff958bf58ae126804a93affdbd6a0bf41615cc91af3f7538a88742dbd in /usr/local/bin/ 
# Wed, 24 May 2023 23:19:18 GMT
ENV DRUPAL_VERSION=9.5.9
# Wed, 24 May 2023 23:19:18 GMT
WORKDIR /opt/drupal
# Wed, 24 May 2023 23:19:42 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Wed, 24 May 2023 23:19:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:3ca7b6c7180eac66b9c4301084a16319f41eb7f7365bdf91bcc272bd24cb4149`  
		Last Modified: Tue, 23 May 2023 00:46:44 GMT  
		Size: 25.9 MB (25921744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9b52276f9677dd50f8ec4feda3892eb7c995d3979af3d26a6b4c7a17c43f7e`  
		Last Modified: Tue, 23 May 2023 05:23:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18db47d2f311cb982b22e58c7c13d6a0951f563df1e87747319389823ee445c8`  
		Last Modified: Tue, 23 May 2023 05:23:50 GMT  
		Size: 70.4 MB (70366540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ff8177973c852a42f375db0f3bd2ab12cb0e13c0653f83691745524cb09cc6`  
		Last Modified: Tue, 23 May 2023 05:23:42 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918c11b523ca8c689d7c08ba3ca641b261680ed43b61707acdf81f25373930f6`  
		Last Modified: Tue, 23 May 2023 05:28:33 GMT  
		Size: 11.1 MB (11123727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ad03c7855c567c5aa6526b7d6a53df508e41f6710f33b3af41cb471a820764`  
		Last Modified: Tue, 23 May 2023 05:28:30 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b330c920b13e9d9068a30e94756a7e46562ba844303f596710303e73b1d72ec7`  
		Last Modified: Tue, 23 May 2023 05:28:59 GMT  
		Size: 24.9 MB (24906991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7048d31072657d52e6f328d661cf72130cf8ebbee2176471001fc03db0f905`  
		Last Modified: Tue, 23 May 2023 05:28:56 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51573bba803e95bb6acca36e2f92ba7e2d5bf9f2fa4fd8c1ea7ac9d65162a7ca`  
		Last Modified: Tue, 23 May 2023 05:28:56 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18663afda42dfe5e19efc291306aa81e02995ab65523abb60efb9e43306e178c`  
		Last Modified: Tue, 23 May 2023 05:28:56 GMT  
		Size: 8.7 KB (8717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591a760a6114f23c059b6701d7284a5f3376e830a9e11f4665ed83506cdc4ef4`  
		Last Modified: Tue, 23 May 2023 11:26:44 GMT  
		Size: 1.9 MB (1876025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a9385888aa4224380eb4ccb2a8ce6253d49637d8af38442f27a3ab8cfe8fc7`  
		Last Modified: Tue, 23 May 2023 11:26:43 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d194286189a12329ab04bd7da6d31938d4ca52ddf74000e2531949499994ce3`  
		Last Modified: Wed, 24 May 2023 23:35:56 GMT  
		Size: 698.1 KB (698147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d22965688c0270f3deb4d383186393160a0ee2dd7cea6aa18bf8897b5490de`  
		Last Modified: Wed, 24 May 2023 23:35:56 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b70b8c4bdee921954dfe7f2e540ca1e468a5a52e87cfc4bf22765ab60d374a`  
		Last Modified: Wed, 24 May 2023 23:36:00 GMT  
		Size: 22.9 MB (22878478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-php8.0-fpm-buster` - linux; 386

```console
$ docker pull drupal@sha256:8f798ca7afc70ad510da9f296c861ddcdbd368c6806e830d93003a6031ad06bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 MB (171959420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab8e749abbe14038f1cc4c7709937ddd97b6f7cf4acc49f3e55984b4c2c37f46`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 May 2023 00:40:01 GMT
ADD file:96715cff0e3569a2a1d7e203f0797ed4880da7714d455e25f032c67bff27221f in / 
# Tue, 23 May 2023 00:40:01 GMT
CMD ["bash"]
# Tue, 23 May 2023 12:59:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 May 2023 12:59:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 May 2023 13:00:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 13:00:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 May 2023 13:00:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 May 2023 13:00:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 13:00:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 13:00:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 May 2023 14:23:44 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Tue, 23 May 2023 14:23:45 GMT
ENV PHP_VERSION=8.0.28
# Tue, 23 May 2023 14:23:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.28.tar.xz.asc
# Tue, 23 May 2023 14:23:45 GMT
ENV PHP_SHA256=5e07278a1f315a67d36a676c01343ca2d4da5ec5bdb15d018e4248b3012bc0cd
# Tue, 23 May 2023 14:24:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 23 May 2023 14:24:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 23 May 2023 14:38:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 23 May 2023 14:38:55 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 23 May 2023 14:38:56 GMT
RUN docker-php-ext-enable sodium
# Tue, 23 May 2023 14:38:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 23 May 2023 14:38:56 GMT
WORKDIR /var/www/html
# Tue, 23 May 2023 14:38:57 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 23 May 2023 14:38:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 May 2023 14:38:57 GMT
EXPOSE 9000
# Tue, 23 May 2023 14:38:57 GMT
CMD ["php-fpm"]
# Tue, 23 May 2023 21:44:20 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 21:44:20 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 24 May 2023 23:04:54 GMT
COPY file:24bf6e4ff958bf58ae126804a93affdbd6a0bf41615cc91af3f7538a88742dbd in /usr/local/bin/ 
# Wed, 24 May 2023 23:04:54 GMT
ENV DRUPAL_VERSION=9.5.9
# Wed, 24 May 2023 23:04:55 GMT
WORKDIR /opt/drupal
# Wed, 24 May 2023 23:05:11 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Wed, 24 May 2023 23:05:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:3c2058520f8e2dee0c8d97a0e68335849888066e5d0d1b82b6ef302541b5c874`  
		Last Modified: Tue, 23 May 2023 00:45:13 GMT  
		Size: 27.8 MB (27797210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1266a4baadae5ef59725941c991dc5adfa2ed13e7cf3fdd85cc6f709265af87`  
		Last Modified: Tue, 23 May 2023 14:48:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e7447771f969594fe1e4ee64c72e57aa11c42c64255e08710ee80d2b15547d8`  
		Last Modified: Tue, 23 May 2023 14:48:21 GMT  
		Size: 81.2 MB (81239303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c108971a278f401b281b6f0afe922e69a4d522140c9166362e30c6967a76bde6`  
		Last Modified: Tue, 23 May 2023 14:48:03 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242df86d0f2b300ce82c468d02f8aa63da895724c3d9ed61546de2be355e0c4a`  
		Last Modified: Tue, 23 May 2023 14:54:07 GMT  
		Size: 11.1 MB (11124294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bc9adb6b3e8cfca9317f49a72568bf128022618a911cc7cc0b944254a92425`  
		Last Modified: Tue, 23 May 2023 14:54:05 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd1d80ec7ead71cbad8cc2a67da43c53e30d8c452fe1f6088e2ff88ec378932`  
		Last Modified: Tue, 23 May 2023 14:54:46 GMT  
		Size: 25.9 MB (25916630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17dbb36724b55a29fc44b1636ca36b48d95edfd0ed117626e19e95464d13d8b1`  
		Last Modified: Tue, 23 May 2023 14:54:40 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812802b192afe32d504c837604f3f1c0fe06bc7950b34b2ce8302d6c66d17c77`  
		Last Modified: Tue, 23 May 2023 14:54:40 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87192fd00f381af22af0ffe4b86829d903bc00e4780de12a0d34210c2a34392`  
		Last Modified: Tue, 23 May 2023 14:54:40 GMT  
		Size: 8.7 KB (8715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28bcd8cfdc4b2fd7a35164762f5de50d4caccf74a09b255cb93290054043e21`  
		Last Modified: Tue, 23 May 2023 21:58:42 GMT  
		Size: 2.3 MB (2292453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a12f52921fcdb789838be55a981bd39eba438dcc172e4c63e932468f8a0496`  
		Last Modified: Tue, 23 May 2023 21:58:41 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff6242fd4c81f593332f50bf0357498e7e347cb00f797174e21687a4af8437c`  
		Last Modified: Wed, 24 May 2023 23:24:04 GMT  
		Size: 698.1 KB (698150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37cbeaffdf3caeb54f402d4ab47223b23d895e0a928be8b296d379afc5e59448`  
		Last Modified: Wed, 24 May 2023 23:24:04 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ddafb2060b7cbeeaa2ac60d3fecb724bffbcde844801d49493c7688c34ba620`  
		Last Modified: Wed, 24 May 2023 23:24:11 GMT  
		Size: 22.9 MB (22878521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
