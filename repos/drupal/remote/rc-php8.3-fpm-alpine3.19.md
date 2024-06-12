## `drupal:rc-php8.3-fpm-alpine3.19`

```console
$ docker pull drupal@sha256:1d86d968ef5c9bfae6b6d61300aa0221bcbab3998fa250ed27754934d8865b59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `drupal:rc-php8.3-fpm-alpine3.19` - linux; amd64

```console
$ docker pull drupal@sha256:f12d6e9f5f7f0b0f6307b716aed7d6bc3ca395ce88a7f461165269f0681c1389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55836786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851a07d41eddc0cf131af7a681f7da052a4534c9e9ef42808a1a9d2e85f53f62`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.3.8
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 9000
# Wed, 22 May 2024 23:55:49 GMT
CMD ["php-fpm"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d2971301bcdd9c073bdf8f9aa1450f4c60e5f21c5c562ffbd80e6e1a289329`  
		Last Modified: Wed, 29 May 2024 23:21:56 GMT  
		Size: 4.8 MB (4846730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6eca4f18622dc57cfbd6cfb4e5caa4c20e8258bd546867d78e401b4ab90046`  
		Last Modified: Wed, 29 May 2024 23:21:55 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d35b189a56bd7418ef643cf710934d9d6ee2c2f34f5565b7876b7f65c0147b`  
		Last Modified: Wed, 29 May 2024 23:21:55 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4edc397ae5aa6295650446d615084c0bc342f9de33250b55c9b0f67ebdfd6d3`  
		Last Modified: Thu, 06 Jun 2024 22:15:26 GMT  
		Size: 12.5 MB (12502052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61392208410a1a5c60270725db4acf169d42c124baa97cff833a7c67527957ec`  
		Last Modified: Thu, 06 Jun 2024 22:15:25 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee5804676fa0df8da330b24532e776eaa1a79aacd8d8630c02e18282c5efa4a`  
		Last Modified: Thu, 06 Jun 2024 22:15:51 GMT  
		Size: 13.1 MB (13081176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b55d7a64eb4c882693f476d7d1fcfc4412f4da360830e14b5fb6ed9167a7a7`  
		Last Modified: Thu, 06 Jun 2024 22:15:49 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de2bd55d517b073940dcbd91c75e8c5235f507aa75732461fd7f1a8e416c795`  
		Last Modified: Thu, 06 Jun 2024 22:15:49 GMT  
		Size: 19.5 KB (19540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a326e5f4c37a5c27a6da2cadaf62feca619218c14987a7f530f86e4a0abb60f6`  
		Last Modified: Thu, 06 Jun 2024 22:15:49 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cc0c9d6c223a346834a83dc594f2cc9dcccbe7ebe04f58932ab838bcb3abfb`  
		Last Modified: Tue, 11 Jun 2024 21:31:24 GMT  
		Size: 2.3 MB (2285456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728b42539925d53e33e68d06e45b5695722ce4cce7905a9053889cab4335465f`  
		Last Modified: Tue, 11 Jun 2024 21:31:23 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ed9cdea5cba38c5164a85553b717500c63d266f82a61efb7d088d578ba8bc8`  
		Last Modified: Tue, 11 Jun 2024 21:31:24 GMT  
		Size: 726.3 KB (726336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290b25a2f4fdf10087902ed0ff58aaad5d687864463016682f497f8b9e8f33a1`  
		Last Modified: Tue, 11 Jun 2024 21:31:17 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f1345ac2d1314b001a6921d0c29fd260e7e057673d3ee41dc6cf1626c8c4a1`  
		Last Modified: Tue, 11 Jun 2024 21:31:25 GMT  
		Size: 19.0 MB (18952689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:7f39f424a24fe63c61dfa17b22661d2bc095138088e57005ca79bde7a9b5de77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 KB (363342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3085c54a56516dd7aca0eb66968805868a1e5dcb43366ae1f2c5f6937a516d`

```dockerfile
```

-	Layers:
	-	`sha256:b156a2194b3bf780e355ce6858870d815510ba22edda6b373d5f6d8fa200ff41`  
		Last Modified: Tue, 11 Jun 2024 21:31:23 GMT  
		Size: 332.4 KB (332423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb39001b349c49de277f13bbd62fa7c9042608c7f7cb89455032bd3d4a10d856`  
		Last Modified: Tue, 11 Jun 2024 21:31:23 GMT  
		Size: 30.9 KB (30919 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-fpm-alpine3.19` - linux; arm variant v6

```console
$ docker pull drupal@sha256:85dcb0f1033f99e5233dbf388dbe7bb16d4c066538ba1f53afc7b83aa3978584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53561449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56cb644818bb331a0363ed0e3d9a2626cf3056749bc5aac93a6876202bb88928`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.3.8
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 9000
# Wed, 22 May 2024 23:55:49 GMT
CMD ["php-fpm"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2229a68e5f4f86db5402477557a0acd824685f1fc1febf404b55582dae8523`  
		Last Modified: Wed, 29 May 2024 22:48:03 GMT  
		Size: 4.5 MB (4526759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f4c459ba5cca05920bae64311fbd4ff52ebbc94c47b443a16c2eee7a61c9b6`  
		Last Modified: Wed, 29 May 2024 22:48:02 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12b140fecb4e26370e6fbbfd503e5d22ad02d6dadf0bd8ac1a5ac70e6d56a85`  
		Last Modified: Wed, 29 May 2024 22:48:01 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185401401dd456ab79237280705dc8e8a255f2c578a1250daa3cf9142cd1626a`  
		Last Modified: Thu, 06 Jun 2024 20:18:45 GMT  
		Size: 12.5 MB (12502073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1400ebf518de76d2327324d7f55d54dd1eb69728c2cb84790f0d1648a281e932`  
		Last Modified: Thu, 06 Jun 2024 20:18:43 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e68d28333124fc25f0e77af92b1314fe26afa60dc9491a5ef100fa7021a2536`  
		Last Modified: Thu, 06 Jun 2024 20:19:13 GMT  
		Size: 11.9 MB (11911693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae2f99d77ffc6432b2e1aa32189b81296574fbee549262514151fd1478e6b66`  
		Last Modified: Thu, 06 Jun 2024 20:19:10 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c96845e1b4de264ce7ab0e5c05516e197f037b861f796e7957645f8163ae7b`  
		Last Modified: Thu, 06 Jun 2024 20:19:10 GMT  
		Size: 19.4 KB (19406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2362e0d0873bc1ed6d40b766cae1c18a58c871445e8099822aad59450c3663a7`  
		Last Modified: Thu, 06 Jun 2024 20:19:10 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b436c05b36388f1550fb50106fff85c742290f53988f87955556e4cd9a2868e`  
		Last Modified: Tue, 11 Jun 2024 20:25:42 GMT  
		Size: 1.7 MB (1742633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715b6bb7546c21b39e2b8a0bf641a36eb814274498d0fcf653f206665aa01ff2`  
		Last Modified: Tue, 11 Jun 2024 20:25:41 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17736a99d0c76a8da96e0eceffd6d0d8da29ccc7c811ac1436d7499614b093ae`  
		Last Modified: Tue, 11 Jun 2024 20:25:42 GMT  
		Size: 726.3 KB (726333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f579dd1a3984b7b8d6fac57b5451be60c4019f1b929a8276728d247a2e343b69`  
		Last Modified: Tue, 11 Jun 2024 20:25:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3daa3f3a369afd529781f97aaf55c21f4d1e837bf51cfcbbc8ddc2676341a286`  
		Last Modified: Tue, 11 Jun 2024 20:25:43 GMT  
		Size: 19.0 MB (18953078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:b2bf5c655659fb7dcb6e1474406464f76a5ffda8aef68c0c382348b4f7b0d892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eaf92214ef5322001f2b0f7dcedb6c98fd7670270f5f64068991787ad4088a7`

```dockerfile
```

-	Layers:
	-	`sha256:80f20d56277f9a6f048ad4e2b665b4b18ed08c8ababac116a4ed3707d8e653ab`  
		Last Modified: Tue, 11 Jun 2024 20:25:41 GMT  
		Size: 30.8 KB (30805 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-fpm-alpine3.19` - linux; arm variant v7

```console
$ docker pull drupal@sha256:bac44511b15ac0f9100145fbeb98e0137d6d2757371c5e92e3b40981ff661367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52165536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc8d2ebc52814aa6666e7d300ff83eb7279d1ddda351b9032129042f509ffd7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.3.8
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 9000
# Wed, 22 May 2024 23:55:49 GMT
CMD ["php-fpm"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088b4454adc82bbe41a7504afeea8c70e4e1187c518a074b8ff18e3e702de7b4`  
		Last Modified: Wed, 29 May 2024 23:38:25 GMT  
		Size: 4.3 MB (4252799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d688abfb00a3c7f5d950844e9028329f3979cbf79db5a56101ffcd0a7394b3`  
		Last Modified: Wed, 29 May 2024 23:38:24 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61edfbd90c304f9b7f03debefa789bb098f8a561f066072f06a934d6b8f758f`  
		Last Modified: Wed, 29 May 2024 23:38:24 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440cf2c85ff411ba5fc9f318276fbc5c93e34154a29d186a481aa923e998964a`  
		Last Modified: Thu, 06 Jun 2024 21:41:51 GMT  
		Size: 12.5 MB (12502063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3dd319ee757868fa5df7eb32c50976c22c95be708a1660a71a07ad98bb9eefb`  
		Last Modified: Thu, 06 Jun 2024 21:41:50 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055ded67a613d026048521a3bac1cba173003f0835bfb7b82c9048fa86dbd4d6`  
		Last Modified: Thu, 06 Jun 2024 21:42:16 GMT  
		Size: 11.2 MB (11171984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc0e6cdf1f43bfa6bbe87e628a4b0bb6434cfc5569704d1e95b7bb3adcb24d6`  
		Last Modified: Thu, 06 Jun 2024 21:42:13 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5459631dea4f6cd68e6b8490bb0861b57ae009d1a166a0723754df854e3c1f7d`  
		Last Modified: Thu, 06 Jun 2024 21:42:13 GMT  
		Size: 19.4 KB (19371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d7b9fb9a096bad129982d30083448e3672a06b7dad1421315c9258b5b96769`  
		Last Modified: Thu, 06 Jun 2024 21:42:13 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268f79688a921f6b00eea0f61f4348992e60d3b36d1169fe62d35f29783bfd30`  
		Last Modified: Fri, 07 Jun 2024 02:40:05 GMT  
		Size: 1.6 MB (1606933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efcf051dfd3091ecbafabfe119215ba8d66fa6eec16f1ce065bfcaa136bba65`  
		Last Modified: Fri, 07 Jun 2024 02:40:05 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335ebbd72cc4fcc8734c1917d8413bed78dc1fa5d3b86ffb3bffc6129ca5a234`  
		Last Modified: Tue, 11 Jun 2024 20:28:49 GMT  
		Size: 726.3 KB (726344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5db2a587fe8549fc055c77a131798ba80c141b34b605e7c0d2847177a38331`  
		Last Modified: Tue, 11 Jun 2024 20:28:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadc4933600976c99dbd24a768ad162d63cbcf8222574d97e179429bcc427c5f`  
		Last Modified: Tue, 11 Jun 2024 20:28:50 GMT  
		Size: 19.0 MB (18953062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:8ff6165b984665987765f0fedf4f9f7ed29c182943a1c818799c08232ec55af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.9 KB (360897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb9e5f74bd1d50068c3b209544b3d232716a4ece779eaec2408ecf3f7d6e4fc`

```dockerfile
```

-	Layers:
	-	`sha256:fa37a911e07e5df24af6bdad711d23f3fe6a4f1dc18648508c3f863c7aeb97a1`  
		Last Modified: Tue, 11 Jun 2024 20:28:49 GMT  
		Size: 329.9 KB (329873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ee564d4dd11a7db0270f3c7e6a91460f6112e67ff7fb9310e93e1ef4be10f19`  
		Last Modified: Tue, 11 Jun 2024 20:28:49 GMT  
		Size: 31.0 KB (31024 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-fpm-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:7bb5d5b2e998ebb8beda12d6b724e41109e448440c0ab38719b41e5c16cc3096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56044820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ddec7235591f16418a18c5526ca1ab8be14f186bbc94e2403257168fcd3ce91`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.3.8
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 9000
# Wed, 22 May 2024 23:55:49 GMT
CMD ["php-fpm"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26433807f0468065894f45f9497291f39a3db456cffd88af5b9d2f6d0ae95c4`  
		Last Modified: Wed, 29 May 2024 22:57:09 GMT  
		Size: 4.8 MB (4787316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7a3c657d5b04b42d4c7eb55f558eff7ec2d0a94f37222e83a6d3f8cbb36020`  
		Last Modified: Wed, 29 May 2024 22:57:08 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a97a54affa9d799fc31695d2347f0515f3bd4c2e66cc60765c43fa4220d3042`  
		Last Modified: Wed, 29 May 2024 22:57:08 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e631c4a552607885926986d3506574bbc7d2875b3a77f3348604a0ca5fd73b5`  
		Last Modified: Thu, 06 Jun 2024 22:22:36 GMT  
		Size: 12.5 MB (12502058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44edb4e4e09b47e189b5e64082d4f676b6dbebd1a80e66aea72c1e81fac52d98`  
		Last Modified: Thu, 06 Jun 2024 22:22:35 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e661a26ea08c0d94323f995a05a2d54cd05f933ee056ecb46806fc8417d7a4c`  
		Last Modified: Thu, 06 Jun 2024 22:23:00 GMT  
		Size: 13.1 MB (13135519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df22f413c5ba128fb3960b8b9c85785ef7b608b3cf640997d658070b0c2977a6`  
		Last Modified: Thu, 06 Jun 2024 22:22:58 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac860e65ee0a8b6dce025664a022bf7463fd1905c6baba1bcb46f913c7470a8f`  
		Last Modified: Thu, 06 Jun 2024 22:22:58 GMT  
		Size: 19.4 KB (19361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8d2f1d386b92b5cbdf26cd947a81fb347d3591fd8d14fd80bc07435f4fd025`  
		Last Modified: Thu, 06 Jun 2024 22:22:58 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f34b8ac92991347ea6e07354db7629b826a28e916b20f407c3842977691497`  
		Last Modified: Fri, 07 Jun 2024 04:24:41 GMT  
		Size: 2.6 MB (2559178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bbe3b65878d2f045d21407ca72bbcf77e44ff7df9c64d60730612ed535f782`  
		Last Modified: Fri, 07 Jun 2024 04:24:41 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85324065d10e5e6e0ac657731e1cd143a6d3b171634d0a804463512eb3f9e5dd`  
		Last Modified: Tue, 11 Jun 2024 20:29:55 GMT  
		Size: 726.3 KB (726344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97c3a2e1132d45b22e50d24091152aebc719c871d3223fc32dffd1163999999`  
		Last Modified: Tue, 11 Jun 2024 20:29:55 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059afa5359f5d1ac155f5746e50028f08d180e6e077db91c6f146b2692972f45`  
		Last Modified: Tue, 11 Jun 2024 20:29:56 GMT  
		Size: 19.0 MB (18953242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:dd35871eba4e2623bbc05c82fba9e66ca3674c30c33870205faa5071778ed04a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.3 KB (361344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20589f8e184ed4eb341c31365c620caa0d469fc68a641f086b4eef5b9c928ab`

```dockerfile
```

-	Layers:
	-	`sha256:2691845cc7a730dc0b88ea8eeed61694d5d0b9b716b031ab4a4bf8d5c5678941`  
		Last Modified: Tue, 11 Jun 2024 20:29:55 GMT  
		Size: 329.9 KB (329889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adc1ab8b9b4a05fe1bba94085306349c380ec6e36fcb855324b3d67bd5195bd2`  
		Last Modified: Tue, 11 Jun 2024 20:29:54 GMT  
		Size: 31.5 KB (31455 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-fpm-alpine3.19` - linux; 386

```console
$ docker pull drupal@sha256:af93d580f536f9f502430530ab63995cbaafd5c39baabaa0f10e07e125da120c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55925061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e812eb2a29ce7dc57c958a506cad20fdce52abca7707dac5646b9c0d72bf3f3d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.3.8
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 9000
# Wed, 22 May 2024 23:55:49 GMT
CMD ["php-fpm"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e75aa876d0175107afbef0c61070688285c7b2563a3ebebd8948d22b60eb20`  
		Last Modified: Thu, 30 May 2024 00:15:47 GMT  
		Size: 4.7 MB (4736177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d04940901e8e4d826ac6b537e8d775fa620454ca3a24dc3b7635c87424eb1fe`  
		Last Modified: Thu, 30 May 2024 00:15:46 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a05a1ebdbd38a39011e62e26d21abb4f411078bb16663ebb3cd6623c9ea690`  
		Last Modified: Thu, 30 May 2024 00:15:46 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8617d86b4f529fe96df565c8fcc0949fd64c357d918f339771589e79e488a1b`  
		Last Modified: Fri, 07 Jun 2024 00:10:46 GMT  
		Size: 12.5 MB (12502074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4eea57379a2fff2bdcbf63fb2f00c23ad7dc16b32724f11bfbde44d022beddc`  
		Last Modified: Fri, 07 Jun 2024 00:10:44 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da02a5b16d8b041bac1a4fb73ca441f89a915294ce192bdfc8f820bc6494b07`  
		Last Modified: Fri, 07 Jun 2024 00:11:14 GMT  
		Size: 13.4 MB (13408800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e3075f451858cf44e3b7e6323be6d33746cbe9ccf915e9d5b3e0f7b79d9a16`  
		Last Modified: Fri, 07 Jun 2024 00:11:11 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefb7a98fd56e8209c0f64798268694c2d83662948861c7a0194386a9e0cac91`  
		Last Modified: Fri, 07 Jun 2024 00:11:11 GMT  
		Size: 19.5 KB (19548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd1831ec74b833ff13a95664713381a7636dcf306e593daf70daf4a40e44264`  
		Last Modified: Fri, 07 Jun 2024 00:11:11 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6300a04c24306677c25ca2c54d5c62c08fcd4ee07844e65077ffa24010601b`  
		Last Modified: Tue, 11 Jun 2024 21:28:34 GMT  
		Size: 2.3 MB (2320833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2ae4c6ce8916c4cdccf34559dbc071f167e937f4c52b2c41ffd2f8f40b9a4d`  
		Last Modified: Tue, 11 Jun 2024 21:28:34 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77aa6b7ab423a2519f47aa670964f689c8938c86bcf0cdd1d72db8b45bb4145f`  
		Last Modified: Tue, 11 Jun 2024 21:28:34 GMT  
		Size: 726.3 KB (726332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d554b0ac8b87f6268d32d76c0495fdaa1c64d15ab11d5e93bb81107397ff15`  
		Last Modified: Tue, 11 Jun 2024 21:28:34 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8519ad45b75bf569855325041f40973ed5be2d3954d82d53ef9feb6c7ac011`  
		Last Modified: Tue, 11 Jun 2024 21:28:35 GMT  
		Size: 19.0 MB (18953200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:1617f0337956b5df5fe3e5cb88ece3c64fd68ee786597e54893e0e5ceefb8e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 KB (363290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6887992c842f7f58b3f52e6727ea372a746d6f5406070cd8c30eee53dc802e4`

```dockerfile
```

-	Layers:
	-	`sha256:f09ae076e6cd88c2aa4daa1afc67425987a5c5cca71ec126068d969fa64bc3a5`  
		Last Modified: Tue, 11 Jun 2024 21:28:34 GMT  
		Size: 332.4 KB (332403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b47da3b51103f206e0ca070bae8bec041bed82074d098fb04d9d44a03d1a300c`  
		Last Modified: Tue, 11 Jun 2024 21:28:34 GMT  
		Size: 30.9 KB (30887 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-fpm-alpine3.19` - linux; ppc64le

```console
$ docker pull drupal@sha256:ee5107ee76216bae155d8f9e1b19961c0105c7f5a8a352c83d27d1f58adcc858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56043858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c290475c1b32e88ac44342c9ca475ae8073a0564172f716c6a0f38892fc4ef4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.3.8
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 9000
# Wed, 22 May 2024 23:55:49 GMT
CMD ["php-fpm"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bc7b61f0d6c154a90a7449b3f9e5fa6497e2e84a90c6ff1c7f0f1d742b5b52`  
		Last Modified: Wed, 29 May 2024 23:51:40 GMT  
		Size: 4.8 MB (4788779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5baf8353008dcf3f5f5e69195782dd4d310c8981e26e9e5b2ecd879453e6af87`  
		Last Modified: Wed, 29 May 2024 23:51:38 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db08c338789dc2268a39e0965af54e2cef9499012fd62f56f8fe38143b578825`  
		Last Modified: Wed, 29 May 2024 23:51:39 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a70ada2c1f1588bd90f52a8e93ac3e68da6cb8e342271dbb9b9c9c65abad62`  
		Last Modified: Thu, 06 Jun 2024 21:31:01 GMT  
		Size: 12.5 MB (12502071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50f6dfd299af22c73ab6578ea2ff8a9d931be3e5394b7176aed1a91d447d504`  
		Last Modified: Thu, 06 Jun 2024 21:31:00 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfed25a390d4a8c1ecbd161fe1e4626a80bd5e9b60d1f75f9e2cb8420a7069c`  
		Last Modified: Thu, 06 Jun 2024 21:31:28 GMT  
		Size: 13.6 MB (13575920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4d127865ecba4537097870f425f4cf9c0c1bf9d22c8cf31e3d5ec2283ece8a`  
		Last Modified: Thu, 06 Jun 2024 21:31:25 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d4e7c3dd1ee514c47f782d0480f5d8b7e738e1bca0a035b38c80d1939af5de`  
		Last Modified: Thu, 06 Jun 2024 21:31:25 GMT  
		Size: 19.4 KB (19380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6258aea9f91653209bdb167a38f668dc06cc761278a90e620f1e832f744fb626`  
		Last Modified: Thu, 06 Jun 2024 21:31:25 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa985ad70e5a67218b34cc5cc2809d801c38cb546b3acca78137c6dd334fe0f`  
		Last Modified: Fri, 07 Jun 2024 03:00:30 GMT  
		Size: 2.1 MB (2105705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c303cc3900b922cb023ee1d10114efff6d27e5b88425b8572fefaa1ffd98dc1d`  
		Last Modified: Fri, 07 Jun 2024 03:00:30 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ae92f654d4694c91ffead8d2ee08bfa7b55da0d0ea6a11c10dbfff78056659`  
		Last Modified: Tue, 11 Jun 2024 20:30:37 GMT  
		Size: 726.3 KB (726347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a374be5067e903c302d532ae6252d6d25074eaf3b705eefdb3de61505da0cc75`  
		Last Modified: Tue, 11 Jun 2024 20:30:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54bbaece12167e34a4405f83c0e32673c8a5927b533c3074e1d159ec82f4d57e`  
		Last Modified: Tue, 11 Jun 2024 20:30:38 GMT  
		Size: 19.0 MB (18953218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:a4ef36ead738ba83ffffabbfb03a29850f3940f92a84194d7caaa372750d232d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 KB (358879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d609c6176e40eb64f517f26ec130b3089b5bb9a17f9cad5cfdf9ecab58649a7`

```dockerfile
```

-	Layers:
	-	`sha256:eb6633985424caccc9816b5749a9ad37f2a30517ba84f7716e72854b8852fb87`  
		Last Modified: Tue, 11 Jun 2024 20:30:36 GMT  
		Size: 327.9 KB (327919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da7ab0ee2335292f3bbc4541c40d3f0ec965750941b85d06e2a6948a85a1f74a`  
		Last Modified: Tue, 11 Jun 2024 20:30:36 GMT  
		Size: 31.0 KB (30960 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-fpm-alpine3.19` - linux; s390x

```console
$ docker pull drupal@sha256:26e2ed2a93d418e67fcbc3835faea927f78d75102096508b5010f29524e731a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.3 MB (55275972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb596d43ddcd46318e25bf8851eb14b77daf04ee1aefce22ae8ed492c9eebe9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.3.8
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 9000
# Wed, 22 May 2024 23:55:49 GMT
CMD ["php-fpm"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e00f6a8508d8306ae24777e19275b3fff54f696990bd1320879334cad1f6c5c`  
		Last Modified: Wed, 29 May 2024 22:45:21 GMT  
		Size: 4.8 MB (4777857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdee0a99f51be1369ba1dac55491a74682fc1d1cbff938b761f17e8f38339bd7`  
		Last Modified: Wed, 29 May 2024 22:45:20 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c00f21ce3de9eedb877e74c52769132188e5339e09c0fa75b35357307e9060`  
		Last Modified: Wed, 29 May 2024 22:45:20 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6acae5f59d2ab39278058851dcc9cd80febf284298c73f89184e52bc3f8e973`  
		Last Modified: Thu, 06 Jun 2024 22:02:41 GMT  
		Size: 12.5 MB (12502070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbf48058bb07f968ddfdd07dc6f9f8a8e111b02e62ef5272555572c19159524`  
		Last Modified: Thu, 06 Jun 2024 22:02:41 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c71791f81eef629802f8195fb4398ee5f0e7349c50d60166c6d083990504a87`  
		Last Modified: Thu, 06 Jun 2024 22:03:01 GMT  
		Size: 13.0 MB (13039981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb31a9d81b9d573426878f7cee5735b9953311c21e6ead17e13d51296147050`  
		Last Modified: Thu, 06 Jun 2024 22:02:59 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93254a5959498e4980957d629fe2ea569384e3bdab71f4eb96b69cb185b2e68`  
		Last Modified: Thu, 06 Jun 2024 22:02:59 GMT  
		Size: 19.4 KB (19374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b88772770545254a82abbae017b014d91f346c21af43fc5064b1b19fdf8c497`  
		Last Modified: Thu, 06 Jun 2024 22:02:59 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9ab0efc92a4a335968029a013f12ebd7477ff640ed906f8e3b0930a6bd873a`  
		Last Modified: Fri, 07 Jun 2024 02:32:45 GMT  
		Size: 2.0 MB (2000358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf1699826c172d998ee19da09ee3adefb5b6e1d2990d7dbb11a4ce8873dff54`  
		Last Modified: Fri, 07 Jun 2024 02:32:45 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda4ed241b4a5bbe84fe7ab175fbf0f404d1002ba9f124f9915b58588621f612`  
		Last Modified: Tue, 11 Jun 2024 20:29:52 GMT  
		Size: 726.3 KB (726344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7812eb82514bac1fb69d9de09b11b728538c357c3ec62f297bbd38ac4950a010`  
		Last Modified: Tue, 11 Jun 2024 20:29:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7f444c88f6971835ad6bc0ffd022e585beb4000dde56f5a69999e830025d72`  
		Last Modified: Tue, 11 Jun 2024 20:29:52 GMT  
		Size: 19.0 MB (18953272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:3d401422639498ab7db59a1e6a223c778c9a45f54e29b3e24f95a9f0cdf19ce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.8 KB (358811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf9255e21dd3143df4672ae6a0b1d4369159cf635bf7f350cb37761a59bdabf`

```dockerfile
```

-	Layers:
	-	`sha256:4daebf11ceca4b84c6cdd546f508429fa9a4253b0343fda2a17a107214e95d29`  
		Last Modified: Tue, 11 Jun 2024 20:29:51 GMT  
		Size: 327.9 KB (327891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aab39647e707250eaeb89cd15e525faf3fe96e10098c86d18c56f7a8f10a7377`  
		Last Modified: Tue, 11 Jun 2024 20:29:51 GMT  
		Size: 30.9 KB (30920 bytes)  
		MIME: application/vnd.in-toto+json
