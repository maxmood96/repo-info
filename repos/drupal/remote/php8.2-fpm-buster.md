## `drupal:php8.2-fpm-buster`

```console
$ docker pull drupal@sha256:51531426a0c87d2d03b3ade85023bef8106cf1345e741636c6f70938e85b2402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `drupal:php8.2-fpm-buster` - linux; amd64

```console
$ docker pull drupal@sha256:1c9e759046604185032c32b875a03cb10a06584254ce00a7fa0df3414a184539
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162522895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d17030e1919e5208ad77cfa98d3404c3277834903b205f33443a83bdcddfc2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 04 Feb 2023 06:52:07 GMT
ADD file:4fbe1e3712cf37c85529cc81e0d03c82085203de00d64b0d669b5996e975925a in / 
# Sat, 04 Feb 2023 06:52:07 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 18:47:46 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 04 Feb 2023 18:47:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 04 Feb 2023 18:48:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 18:48:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 04 Feb 2023 18:48:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 04 Feb 2023 18:48:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 04 Feb 2023 18:48:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 04 Feb 2023 18:48:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 04 Feb 2023 18:48:05 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 04 Feb 2023 18:48:06 GMT
ENV PHP_VERSION=8.2.2
# Sat, 04 Feb 2023 18:48:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.2.tar.xz.asc
# Sat, 04 Feb 2023 18:48:06 GMT
ENV PHP_SHA256=bdc4aa38e652bac86039601840bae01c0c3653972eaa6f9f93d5f71953a7ee33
# Sat, 04 Feb 2023 18:48:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 04 Feb 2023 18:48:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 04 Feb 2023 18:58:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 04 Feb 2023 18:58:16 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 04 Feb 2023 18:58:16 GMT
RUN docker-php-ext-enable sodium
# Sat, 04 Feb 2023 18:58:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 04 Feb 2023 18:58:17 GMT
WORKDIR /var/www/html
# Sat, 04 Feb 2023 18:58:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 04 Feb 2023 18:58:17 GMT
STOPSIGNAL SIGQUIT
# Sat, 04 Feb 2023 18:58:17 GMT
EXPOSE 9000
# Sat, 04 Feb 2023 18:58:17 GMT
CMD ["php-fpm"]
# Sun, 05 Feb 2023 02:28:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sun, 05 Feb 2023 02:28:57 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sun, 05 Feb 2023 02:28:57 GMT
COPY file:81cad59228e2dc61b9d880277f60e1ab16f4d7a32f9f11b33c68bd0b2bacdc3a in /usr/local/bin/ 
# Sun, 05 Feb 2023 02:28:57 GMT
ENV DRUPAL_VERSION=10.0.3
# Sun, 05 Feb 2023 02:28:57 GMT
WORKDIR /opt/drupal
# Sun, 05 Feb 2023 02:29:07 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Sun, 05 Feb 2023 02:29:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0cf508b37688dca559387b506062329202aaf08b48be5f55f9278b2a818ad2c9`  
		Last Modified: Sat, 04 Feb 2023 06:56:58 GMT  
		Size: 27.1 MB (27140353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae08958ff1bd1856a03e2bfbae52b79c27be0d2f80bf155c8aa532f9ad46e220`  
		Last Modified: Sat, 04 Feb 2023 19:58:50 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db284214e0a94216b2a47f1bf6f9a9adf6209c7b73a59ea110027e2cb6e54469`  
		Last Modified: Sat, 04 Feb 2023 19:59:01 GMT  
		Size: 76.7 MB (76688297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881a1d9f7f864087aced46e16f6fb5f479692c06e9f75bc2b4b6f6af074a402d`  
		Last Modified: Sat, 04 Feb 2023 19:58:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b47d4d5e9c5d16445db617eb3cf25c1cbeac8792ac23e794baac9b8ab149693`  
		Last Modified: Sat, 04 Feb 2023 19:58:49 GMT  
		Size: 12.3 MB (12259317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b836977855b75f49e32ad1814517642cc83bf0f9bbbf89c1f1af47463c45cff`  
		Last Modified: Sat, 04 Feb 2023 19:58:48 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e55e563cbc86f6c289adbdccd7a1229e7efcd0380accabf527aa596152d63c`  
		Last Modified: Sat, 04 Feb 2023 19:59:45 GMT  
		Size: 26.0 MB (26001219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aea8986c19e17313983e89d57e0aa46b016641d5d286e23bc7461e86f593a96`  
		Last Modified: Sat, 04 Feb 2023 19:59:41 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8dae7411c0e3c6da6003db471b0966acf8cba2e9012afe7ac29a961ed75161`  
		Last Modified: Sat, 04 Feb 2023 19:59:41 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cbe35776e89462e5bde6dcd20e91efccd392aeaaa20bbff1f835758dc8a61f`  
		Last Modified: Sat, 04 Feb 2023 19:59:41 GMT  
		Size: 9.2 KB (9150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930aca14e66c7d4b31f66b0faa29d93482ff94d44be47905ef1b3817eb3d862b`  
		Last Modified: Sun, 05 Feb 2023 02:49:38 GMT  
		Size: 2.1 MB (2065728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8cb6d4fe3a37d6861c7239701297b015eefdaeb6e7cbe2c3e31b0754050239`  
		Last Modified: Sun, 05 Feb 2023 02:49:37 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca89604e5dcd693ae138ebdecad9d064a42959334fec4f3be384b3d6594d88d`  
		Last Modified: Sun, 05 Feb 2023 02:49:38 GMT  
		Size: 700.1 KB (700098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d850d60b6bc8b176e7364d7273178dc47b0eb2e9cd6b8d6fc03a00419a362d51`  
		Last Modified: Sun, 05 Feb 2023 02:49:37 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805dce356d5daac09fc6bcbc6ff2147f05795dff7667b06536eaa10de5492a76`  
		Last Modified: Sun, 05 Feb 2023 02:49:42 GMT  
		Size: 17.7 MB (17654579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:php8.2-fpm-buster` - linux; arm variant v7

```console
$ docker pull drupal@sha256:4d688e39d295ecaa9090aee5a049feceb97a4a4cda4224eccbb1feabe5b1e9f3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138091923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:625d047beea538a1ce6fedbd6d3c3ee2a08d04e188f2aa9e28f2b16f18461722`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 04 Feb 2023 10:00:07 GMT
ADD file:846a879e62f9818b9aa015fa10169114de528e64d1a704cdcd1e7ee2b0707dac in / 
# Sat, 04 Feb 2023 10:00:07 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 17:45:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 04 Feb 2023 17:45:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 04 Feb 2023 17:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:45:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 04 Feb 2023 17:45:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 04 Feb 2023 17:45:37 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 04 Feb 2023 17:45:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 04 Feb 2023 17:45:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 04 Feb 2023 17:45:37 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 04 Feb 2023 17:45:37 GMT
ENV PHP_VERSION=8.2.2
# Sat, 04 Feb 2023 17:45:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.2.tar.xz.asc
# Sat, 04 Feb 2023 17:45:37 GMT
ENV PHP_SHA256=bdc4aa38e652bac86039601840bae01c0c3653972eaa6f9f93d5f71953a7ee33
# Sat, 04 Feb 2023 17:45:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 04 Feb 2023 17:45:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 04 Feb 2023 17:54:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 04 Feb 2023 17:54:06 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 04 Feb 2023 17:54:06 GMT
RUN docker-php-ext-enable sodium
# Sat, 04 Feb 2023 17:54:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 04 Feb 2023 17:54:07 GMT
WORKDIR /var/www/html
# Sat, 04 Feb 2023 17:54:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 04 Feb 2023 17:54:07 GMT
STOPSIGNAL SIGQUIT
# Sat, 04 Feb 2023 17:54:07 GMT
EXPOSE 9000
# Sat, 04 Feb 2023 17:54:07 GMT
CMD ["php-fpm"]
# Sun, 05 Feb 2023 08:50:48 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sun, 05 Feb 2023 08:50:48 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sun, 05 Feb 2023 08:50:48 GMT
COPY file:81cad59228e2dc61b9d880277f60e1ab16f4d7a32f9f11b33c68bd0b2bacdc3a in /usr/local/bin/ 
# Sun, 05 Feb 2023 08:50:49 GMT
ENV DRUPAL_VERSION=10.0.3
# Sun, 05 Feb 2023 08:50:49 GMT
WORKDIR /opt/drupal
# Sun, 05 Feb 2023 08:51:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Sun, 05 Feb 2023 08:51:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8f31db5a63e959a9d015a334241216fa6923a49f0bc031bde1bf336efc7a9614`  
		Last Modified: Sat, 04 Feb 2023 10:07:17 GMT  
		Size: 22.7 MB (22748916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd9c5e07ad6aabb7f2d5afcd2bd672f5ce044d8d8232c1d426c6ee304bd8089`  
		Last Modified: Sat, 04 Feb 2023 18:52:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376b0a5b355348b427e4584aa60883dc7f2c8028164154ecc5d6a971e08c2b63`  
		Last Modified: Sat, 04 Feb 2023 18:52:15 GMT  
		Size: 59.5 MB (59541437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535c3c3ca3201e7c8dd97d901114d29bfd620670e80e44af5595ad010f61f766`  
		Last Modified: Sat, 04 Feb 2023 18:52:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb25e4ef307afe04d7d58c6d385e82a5015b0c9051d4f24b49e680a6dcfb0b08`  
		Last Modified: Sat, 04 Feb 2023 18:52:04 GMT  
		Size: 12.3 MB (12257578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934da7077a09770bd5346ed014c670f2ff12f85c341fe7e3c987e7bcc8ff7e86`  
		Last Modified: Sat, 04 Feb 2023 18:52:03 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e061d5a7ccc043c6e4bafd418cd7a9444c9a8b69a382a917eaa5a5e51f9f80`  
		Last Modified: Sat, 04 Feb 2023 18:53:15 GMT  
		Size: 23.7 MB (23707798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806674adc2181e14d69b978c2e14b3937666277fb976afb60900233c923bd129`  
		Last Modified: Sat, 04 Feb 2023 18:53:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4757db830002ca2c24af3a56f907af31d82102f7e8a2915fa74f7c72ecec09`  
		Last Modified: Sat, 04 Feb 2023 18:53:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430c8532ffac7d1067bd1d8f37e446cb6f270d0a39983ced0f8ab7dada781dbc`  
		Last Modified: Sat, 04 Feb 2023 18:53:11 GMT  
		Size: 9.2 KB (9151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df14e0a4d6e83f60e2fd69e6e9b323df2824c0ee7632f39331dd34b1283ad5c9`  
		Last Modified: Sun, 05 Feb 2023 09:23:15 GMT  
		Size: 1.5 MB (1465896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d133187fbf62afa3537e22d07cee4d7ead99790ab2594e6409b5cb12ecf4c503`  
		Last Modified: Sun, 05 Feb 2023 09:23:14 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ad692069aaf445e3c465f01f441a015fae07ba3ab04b9a9a3b64c43ee8f0f4`  
		Last Modified: Sun, 05 Feb 2023 09:23:15 GMT  
		Size: 700.1 KB (700097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45b7f07e39555ab3e1e035276d15a915035457c4423bab880a2bac5fc5dc7f6`  
		Last Modified: Sun, 05 Feb 2023 09:23:14 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b84763455db58e638739eac521638c17d8ca4ad7de4d98fada91ab589f906a`  
		Last Modified: Sun, 05 Feb 2023 09:23:21 GMT  
		Size: 17.7 MB (17656980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:php8.2-fpm-buster` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:60f61047693d477caa291b2aba0197c77626eb20ffac20a4ce4a582e14271ed4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155300664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193e037a5431b3d20830df6e3fba47535baaef414fe6664159fb608aa88ba603`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:54 GMT
ADD file:cf6ecb1d6b034b0d4fc309542cb25fff0c997661b323f524ecc258ac323e43f6 in / 
# Sat, 04 Feb 2023 06:17:55 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 12:18:58 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 04 Feb 2023 12:18:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 04 Feb 2023 12:19:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 12:19:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 04 Feb 2023 12:19:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 04 Feb 2023 12:19:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 04 Feb 2023 12:19:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 04 Feb 2023 12:19:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 04 Feb 2023 12:19:17 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 04 Feb 2023 12:19:17 GMT
ENV PHP_VERSION=8.2.2
# Sat, 04 Feb 2023 12:19:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.2.tar.xz.asc
# Sat, 04 Feb 2023 12:19:17 GMT
ENV PHP_SHA256=bdc4aa38e652bac86039601840bae01c0c3653972eaa6f9f93d5f71953a7ee33
# Sat, 04 Feb 2023 12:19:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 04 Feb 2023 12:19:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 04 Feb 2023 12:28:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 04 Feb 2023 12:28:28 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 04 Feb 2023 12:28:28 GMT
RUN docker-php-ext-enable sodium
# Sat, 04 Feb 2023 12:28:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 04 Feb 2023 12:28:29 GMT
WORKDIR /var/www/html
# Sat, 04 Feb 2023 12:28:29 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 04 Feb 2023 12:28:29 GMT
STOPSIGNAL SIGQUIT
# Sat, 04 Feb 2023 12:28:29 GMT
EXPOSE 9000
# Sat, 04 Feb 2023 12:28:29 GMT
CMD ["php-fpm"]
# Sat, 04 Feb 2023 22:11:23 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 22:11:23 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 04 Feb 2023 22:11:23 GMT
COPY file:81cad59228e2dc61b9d880277f60e1ab16f4d7a32f9f11b33c68bd0b2bacdc3a in /usr/local/bin/ 
# Sat, 04 Feb 2023 22:11:24 GMT
ENV DRUPAL_VERSION=10.0.3
# Sat, 04 Feb 2023 22:11:24 GMT
WORKDIR /opt/drupal
# Sat, 04 Feb 2023 22:11:43 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Sat, 04 Feb 2023 22:11:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:bd2853c1424a5596deda2f31e1f82920613a03c667c3ff58cb461340b7bb89cd`  
		Last Modified: Sat, 04 Feb 2023 06:22:04 GMT  
		Size: 25.9 MB (25922631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78a59b8ccf3c868a96ffe9151ff3a1f1a89fee4d0151785e9080a02e8767c46`  
		Last Modified: Sat, 04 Feb 2023 13:18:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c974607a8d0be8f9cd77efc0f50a9b22ac01baef575c035f7e8f6cef7654dd`  
		Last Modified: Sat, 04 Feb 2023 13:19:00 GMT  
		Size: 70.4 MB (70361880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dae2c40cdca83210ffd87d10080044d2271241f03f6ca418351c27703acbeb`  
		Last Modified: Sat, 04 Feb 2023 13:18:51 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a7878fafcb27812168fe4c6afa3531f610bf494d48a2c03c2975e517b8e8c6`  
		Last Modified: Sat, 04 Feb 2023 13:18:50 GMT  
		Size: 12.3 MB (12258218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cd0ff7842441660aa9b0422eb4fba3efe5398411e86fc6c645e8b38792e091`  
		Last Modified: Sat, 04 Feb 2023 13:18:50 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2db7fd0c7e330a16cf8bbf48a44ad1e8231d4229e8c65070eeedb53095ee5fc`  
		Last Modified: Sat, 04 Feb 2023 13:19:43 GMT  
		Size: 26.1 MB (26054444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53919c55c29f6924b8cd1a99a88fd1309da2e5b917b2386a7d07eb605f5d8b3`  
		Last Modified: Sat, 04 Feb 2023 13:19:40 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df40758e5635b0091502b644ae37cb7940f5cc82ae1ffda588bba41b72d2da2d`  
		Last Modified: Sat, 04 Feb 2023 13:19:40 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04ec242594305a498016eaae3986e6fe339e3ad0410d70c6c5214e01c37d7ee`  
		Last Modified: Sat, 04 Feb 2023 13:19:40 GMT  
		Size: 9.1 KB (9149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd16ad0567fd7feb20a50a4597291c1656082a3d4c80fbb313a24fdb16cf6758`  
		Last Modified: Sat, 04 Feb 2023 22:33:49 GMT  
		Size: 2.3 MB (2333688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844b2c44a454dd18839544249885fd62b2840c6385400d9e4b5c491f7fd765f9`  
		Last Modified: Sat, 04 Feb 2023 22:33:48 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139f43c513e418bfbf4870280178453832734b225f42ce113be159f9f1185f46`  
		Last Modified: Sat, 04 Feb 2023 22:33:49 GMT  
		Size: 700.1 KB (700097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd486eebfb2ad3bbf4d53e82e533266cf2c142532b50538c324a7d04e74dd8b`  
		Last Modified: Sat, 04 Feb 2023 22:33:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a891376f32d11481155bbe6604a0c55f226bcfa30f0770bfb1046a0e9b1bf8`  
		Last Modified: Sat, 04 Feb 2023 22:33:52 GMT  
		Size: 17.7 MB (17656406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:php8.2-fpm-buster` - linux; 386

```console
$ docker pull drupal@sha256:ee336ff299e4433fb8ce66f427ce77f42f358ff22eeae439476bb274010619fd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.6 MB (167639112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7214c74d9148038b8a534d42a69370d7414289715986cd21201aee728b70fe7f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 04 Feb 2023 07:49:48 GMT
ADD file:060bbacc8df3d1b157ff409535b3ea29dd0b5667425e3dcf6e60556dcfa4e7f1 in / 
# Sat, 04 Feb 2023 07:49:48 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 14:30:07 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 04 Feb 2023 14:30:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 04 Feb 2023 14:30:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 14:30:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 04 Feb 2023 14:30:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 04 Feb 2023 14:30:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 04 Feb 2023 14:30:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 04 Feb 2023 14:30:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 04 Feb 2023 14:30:33 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 04 Feb 2023 14:30:34 GMT
ENV PHP_VERSION=8.2.2
# Sat, 04 Feb 2023 14:30:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.2.tar.xz.asc
# Sat, 04 Feb 2023 14:30:36 GMT
ENV PHP_SHA256=bdc4aa38e652bac86039601840bae01c0c3653972eaa6f9f93d5f71953a7ee33
# Sat, 04 Feb 2023 14:30:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 04 Feb 2023 14:30:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 04 Feb 2023 14:39:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 04 Feb 2023 14:39:57 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 04 Feb 2023 14:39:57 GMT
RUN docker-php-ext-enable sodium
# Sat, 04 Feb 2023 14:39:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 04 Feb 2023 14:39:59 GMT
WORKDIR /var/www/html
# Sat, 04 Feb 2023 14:40:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 04 Feb 2023 14:40:01 GMT
STOPSIGNAL SIGQUIT
# Sat, 04 Feb 2023 14:40:02 GMT
EXPOSE 9000
# Sat, 04 Feb 2023 14:40:03 GMT
CMD ["php-fpm"]
# Sat, 04 Feb 2023 23:31:24 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 23:31:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 04 Feb 2023 23:31:27 GMT
COPY file:e2da1c2113094da76d330eef39e0e1916af11394dff778e02af557c116266d7c in /usr/local/bin/ 
# Sat, 04 Feb 2023 23:31:27 GMT
ENV DRUPAL_VERSION=10.0.3
# Sat, 04 Feb 2023 23:31:28 GMT
WORKDIR /opt/drupal
# Sat, 04 Feb 2023 23:31:42 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Sat, 04 Feb 2023 23:31:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8e0d975bedf8c90406704c677df48435cd2d53449ac9ab15a876323ceb95ff8f`  
		Last Modified: Sat, 04 Feb 2023 07:55:52 GMT  
		Size: 27.8 MB (27798503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7530cf666fff6e57c2fd7b789b76bf7b9512b00c5d78ed4d83019d31c306e105`  
		Last Modified: Sat, 04 Feb 2023 15:42:40 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bdb983fe81a5de6de33350ecbdd92cb52b3afb4f1d1d693c6384470024c6940`  
		Last Modified: Sat, 04 Feb 2023 15:42:51 GMT  
		Size: 81.2 MB (81235952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4035ed3a2e1d31e52d608036c5e463521bd61f242d5c91be4dd94cecd412b6d2`  
		Last Modified: Sat, 04 Feb 2023 15:42:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afec1e9267df5e6caf4bd4e9beb5ab7bc936221fcedd4ea568443bad73a6606`  
		Last Modified: Sat, 04 Feb 2023 15:42:40 GMT  
		Size: 12.0 MB (12045181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a605a5b3ccdd5c8758520ea6f71e4195fd7ad4208696bf6a1de9eb95c4e9b771`  
		Last Modified: Sat, 04 Feb 2023 15:42:38 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1039cfcddf73ff6b272ddd9c6801f89eabdabb8932c146f979934c81e0393e`  
		Last Modified: Sat, 04 Feb 2023 15:43:44 GMT  
		Size: 26.3 MB (26270354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a00c1273dfda21cc1bdc0d7f3eba51dcdf93071a67e9c8bbd4252f9cb21ceec`  
		Last Modified: Sat, 04 Feb 2023 15:43:40 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:defe4574600c0f27e1bb99e51f9c1d2c41ced4f66a9405e513c181b150fe4f58`  
		Last Modified: Sat, 04 Feb 2023 15:43:40 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ddb04d39db18fb09175e846e67902e23ac0f5c0068858540c5c7b18721bc11`  
		Last Modified: Sat, 04 Feb 2023 15:43:40 GMT  
		Size: 9.2 KB (9158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30891a5df71e2c0138221e94f796a061a4548ec8bb4bf1b7d912c45386f9d2bb`  
		Last Modified: Sat, 04 Feb 2023 23:59:55 GMT  
		Size: 1.9 MB (1922009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6075c906549c1d2cbf831864aa7c6820f23e6a2a93744868d147c0e4ef1f58bc`  
		Last Modified: Sat, 04 Feb 2023 23:59:55 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6702b8ad38f60db112681de9410aa2bff0e710c56f3b9b7a361c9923f324563f`  
		Last Modified: Sat, 04 Feb 2023 23:59:55 GMT  
		Size: 695.2 KB (695203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83378b4a292ac9b13403bf007b27ece9b6df545705a30aefe1d1ea3dc97ecfd4`  
		Last Modified: Sat, 04 Feb 2023 23:59:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa793e784ae8c0a078b69d0c37872e74c0ba34da80dfebb485953c7d6620bdc`  
		Last Modified: Sat, 04 Feb 2023 23:59:59 GMT  
		Size: 17.7 MB (17658682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
