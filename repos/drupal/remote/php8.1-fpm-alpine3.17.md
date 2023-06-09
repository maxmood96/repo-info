## `drupal:php8.1-fpm-alpine3.17`

```console
$ docker pull drupal@sha256:6e3fd6d3650db6027e2736800e62abe0a0562a51cf17278c0f8e6e06f5378084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `drupal:php8.1-fpm-alpine3.17` - linux; amd64

```console
$ docker pull drupal@sha256:de92b544f18d71cf592357833f2f1ca2d1c819b3104185a48d5922f36ac91c47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53014158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e01d786497a5e665e9545f2979decdf838099d174a9bca361d3375dcdbef387`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:40:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 Mar 2023 22:40:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 29 Mar 2023 22:40:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 Mar 2023 22:40:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 Mar 2023 22:40:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 Mar 2023 22:40:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 22:40:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 22:40:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 29 Mar 2023 23:04:33 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 09 Jun 2023 01:36:48 GMT
ENV PHP_VERSION=8.1.20
# Fri, 09 Jun 2023 01:36:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Fri, 09 Jun 2023 01:36:49 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Fri, 09 Jun 2023 01:36:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 09 Jun 2023 01:36:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:44:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 09 Jun 2023 01:44:14 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:44:15 GMT
RUN docker-php-ext-enable sodium
# Fri, 09 Jun 2023 01:44:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jun 2023 01:44:16 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 01:44:16 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 09 Jun 2023 01:44:16 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jun 2023 01:44:16 GMT
EXPOSE 9000
# Fri, 09 Jun 2023 01:44:16 GMT
CMD ["php-fpm"]
# Fri, 09 Jun 2023 03:28:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Fri, 09 Jun 2023 03:28:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 09 Jun 2023 03:28:59 GMT
COPY file:24bf6e4ff958bf58ae126804a93affdbd6a0bf41615cc91af3f7538a88742dbd in /usr/local/bin/ 
# Fri, 09 Jun 2023 03:28:59 GMT
ENV DRUPAL_VERSION=10.0.9
# Fri, 09 Jun 2023 03:28:59 GMT
WORKDIR /opt/drupal
# Fri, 09 Jun 2023 03:29:09 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Fri, 09 Jun 2023 03:29:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace8de9a4ff59932f451431025d83ed30afbc238a70e7fe837fa9757cec1c74d`  
		Last Modified: Wed, 29 Mar 2023 23:41:17 GMT  
		Size: 1.9 MB (1878588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac818333da4c37131af0fcde8f101e32f12115ea27e4b3c6c4dcc1676246b26e`  
		Last Modified: Wed, 29 Mar 2023 23:41:17 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f4138fad9a5a8dc17fe4d773b9349c86bca1a73913fc2e722dd49114f6e485`  
		Last Modified: Wed, 29 Mar 2023 23:41:17 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dcd20eaa36c477b0eca18f7f00cfb7789d392be7c7c30bc4ac93e257689e20a`  
		Last Modified: Fri, 09 Jun 2023 02:51:49 GMT  
		Size: 11.8 MB (11813647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554f2942d46dc9578d4a4d313a2ee01fdd2911fb4ace6fe73a5ccf4d226ae28d`  
		Last Modified: Fri, 09 Jun 2023 02:51:48 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8d3d20c1f254a44056c374bc995020b65c77382e36b3a654ded2c6a100fa01`  
		Last Modified: Fri, 09 Jun 2023 02:52:06 GMT  
		Size: 15.3 MB (15334919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83ceea59c78e3387a4621273674df0fd76efcb00d3cdde2d82b5f4d7714f863`  
		Last Modified: Fri, 09 Jun 2023 02:52:04 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f93466ca74d207f25c98a0607ce9e394a26b278796e2e949c9e830f70fa46c8`  
		Last Modified: Fri, 09 Jun 2023 02:52:04 GMT  
		Size: 19.1 KB (19110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb4f3681562dcf03c1a6e100bc47aed90e68cf1be1c6252eefd4acbef16ff84`  
		Last Modified: Fri, 09 Jun 2023 02:52:04 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace993afc38d0b74f47cce98eb9d03c88c851573e780d93c9aa25d9c68f41b5b`  
		Last Modified: Fri, 09 Jun 2023 03:47:52 GMT  
		Size: 2.2 MB (2205928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfaa597b2010546e25cfaf9118d9dcf9f2c34bc880475257304d1e83f31eca8`  
		Last Modified: Fri, 09 Jun 2023 03:47:51 GMT  
		Size: 312.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c325cccb104d3e490f398af65010e8d393d17d8f30cd2020595c901831c1e2a`  
		Last Modified: Fri, 09 Jun 2023 03:47:52 GMT  
		Size: 698.1 KB (698147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8960fac1e463bf258996a8d6a333d6706412c7e2dc5d44a401ef7f99bec10c78`  
		Last Modified: Fri, 09 Jun 2023 03:47:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcf9bf217388c5e44dc629d5834a6243e29fe2cd017033e6b60e989d49ae5dc`  
		Last Modified: Fri, 09 Jun 2023 03:47:55 GMT  
		Size: 17.7 MB (17675446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:php8.1-fpm-alpine3.17` - linux; arm variant v6

```console
$ docker pull drupal@sha256:d56b0dc9a39e1c4f05f526c5091f7f5765f63225b4d7d69d9b1b33c022a357d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50681273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971d777644d7240e731e435d915d5cfc3c7ceb0529195c791a3a080d460a8d1f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:09 GMT
ADD file:2dd294d20c0b500c8fed6b410b059429b36f51cd48a45eaf7a06ecbef9e2a3bb in / 
# Wed, 29 Mar 2023 18:01:09 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 20:31:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 Mar 2023 20:31:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 29 Mar 2023 20:31:15 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 Mar 2023 20:31:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 Mar 2023 20:31:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 Mar 2023 20:31:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 20:31:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 20:31:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 29 Mar 2023 20:56:09 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 09 Jun 2023 00:51:37 GMT
ENV PHP_VERSION=8.1.20
# Fri, 09 Jun 2023 00:51:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Fri, 09 Jun 2023 00:51:37 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Fri, 09 Jun 2023 00:51:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 09 Jun 2023 00:51:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:00:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 09 Jun 2023 01:00:06 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:00:08 GMT
RUN docker-php-ext-enable sodium
# Fri, 09 Jun 2023 01:00:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jun 2023 01:00:08 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 01:00:08 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 09 Jun 2023 01:00:09 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jun 2023 01:00:09 GMT
EXPOSE 9000
# Fri, 09 Jun 2023 01:00:09 GMT
CMD ["php-fpm"]
# Fri, 09 Jun 2023 02:03:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Fri, 09 Jun 2023 02:03:09 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 09 Jun 2023 02:03:10 GMT
COPY file:24bf6e4ff958bf58ae126804a93affdbd6a0bf41615cc91af3f7538a88742dbd in /usr/local/bin/ 
# Fri, 09 Jun 2023 02:03:10 GMT
ENV DRUPAL_VERSION=10.0.9
# Fri, 09 Jun 2023 02:03:10 GMT
WORKDIR /opt/drupal
# Fri, 09 Jun 2023 02:03:22 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Fri, 09 Jun 2023 02:03:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:75257e753735e4ff78fae2d44018022a6ac775290e02103713a70699ece7576e`  
		Last Modified: Wed, 29 Mar 2023 18:01:52 GMT  
		Size: 3.1 MB (3110802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbc0647f6aa0b25292f3d768c2428684069b2a7af956dda6deec101e995fadb`  
		Last Modified: Tue, 04 Apr 2023 00:26:38 GMT  
		Size: 1.9 MB (1866057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b777c5831fd5d0def544973f7e00ee4632654243976be255164e5b719fdf8c`  
		Last Modified: Tue, 04 Apr 2023 00:26:37 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab9b5113557063a83a3b51f7c2b7755340a1c3a0a2749d54234afb4a1a79513`  
		Last Modified: Tue, 04 Apr 2023 00:26:37 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:836343c4e8cebd5661df4fdeb1e9cd9a30128f2969d3654531eb330a010e6e7f`  
		Last Modified: Fri, 09 Jun 2023 01:37:31 GMT  
		Size: 11.8 MB (11813639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfdc12bc91098adb42e88b315375c49e74034d6bee12a3658d6e8de3338bdae2`  
		Last Modified: Fri, 09 Jun 2023 01:37:30 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8403bac432baf7457707710427b28b6304a42ad688ec74c4accf82c4e11774`  
		Last Modified: Fri, 09 Jun 2023 01:37:50 GMT  
		Size: 13.8 MB (13816686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a316519c7f26bd8173109b246d6b151c7385da59fefa4c8a969d83f3915217cc`  
		Last Modified: Fri, 09 Jun 2023 01:37:48 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcf56ae021f447bd11894147f0b4d379d2c2d4a33faf50f4f1cf62de95f309f`  
		Last Modified: Fri, 09 Jun 2023 01:37:48 GMT  
		Size: 18.9 KB (18865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa389a1e2f3ce1eff177a0525f463a6a52f2d9b3613581d0496630d547bf9bd9`  
		Last Modified: Fri, 09 Jun 2023 01:37:48 GMT  
		Size: 8.9 KB (8879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268b2bf68038ad7e9ebe3dd93b88965a1dddd1a1620de2076af7b79087ae92e4`  
		Last Modified: Fri, 09 Jun 2023 02:08:46 GMT  
		Size: 1.7 MB (1667919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239f7c7df72fd1c0d1906bd47b9e617bd61607d9e91f58af39782a1f01d287ed`  
		Last Modified: Fri, 09 Jun 2023 02:08:45 GMT  
		Size: 312.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65acc4cf45c3a1c5898495554763de73972dc227afabb370bdbb0f5d2df30da1`  
		Last Modified: Fri, 09 Jun 2023 02:08:46 GMT  
		Size: 698.1 KB (698148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df41f2c4d366363ac6b62b228aa3e1d0b7c9242a0b332ff76069ce864ab912d`  
		Last Modified: Fri, 09 Jun 2023 02:08:45 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542a03009abb23e8c91c9ac560f4ad0059916d151d352e65692eb69d6118cc4a`  
		Last Modified: Fri, 09 Jun 2023 02:08:52 GMT  
		Size: 17.7 MB (17675344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:php8.1-fpm-alpine3.17` - linux; arm variant v7

```console
$ docker pull drupal@sha256:370e4582a73b38f4887a41cb062d1b33a18214e52db00237332100a1b50811fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48960513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9659795481e7c0f8d87982cfcfff3c0e288c969111bd4c6286b974b688b5d0a3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 29 Mar 2023 18:03:38 GMT
ADD file:959fa0ffb60c37c4fdc0d32ac31511f8dead32ef7f4bd848b11ff144a6b37012 in / 
# Wed, 29 Mar 2023 18:03:38 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:56:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 Mar 2023 22:56:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 29 Mar 2023 22:56:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 Mar 2023 22:56:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 Mar 2023 22:56:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 Mar 2023 22:56:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 22:56:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 22:56:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 29 Mar 2023 23:23:34 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 13 May 2023 01:03:51 GMT
ENV PHP_VERSION=8.1.19
# Sat, 13 May 2023 01:03:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.19.tar.xz.asc
# Sat, 13 May 2023 01:03:52 GMT
ENV PHP_SHA256=f42f0e93467415b2d30aa5b7ac825f0079a74207e0033010383cdc1e13657379
# Sat, 13 May 2023 01:04:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 13 May 2023 01:04:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 13 May 2023 01:11:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 13 May 2023 01:11:16 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 13 May 2023 01:11:18 GMT
RUN docker-php-ext-enable sodium
# Sat, 13 May 2023 01:11:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 13 May 2023 01:11:18 GMT
WORKDIR /var/www/html
# Sat, 13 May 2023 01:11:18 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 13 May 2023 01:11:18 GMT
STOPSIGNAL SIGQUIT
# Sat, 13 May 2023 01:11:19 GMT
EXPOSE 9000
# Sat, 13 May 2023 01:11:19 GMT
CMD ["php-fpm"]
# Sat, 13 May 2023 01:52:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 13 May 2023 01:52:10 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 24 May 2023 23:18:46 GMT
COPY file:24bf6e4ff958bf58ae126804a93affdbd6a0bf41615cc91af3f7538a88742dbd in /usr/local/bin/ 
# Wed, 24 May 2023 23:18:46 GMT
ENV DRUPAL_VERSION=10.0.9
# Wed, 24 May 2023 23:18:46 GMT
WORKDIR /opt/drupal
# Wed, 24 May 2023 23:18:57 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Wed, 24 May 2023 23:18:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:fd4b2aeb476b6c2c0c3049dae919de20fe09e90deac95e3181d717055cbe6707`  
		Last Modified: Wed, 29 Mar 2023 18:06:56 GMT  
		Size: 2.9 MB (2868519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d801477645c6152bedd176a48dd4cd43848b4628df963f29190ca396a08cda1b`  
		Last Modified: Fri, 31 Mar 2023 23:09:11 GMT  
		Size: 1.7 MB (1715928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bf14e8ce70e4d5b9dc80eefdce167d1b7c565c34eace0f6282428b4ed6ac44`  
		Last Modified: Fri, 31 Mar 2023 23:09:10 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba08b30181e8a0fd2e9555d9f184958e0cf2b0ac3ad5d11f50dc8a534fd0208`  
		Last Modified: Fri, 31 Mar 2023 23:09:10 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8471c92ac58c30b3a8a00ddc314314ac2a47061dccd25f06cbab510da666759`  
		Last Modified: Sat, 13 May 2023 01:19:26 GMT  
		Size: 11.9 MB (11867548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3aebe05b546e43fab3fd020dfe48d45ade39b6565c4b526610a4d93024b42c`  
		Last Modified: Sat, 13 May 2023 01:19:25 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e79905213d66197904f104de62d2462bea437fb925a1310841747b0e49c20ae`  
		Last Modified: Sat, 13 May 2023 01:19:43 GMT  
		Size: 12.6 MB (12565534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba9dd52bbc5db1051b9a8db6bcde95e2dbbbdb27c996f7d3b71dbdccc286a82`  
		Last Modified: Sat, 13 May 2023 01:19:41 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae657d7184e86a8e36eeaf37dddd26f7026e25b9d38fe961bc2672182ae8f720`  
		Last Modified: Sat, 13 May 2023 01:19:41 GMT  
		Size: 18.8 KB (18843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997d1ceaf95a15f3d5cd54ba1238832288ac32c8b79ebeb974e82d64f9645127`  
		Last Modified: Sat, 13 May 2023 01:19:41 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2359ea94a33f1775b41f8ea77b7260ed7b153754a02bc3484e0ab7091629baaf`  
		Last Modified: Sat, 13 May 2023 02:00:24 GMT  
		Size: 1.5 MB (1536817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9474afcbf63c87b7816633d231a83e47322fac1cde8964d40d6c855fa521ac2`  
		Last Modified: Sat, 13 May 2023 02:00:23 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8040711e1b98fa890fbc3a44ce9101e63f5f83e04b1ccd60a37d445a9879795d`  
		Last Modified: Wed, 24 May 2023 23:37:16 GMT  
		Size: 698.1 KB (698149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd38a120705e80e6615cd4e9d04149df691e46eb8ce45fc528876ed7c3aa5d27`  
		Last Modified: Wed, 24 May 2023 23:37:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0933ff4191fb3eac70d0483675da68c61ae49b766226b365dcb851fe47b961fa`  
		Last Modified: Wed, 24 May 2023 23:37:29 GMT  
		Size: 17.7 MB (17675359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:php8.1-fpm-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:4e1869ee4f4c20daaf08f4acb2ecb4ffcf9ec3d43f0381cebd0674b3160873b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52991156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a08ab7e230bbd6ab8f5490f90b4ccc8692c3209a6a7bdf8c779c80e07b1ae34`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:18 GMT
ADD file:e51d4089e73ad6dee52b31f0c8059a00c17df6e23f6741fe11b43bd84cc99008 in / 
# Wed, 29 Mar 2023 17:39:18 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 21:26:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 Mar 2023 21:26:02 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 29 Mar 2023 21:26:02 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 Mar 2023 21:26:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 Mar 2023 21:26:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 Mar 2023 21:26:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 21:26:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 21:26:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 29 Mar 2023 21:50:54 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 09 Jun 2023 02:03:00 GMT
ENV PHP_VERSION=8.1.20
# Fri, 09 Jun 2023 02:03:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Fri, 09 Jun 2023 02:03:00 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Fri, 09 Jun 2023 02:03:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 09 Jun 2023 02:03:07 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 09 Jun 2023 02:10:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 09 Jun 2023 02:10:33 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 09 Jun 2023 02:10:34 GMT
RUN docker-php-ext-enable sodium
# Fri, 09 Jun 2023 02:10:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jun 2023 02:10:34 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 02:10:35 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 09 Jun 2023 02:10:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jun 2023 02:10:35 GMT
EXPOSE 9000
# Fri, 09 Jun 2023 02:10:35 GMT
CMD ["php-fpm"]
# Fri, 09 Jun 2023 03:58:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Fri, 09 Jun 2023 03:58:19 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 09 Jun 2023 03:58:19 GMT
COPY file:24bf6e4ff958bf58ae126804a93affdbd6a0bf41615cc91af3f7538a88742dbd in /usr/local/bin/ 
# Fri, 09 Jun 2023 03:58:20 GMT
ENV DRUPAL_VERSION=10.0.9
# Fri, 09 Jun 2023 03:58:20 GMT
WORKDIR /opt/drupal
# Fri, 09 Jun 2023 03:58:29 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Fri, 09 Jun 2023 03:58:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c41833b44d910632b415cd89a9cdaa4d62c9725dc56c99a7ddadafd6719960f9`  
		Last Modified: Wed, 29 Mar 2023 17:39:44 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d77c941283c11ee9f230d663ff3c25aca7870a31444cb1723c18ee503842665`  
		Last Modified: Wed, 29 Mar 2023 22:25:36 GMT  
		Size: 1.9 MB (1872947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324637722404787754813e943dd4dc9a3350498eef87dba1fb032bfd71f0d1fe`  
		Last Modified: Wed, 29 Mar 2023 22:25:35 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f6defe637ba8946d3e40ccdba5e5bc73185057e4c2004844feef551800b42e`  
		Last Modified: Wed, 29 Mar 2023 22:25:34 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4388eb72d52678f4ed826710722d2f173d82445e64e7a87feed9986487ef760f`  
		Last Modified: Fri, 09 Jun 2023 03:07:48 GMT  
		Size: 11.8 MB (11813645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7e6a6a35c57152f4ca379d7cbf33bb81f8f83ba5771b2c531204538657cb8d`  
		Last Modified: Fri, 09 Jun 2023 03:07:48 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cac14a8c9fbc71fadf83341d68808d407a641381db9bfa99db5c6028de8fac`  
		Last Modified: Fri, 09 Jun 2023 03:08:04 GMT  
		Size: 15.2 MB (15194171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d00a295721cd801505c9a1d3b5c8f1f81b65eced686e7e5bb5d069f0c545ead`  
		Last Modified: Fri, 09 Jun 2023 03:08:02 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad50be141104975480b922320282dc3e654cf031cbcfb223c1a28e5e8f225fb6`  
		Last Modified: Fri, 09 Jun 2023 03:08:02 GMT  
		Size: 18.9 KB (18873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd8f6fff7d9543622c981e8d0b06aafc858ff91cb1db4971c12ac3a40e3ebaa`  
		Last Modified: Fri, 09 Jun 2023 03:08:02 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d33d0f7e04b36c35e967ae223ff9e76bee5a83c426ef9fb97aa38cb5744403`  
		Last Modified: Fri, 09 Jun 2023 04:16:13 GMT  
		Size: 2.4 MB (2442423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592df042fb833f9f77450b35cd149208f6c40846b62bf4c5d88c2a9526c12790`  
		Last Modified: Fri, 09 Jun 2023 04:16:13 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b775951fe5ea3902eed7897bbf46f6aeb662b244e4441cccb53c71bfbf79f1`  
		Last Modified: Fri, 09 Jun 2023 04:16:13 GMT  
		Size: 698.1 KB (698146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16e63b1fff95adde40f31556f668dd9b66f2b5850fcc626218dc4907c9dfc42`  
		Last Modified: Fri, 09 Jun 2023 04:16:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefa0fc2c5caa72b766b1610ce6e5e71dad978131587d25c9b31aa7716346214`  
		Last Modified: Fri, 09 Jun 2023 04:16:16 GMT  
		Size: 17.7 MB (17675287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:php8.1-fpm-alpine3.17` - linux; 386

```console
$ docker pull drupal@sha256:79a6395bdae244934885c8f7fc734f0cdba48e815af2c914f1d60c3a1ed41cc4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53239718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699f3e7379cb35291a428cf8a43601a380aa6f7d3da664127b26c17e06f655c2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:30 GMT
ADD file:61bc44c9685b610d18bddd05d2ea1e57b4313f5f433a0a0b7e5269ec24f108b0 in / 
# Wed, 29 Mar 2023 17:38:30 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 20:02:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 Mar 2023 20:02:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 29 Mar 2023 20:02:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 Mar 2023 20:02:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 Mar 2023 20:02:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 Mar 2023 20:02:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 20:02:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 20:02:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 29 Mar 2023 20:44:31 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 13 May 2023 01:47:35 GMT
ENV PHP_VERSION=8.1.19
# Sat, 13 May 2023 01:47:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.19.tar.xz.asc
# Sat, 13 May 2023 01:47:35 GMT
ENV PHP_SHA256=f42f0e93467415b2d30aa5b7ac825f0079a74207e0033010383cdc1e13657379
# Sat, 13 May 2023 01:47:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 13 May 2023 01:47:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 13 May 2023 01:59:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 13 May 2023 01:59:58 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 13 May 2023 01:59:59 GMT
RUN docker-php-ext-enable sodium
# Sat, 13 May 2023 01:59:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 13 May 2023 01:59:59 GMT
WORKDIR /var/www/html
# Sat, 13 May 2023 02:00:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 13 May 2023 02:00:00 GMT
STOPSIGNAL SIGQUIT
# Sat, 13 May 2023 02:00:00 GMT
EXPOSE 9000
# Sat, 13 May 2023 02:00:00 GMT
CMD ["php-fpm"]
# Sat, 13 May 2023 03:53:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 13 May 2023 03:53:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 24 May 2023 23:01:45 GMT
COPY file:24bf6e4ff958bf58ae126804a93affdbd6a0bf41615cc91af3f7538a88742dbd in /usr/local/bin/ 
# Wed, 24 May 2023 23:01:45 GMT
ENV DRUPAL_VERSION=10.0.9
# Wed, 24 May 2023 23:01:45 GMT
WORKDIR /opt/drupal
# Wed, 24 May 2023 23:01:58 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Wed, 24 May 2023 23:01:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:b2b0f0faedf1b87a3c77cf90d027fb7a25aa67f35400244a4655ad5842a757e4`  
		Last Modified: Wed, 29 Mar 2023 17:39:00 GMT  
		Size: 3.4 MB (3412260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7929931a828d2015dd9e95a14bd27c73e8ed62100cf82854210175cc954be7`  
		Last Modified: Wed, 29 Mar 2023 21:49:02 GMT  
		Size: 2.0 MB (1992200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026beb5ca186e3c7d06eeb9c4ef9f6f17d8413c0ea078b6b51778c9f64557608`  
		Last Modified: Wed, 29 Mar 2023 21:49:02 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2223ea2b0fd26911a7879b6d53134b714418def170fb74dd549259cdd83ad5f`  
		Last Modified: Wed, 29 Mar 2023 21:49:01 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c86c6b8303aee7f98e1081d0cf76d7c6a24a0bd02a6b8fd34616bce72cf94d`  
		Last Modified: Sat, 13 May 2023 02:11:32 GMT  
		Size: 11.9 MB (11867563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55ffda4783cd9baf665dad25fc3f99446c4384e60faf2b795ceb7a0206a31ec`  
		Last Modified: Sat, 13 May 2023 02:11:31 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ceebcf781d40fc966e872f0ad4b857ee3c8a139e5a00d9a0d4506765e807005`  
		Last Modified: Sat, 13 May 2023 02:11:52 GMT  
		Size: 15.3 MB (15277870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613a272a749c5ac15732aac27f798156fbbda7d63b997a80375bfe798d0f3cd0`  
		Last Modified: Sat, 13 May 2023 02:11:49 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f817ecfceccf127501ce316002ffe90243ee74a6d2c9d7ca4eb5c695881f2217`  
		Last Modified: Sat, 13 May 2023 02:11:49 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a081d73f7808e1e6b5238e87bf700a441c6c2887390f7573848f8645274af85f`  
		Last Modified: Sat, 13 May 2023 02:11:49 GMT  
		Size: 8.9 KB (8879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da874b19c18203166b0efb3719a09806ccdd4742370df71c355548e9072d0ee`  
		Last Modified: Sat, 13 May 2023 04:01:23 GMT  
		Size: 2.3 MB (2283508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae0dbb67b59453eea7e93707678347bc28fa85a727592f08abb4349db070300`  
		Last Modified: Sat, 13 May 2023 04:01:23 GMT  
		Size: 312.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6accdafd043e34b8000929ee0fb21d2d6b5e8bd855224f76008d5b6b7bef05`  
		Last Modified: Wed, 24 May 2023 23:17:58 GMT  
		Size: 698.1 KB (698150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610e5ab5ab0cb23d9d32522f6be49c596943e0f15d02726b2f27f57aa38bf3eb`  
		Last Modified: Wed, 24 May 2023 23:17:58 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eace380f0fd9a2aa1a3cd92c82f6e1c7aad4fe993c91682ccfc7616e05a9f304`  
		Last Modified: Wed, 24 May 2023 23:18:04 GMT  
		Size: 17.7 MB (17675316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:php8.1-fpm-alpine3.17` - linux; ppc64le

```console
$ docker pull drupal@sha256:2e77102e671882c9abd58016fa9372437324dfb02ac9eb2d2bf72ef86c67b7b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53166610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb546783f7779ed5a10b39efc338ec996e00ab7a752bc59cdb37ff2fbeeeaac`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 29 Mar 2023 18:16:27 GMT
ADD file:e95c1f256ba4bda85c5cbc0d8e84e6f329aa17c9dd2715b2da043e2139049124 in / 
# Wed, 29 Mar 2023 18:16:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:36:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 Mar 2023 22:36:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 29 Mar 2023 22:36:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 Mar 2023 22:36:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 Mar 2023 22:36:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 Mar 2023 22:36:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 22:36:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 22:36:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 29 Mar 2023 23:07:42 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 09 Jun 2023 01:16:58 GMT
ENV PHP_VERSION=8.1.20
# Fri, 09 Jun 2023 01:16:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Fri, 09 Jun 2023 01:16:58 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Fri, 09 Jun 2023 01:17:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 09 Jun 2023 01:17:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:24:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 09 Jun 2023 01:24:58 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:25:00 GMT
RUN docker-php-ext-enable sodium
# Fri, 09 Jun 2023 01:25:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jun 2023 01:25:00 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 01:25:01 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 09 Jun 2023 01:25:01 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jun 2023 01:25:01 GMT
EXPOSE 9000
# Fri, 09 Jun 2023 01:25:02 GMT
CMD ["php-fpm"]
# Fri, 09 Jun 2023 03:04:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Fri, 09 Jun 2023 03:04:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 09 Jun 2023 03:04:17 GMT
COPY file:24bf6e4ff958bf58ae126804a93affdbd6a0bf41615cc91af3f7538a88742dbd in /usr/local/bin/ 
# Fri, 09 Jun 2023 03:04:17 GMT
ENV DRUPAL_VERSION=10.0.9
# Fri, 09 Jun 2023 03:04:17 GMT
WORKDIR /opt/drupal
# Fri, 09 Jun 2023 03:04:37 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Fri, 09 Jun 2023 03:04:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:1b7d25764eb3d3c55d73f5dfb9e3e9d75f3f39132e1b16142319de2a062dd673`  
		Last Modified: Wed, 29 Mar 2023 18:17:14 GMT  
		Size: 3.4 MB (3390935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdac02b375fa12e4f7e544161fe642829107cb793b902ce9767a6fd39b686cc4`  
		Last Modified: Wed, 29 Mar 2023 23:54:26 GMT  
		Size: 2.0 MB (1957752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678a0f24012397aebcdbcea1e47fc787669721aa4dcc86d8a479a3dfaaf65bc5`  
		Last Modified: Wed, 29 Mar 2023 23:54:25 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120694ccc44924cba22112225821e706b18ee4ef54190ecb4f21d5a8b6262ec4`  
		Last Modified: Wed, 29 Mar 2023 23:54:25 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c125b61903038afeadf6d982a9f3927546ede32121d8dfdaa3f36dbbf5b45a24`  
		Last Modified: Fri, 09 Jun 2023 02:32:17 GMT  
		Size: 11.8 MB (11813655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8b7d35fe79733e0274d651bd833a16d4bfbae8a4ec222dd854601a5bf4881e`  
		Last Modified: Fri, 09 Jun 2023 02:32:16 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b5cc7d26e5bb19d87c1954259d16e3f46fee892d6b581b951e56190c7ce9478`  
		Last Modified: Fri, 09 Jun 2023 02:32:43 GMT  
		Size: 15.7 MB (15674784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4a6bb5cfc6902a6ff15ba2b8a34a79d31ee9136130399a2742c8b30f5e638c`  
		Last Modified: Fri, 09 Jun 2023 02:32:38 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7a0e5d0f6a894dcd3140170f82dbd0818eed4c31184317659ff9aa93d3752e2`  
		Last Modified: Fri, 09 Jun 2023 02:32:38 GMT  
		Size: 18.9 KB (18889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f963751773b2fe9ad4103da9f26059d6c8e3e0175834b8e27d191342b2d20ffe`  
		Last Modified: Fri, 09 Jun 2023 02:32:38 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcefb02ec1283f9054901f1996523730141ac651a1003aaeb71d011dfbb5e7df`  
		Last Modified: Fri, 09 Jun 2023 03:25:17 GMT  
		Size: 1.9 MB (1923498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e4826b458f2f74bfce0c3b42715de720d7afe5be9a53e30d41679211bbd248`  
		Last Modified: Fri, 09 Jun 2023 03:25:16 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f584a33c5ffdbff695f46b6ab90fcb3c09b084b03dd25cd0a4361ae95434570d`  
		Last Modified: Fri, 09 Jun 2023 03:25:17 GMT  
		Size: 698.1 KB (698149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ab6e27f19e0655aa8c0510432c1418c488d7c0dec07b992551b31a66251e6f`  
		Last Modified: Fri, 09 Jun 2023 03:25:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9acb513fa078141c1c21f4972a2f47afd467c82b61c5543478542e54513a254a`  
		Last Modified: Fri, 09 Jun 2023 03:25:35 GMT  
		Size: 17.7 MB (17675127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:php8.1-fpm-alpine3.17` - linux; s390x

```console
$ docker pull drupal@sha256:be6b2a57c644e329c4fbe574db972cd96401e2c851c124b9649a329c3fc8e68b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51366396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8bebd2a0c4130bafba71325222738cc16afee3730e42c0433cb221c8e0ca31`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 29 Mar 2023 17:41:57 GMT
ADD file:675ad8acf4b076e34aeeba26dd482be7640df5912b1ec5e3183b7eb69c01e83e in / 
# Wed, 29 Mar 2023 17:41:57 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:02:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 Mar 2023 19:03:01 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 29 Mar 2023 19:03:01 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 Mar 2023 19:03:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 Mar 2023 19:03:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 Mar 2023 19:03:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 19:03:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 19:03:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 29 Mar 2023 19:23:01 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 09 Jun 2023 00:55:39 GMT
ENV PHP_VERSION=8.1.20
# Fri, 09 Jun 2023 00:55:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Fri, 09 Jun 2023 00:55:39 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Fri, 09 Jun 2023 00:55:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 09 Jun 2023 00:55:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:01:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 09 Jun 2023 01:01:04 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:01:05 GMT
RUN docker-php-ext-enable sodium
# Fri, 09 Jun 2023 01:01:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jun 2023 01:01:05 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 01:01:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 09 Jun 2023 01:01:06 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jun 2023 01:01:06 GMT
EXPOSE 9000
# Fri, 09 Jun 2023 01:01:06 GMT
CMD ["php-fpm"]
# Fri, 09 Jun 2023 02:05:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Fri, 09 Jun 2023 02:05:14 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 09 Jun 2023 02:05:15 GMT
COPY file:24bf6e4ff958bf58ae126804a93affdbd6a0bf41615cc91af3f7538a88742dbd in /usr/local/bin/ 
# Fri, 09 Jun 2023 02:05:15 GMT
ENV DRUPAL_VERSION=10.0.9
# Fri, 09 Jun 2023 02:05:15 GMT
WORKDIR /opt/drupal
# Fri, 09 Jun 2023 02:05:23 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Fri, 09 Jun 2023 02:05:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:a76f78d8854217635d8049ec8501edb806f961e72989cfff8503982e6ff2579d`  
		Last Modified: Wed, 29 Mar 2023 17:42:31 GMT  
		Size: 3.2 MB (3175187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6521aff379460e3b23538794f9f58987d8c205d856adb8b1906678f475549d`  
		Last Modified: Wed, 29 Mar 2023 19:53:09 GMT  
		Size: 1.9 MB (1926778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ccc0e3e0585970bf7f018f1b481c5bda3c11ade58ae10a67fac7eb146920ec`  
		Last Modified: Wed, 29 Mar 2023 19:53:09 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ffa02384e22bdeff50d42395895a9ce2b39494195bc42784c30061aa4ea5384`  
		Last Modified: Wed, 29 Mar 2023 19:53:09 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3402ace89152441ac7d199f7d3cee24a56ade6b9641e7297fe5c3f4682a6ab`  
		Last Modified: Fri, 09 Jun 2023 01:39:41 GMT  
		Size: 11.8 MB (11813657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ae5448bad198f00d9d8b1ddb45e958fd3dd8fc74d1030d2dd5b0ee18c10618`  
		Last Modified: Fri, 09 Jun 2023 01:39:40 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfab716aac91c3a4754aef0092dc326bbf772dce6ee2c2749afad1f20b39d99b`  
		Last Modified: Fri, 09 Jun 2023 01:39:53 GMT  
		Size: 14.2 MB (14242110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caf1cb2284e2279dea5071b1c5e753c1167c7764c11ab5c261d9e1e0501c015`  
		Last Modified: Fri, 09 Jun 2023 01:39:51 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2717a47340667abb71735e4882881ebdf56cfdb3452400cfa2339ee6eace2ea1`  
		Last Modified: Fri, 09 Jun 2023 01:39:51 GMT  
		Size: 18.9 KB (18895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56de5280ccea55333ff2628a4fe13eaf5bd8e132003dd6e48b7885045f35b1c`  
		Last Modified: Fri, 09 Jun 2023 01:39:52 GMT  
		Size: 8.9 KB (8876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dce2c105ab08c5a5cb1ad8aa86bb8b16c9e32cb670c21ab3d9df79198d422a`  
		Last Modified: Fri, 09 Jun 2023 02:16:56 GMT  
		Size: 1.8 MB (1802569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3b43da45248eda8dabbc4e4631404e606cc496f94366e48e579496da2b766d`  
		Last Modified: Fri, 09 Jun 2023 02:16:56 GMT  
		Size: 312.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2fff6b34fa91578a22164f02800482fab0ff195d289a185f197065bea69a95`  
		Last Modified: Fri, 09 Jun 2023 02:16:56 GMT  
		Size: 698.1 KB (698148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5117d78d60c0bf02cfe20e2db7e9502eb4d7703649606ab02bcb724e1cc460`  
		Last Modified: Fri, 09 Jun 2023 02:16:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db7d6e61255c0382990258374cfad7d9434ba7873165e445a74ed409546e6ee`  
		Last Modified: Fri, 09 Jun 2023 02:16:59 GMT  
		Size: 17.7 MB (17675241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
