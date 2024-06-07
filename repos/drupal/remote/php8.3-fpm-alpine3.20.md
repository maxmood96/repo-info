## `drupal:php8.3-fpm-alpine3.20`

```console
$ docker pull drupal@sha256:ac33fcd13725f52adef0569b5c12c0ecda9b95567ef53bf59ce7938eea28757f
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

### `drupal:php8.3-fpm-alpine3.20` - linux; amd64

```console
$ docker pull drupal@sha256:d304e4baa89055b1c0bd9479731cb82a371cd53573ffa91d94d0c6125618921f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54407515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57bb0d7e9f4e98693ef09ab164ff4512af58b52641ca1355b33040197c23e12`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 22:49:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 May 2024 22:49:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 29 May 2024 22:49:39 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 May 2024 22:49:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 May 2024 22:49:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 May 2024 22:49:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:49:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:49:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 29 May 2024 22:49:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_VERSION=8.3.8
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Jun 2024 10:04:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 10:04:54 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 10:04:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 06 Jun 2024 10:04:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Jun 2024 10:04:54 GMT
EXPOSE 9000
# Thu, 06 Jun 2024 10:04:54 GMT
CMD ["php-fpm"]
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV DRUPAL_VERSION=10.2.7
# Thu, 06 Jun 2024 10:04:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /opt/drupal
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014df3980fae18c782aea9d0723608f946d6d6e8f6125728c16633b2d972368c`  
		Last Modified: Wed, 29 May 2024 23:20:58 GMT  
		Size: 3.3 MB (3267768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336cedf37d159d49eef4060e02027c6d7a25eee6a23e0cebe098dd2df627e02c`  
		Last Modified: Wed, 29 May 2024 23:20:58 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c0de909185a283d5194786f7c61bf2d3fa30ebc0cff2e7d21c1258f445f6e5`  
		Last Modified: Wed, 29 May 2024 23:20:57 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a71e75d58af89d4139a522fc8379abc1953919607f8f220bf99685a8cbc754`  
		Last Modified: Thu, 06 Jun 2024 22:13:54 GMT  
		Size: 12.5 MB (12502043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f77eef839580c37001f2f4eb2aa92683348073fb53ae676169b8107e3e454d`  
		Last Modified: Thu, 06 Jun 2024 22:13:53 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849fa18ee89f788adb21e90f10027142c435213f73a36666e0630cbd6e5e4c93`  
		Last Modified: Thu, 06 Jun 2024 22:14:37 GMT  
		Size: 13.1 MB (13094990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aaf9cc74eb1ea117249e9ae38a17b55f70805eaa9cb385d7452167692c25882`  
		Last Modified: Thu, 06 Jun 2024 22:14:35 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde126975f49b8e634f3e093150d106de71d49cf02841ff2db5ab19d541c9ebc`  
		Last Modified: Thu, 06 Jun 2024 22:14:35 GMT  
		Size: 19.7 KB (19684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfa49915de6759bf0d550bedc8c7565f470a64f39a317531e4d72ebc1402bca`  
		Last Modified: Thu, 06 Jun 2024 22:14:35 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e3f3ce7df123161317de9956dc61b484b93d48eceb3b779ace1796a6df0387`  
		Last Modified: Fri, 07 Jun 2024 01:03:56 GMT  
		Size: 1.9 MB (1900564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f55269a799a9df56490051a70aa6a336113742090b670740156bf0ac26672f`  
		Last Modified: Fri, 07 Jun 2024 01:03:56 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844a1d6b9fe6284daee2c3f8f175188fc6dfe4f122d78cadf72a7a89ba418101`  
		Last Modified: Fri, 07 Jun 2024 01:03:56 GMT  
		Size: 724.7 KB (724732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2ba80250ef201764862c9cfbc0440b32e24f5da30360fb469269de7e592316`  
		Last Modified: Fri, 07 Jun 2024 01:03:56 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9c802fb70464dead32cc8fe052d2f18363a51e36e44e5353b4ce916e872e7f`  
		Last Modified: Fri, 07 Jun 2024 01:03:58 GMT  
		Size: 19.3 MB (19261854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:f1512fb35d264ac185a62cfda7fbc323bec688c5d5054700eceea82b565a4b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.9 KB (362870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99e78dad4910d23a76d181846ea87d25c8588cdef7b1fce0e76bf26f3ab4788`

```dockerfile
```

-	Layers:
	-	`sha256:f96f3ad47f5657a96e5eac3664fb6ffcc5bff5ceefa7666eb2c4d268044b877f`  
		Last Modified: Fri, 07 Jun 2024 01:03:56 GMT  
		Size: 330.4 KB (330365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3bae2d0cb45635eecf2fb15644c2a6df22ee9a2d26ea3f5712ce9ee070228ec`  
		Last Modified: Fri, 07 Jun 2024 01:03:56 GMT  
		Size: 32.5 KB (32505 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine3.20` - linux; arm variant v6

```console
$ docker pull drupal@sha256:22f79766470eabeb0a6ebf717370215a0dc55edc3d8ed8bc5e93556a890a0fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52445689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d93d6152985a6ffaf1046bcc65db32a37dd7671d65a4476c83e0951b80d5887`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:50:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 May 2024 21:50:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 29 May 2024 21:50:44 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 May 2024 21:50:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 May 2024 21:50:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 May 2024 21:50:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 21:50:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 21:50:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 29 May 2024 21:50:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_VERSION=8.3.8
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Jun 2024 10:04:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 10:04:54 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 10:04:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 06 Jun 2024 10:04:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Jun 2024 10:04:54 GMT
EXPOSE 9000
# Thu, 06 Jun 2024 10:04:54 GMT
CMD ["php-fpm"]
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV DRUPAL_VERSION=10.2.7
# Thu, 06 Jun 2024 10:04:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /opt/drupal
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fbde2bc87fb1211abfaa9d742eb1626779b6e008e3910fc9e86d002d2c18b4`  
		Last Modified: Wed, 29 May 2024 22:46:54 GMT  
		Size: 3.3 MB (3256537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3d57f281c14652f66f7ed738a118a66f8f9fe01923de337160db44abde6c2e`  
		Last Modified: Wed, 29 May 2024 22:46:53 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df4f95681943fb2de91ae5af31702772ccab2891b4971de5a53ad5b5f06489e`  
		Last Modified: Wed, 29 May 2024 22:46:53 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dc7aefb0eac807e49de2244d3d9e4f7fb19bdbecc911cb4cc81da790d966c2`  
		Last Modified: Thu, 06 Jun 2024 20:17:07 GMT  
		Size: 12.5 MB (12502047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8446b5ce6a6a6962922d97f76aded6f2a9f6c449f60fd19b4b4fb9fc84de69e`  
		Last Modified: Thu, 06 Jun 2024 20:17:05 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ba84b05b06c1db9eb6ef3e739a9c7db5b0a110c833adfc8b89e7da70f3c06f`  
		Last Modified: Thu, 06 Jun 2024 20:17:53 GMT  
		Size: 11.9 MB (11916585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d25c97b6ee475a99d2e89c104a0bacb10bf4cdb9e13462679f89d30703cbfd5`  
		Last Modified: Thu, 06 Jun 2024 20:17:50 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284ab16a605876efbed87052d86e2dfc111369f6d411c6eb491c20d7317e968d`  
		Last Modified: Thu, 06 Jun 2024 20:17:50 GMT  
		Size: 19.5 KB (19490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5463efb02b6a77d898207779ac3b8c0ef8de06987f2dc61fae306e8c60b708`  
		Last Modified: Thu, 06 Jun 2024 20:17:50 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8f21fc28ef994007f223e7048e547595bedb96cc0a99824b1910f685e413e2`  
		Last Modified: Thu, 06 Jun 2024 21:56:43 GMT  
		Size: 1.4 MB (1385012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ede098b309eaeccfcdc37d41e9fb63a9705e33645dfbff62d60a058d15384e`  
		Last Modified: Thu, 06 Jun 2024 21:56:43 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fca540b95936d0354c998eac808283dfe4c7db2b2a870bf0ecaabe681b7cfdf`  
		Last Modified: Thu, 06 Jun 2024 21:56:43 GMT  
		Size: 724.7 KB (724731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4e82ca7afcd154c660cccde35275ddfe5d7b6d68b1ce983bd38f71302030ed`  
		Last Modified: Thu, 06 Jun 2024 21:56:43 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4987514014641241bf77863544d370883501e9c5c0ef98c5c471773662c05f0`  
		Last Modified: Thu, 06 Jun 2024 22:00:47 GMT  
		Size: 19.3 MB (19262450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:b02d927e5b15ff76bcb1387d06794bf63aa1228213f7e5a549eea4368f6c275c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 KB (32428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4fe5d9c5856628758761c5427de1aa86f951ebc447a74dda9e520606f83094`

```dockerfile
```

-	Layers:
	-	`sha256:ccb4c483d87e29e28137f4aea1ee54685540b0e65412918693f5279b20c8c05b`  
		Last Modified: Thu, 06 Jun 2024 22:00:46 GMT  
		Size: 32.4 KB (32428 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine3.20` - linux; arm variant v7

```console
$ docker pull drupal@sha256:a34e3ed14de1b377f25e602701b8b3945ab0f9e9df5d4a91dea15564b04cc965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51138667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48ebd9cc7ac2f5456d0c20b57d3bddfe4f78cf8243a8dd28f645d91fbdad02d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 22:44:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 May 2024 22:44:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 29 May 2024 22:44:08 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 May 2024 22:44:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 May 2024 22:44:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 May 2024 22:44:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:44:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:44:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 29 May 2024 22:44:10 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_VERSION=8.3.8
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Jun 2024 10:04:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 10:04:54 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 10:04:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 06 Jun 2024 10:04:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Jun 2024 10:04:54 GMT
EXPOSE 9000
# Thu, 06 Jun 2024 10:04:54 GMT
CMD ["php-fpm"]
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV DRUPAL_VERSION=10.2.7
# Thu, 06 Jun 2024 10:04:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /opt/drupal
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b726d2ea6325cbe2918171017f17d1d12ab778e5c1d68d663b22b061790803e5`  
		Last Modified: Wed, 29 May 2024 23:37:27 GMT  
		Size: 3.1 MB (3069336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2825cd15ae946086782a856b1d53fadaac330d395b11caf35413766a5903ab25`  
		Last Modified: Wed, 29 May 2024 23:37:26 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ea0ff5951f7688d6fc2e3212eae4ff67224a3150942bba64e271e0e6878353`  
		Last Modified: Wed, 29 May 2024 23:37:25 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e731b6ca2aa3787756ab7092f8f29914b22c80a39d09d7f345bc7523a7c92b4d`  
		Last Modified: Thu, 06 Jun 2024 21:40:19 GMT  
		Size: 12.5 MB (12502051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a888b47c3a34f732c538085262156201e79d5fc96fc668f16335aa072b4dd7a4`  
		Last Modified: Thu, 06 Jun 2024 21:40:18 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96afe2588e27ed14da4631d5d872ec78f77fc424be62ffeb9e8645f8e0e4189`  
		Last Modified: Thu, 06 Jun 2024 21:41:02 GMT  
		Size: 11.2 MB (11178151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9df061d0996bdeb82ce9edc1ecf757faaff7e0ab9097d5f9fdbb5be63a1944`  
		Last Modified: Thu, 06 Jun 2024 21:40:59 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdaeeff983d9c21adaea951ba26f0f83f65d29ab8eac05ea97e23ee1d8edbd9`  
		Last Modified: Thu, 06 Jun 2024 21:40:59 GMT  
		Size: 19.5 KB (19484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f971aaf1ced399fe03eae9a173da6e42c68796d1bc7761adb4e9cd2a3db75e64`  
		Last Modified: Thu, 06 Jun 2024 21:40:59 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbdfdf65ceb8ef5d348899fc1cc9e62ac9574510668e87e928c2dc6bd6d2ab4`  
		Last Modified: Fri, 07 Jun 2024 02:38:49 GMT  
		Size: 1.3 MB (1275259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ad880811b220dca279212262859b836fb3094aa1659a61b06534d4cbf75268`  
		Last Modified: Fri, 07 Jun 2024 02:38:50 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d0766466e0427995a36e89fc7655e531502a579b307d11f500a7ab34b0454c`  
		Last Modified: Fri, 07 Jun 2024 02:38:50 GMT  
		Size: 724.7 KB (724731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0669a88f8a091baf0e748afc0d0461d7ae7e8dc293c8217d6858497b01d03dfd`  
		Last Modified: Fri, 07 Jun 2024 02:38:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab411b1d10f564c806f45aa65c436c4e2ccd545462b824963aeb7339d1088d6`  
		Last Modified: Fri, 07 Jun 2024 03:05:32 GMT  
		Size: 19.3 MB (19261832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:4c568aced7e000f7c9ebcd0326d76eb503434610bdbcd1d487ebd62d0f990bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.5 KB (360503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b83060368bda8c29dd8dfe8ed38571a8e892da5f0f3592a3c08f14b7c964460`

```dockerfile
```

-	Layers:
	-	`sha256:37fa6ab5a0a0853ce24656d54eef3279bc2602a74ac7943f8071afb38b7af822`  
		Last Modified: Fri, 07 Jun 2024 03:05:29 GMT  
		Size: 327.9 KB (327855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ef57bd97e877a22cdd738c881c49bff9f42bbc53c48ae395a7396fc74a049ee`  
		Last Modified: Fri, 07 Jun 2024 03:05:29 GMT  
		Size: 32.6 KB (32648 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:abf06bfcef8f94599e0629c405eb75b63512fb5f9e4aaf9cd8ebe11461a1e934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.3 MB (55255745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c9cf811303c9f5882887c52d8ebcae4405ffede0c27e4c3d37d3f96bd1246d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 22:24:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 May 2024 22:24:50 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 29 May 2024 22:24:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 May 2024 22:24:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 May 2024 22:24:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 May 2024 22:24:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:24:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:24:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 29 May 2024 22:24:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_VERSION=8.3.8
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Jun 2024 10:04:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 10:04:54 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 10:04:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 06 Jun 2024 10:04:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Jun 2024 10:04:54 GMT
EXPOSE 9000
# Thu, 06 Jun 2024 10:04:54 GMT
CMD ["php-fpm"]
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV DRUPAL_VERSION=10.2.7
# Thu, 06 Jun 2024 10:04:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /opt/drupal
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499c233d91e0b285ef0ee55a1f0788e53ee03c80e7d609f44dfb93d39b760d4b`  
		Last Modified: Wed, 29 May 2024 22:56:13 GMT  
		Size: 3.3 MB (3321187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d2271fbac7611742e70ef3cf276070acf7876e4bcb10f6841029eb4f88f0f9`  
		Last Modified: Wed, 29 May 2024 22:56:12 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9701985de31ecc58dfb2496e5353c355dc9587a81cddc0dc9043524261c37c5`  
		Last Modified: Wed, 29 May 2024 22:56:12 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b017580d96179a72fe9cda921f2f3cbd2418664143652182f7a5860cb2d718`  
		Last Modified: Thu, 06 Jun 2024 22:21:10 GMT  
		Size: 12.5 MB (12502044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9250b7b0b5c6cae59ab2c5ce4f5155916288e108aa80cb882bd9194d82cb3da7`  
		Last Modified: Thu, 06 Jun 2024 22:21:09 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1025e562d95afca5083f2da5b29abadf391d0babb607dfc79d08de669e0f58a`  
		Last Modified: Thu, 06 Jun 2024 22:21:51 GMT  
		Size: 13.1 MB (13148603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2712edf855253b89bab9da31a770c5c9dc544ff63a1829a8d0e4dd4d994d04dd`  
		Last Modified: Thu, 06 Jun 2024 22:21:49 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5280e580ddf3d733609ca1268fba565202212e5a89be26fd5e6f6315c8756eef`  
		Last Modified: Thu, 06 Jun 2024 22:21:49 GMT  
		Size: 19.5 KB (19470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd71b2c50df1b3b00c5b0dc32f5b7993d76432a9b0e2783c22c381d2ecbba1de`  
		Last Modified: Thu, 06 Jun 2024 22:21:49 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd9e80eee719d828074bc8d3783bc2f205da9596c4c95622bed45185564ef76`  
		Last Modified: Fri, 07 Jun 2024 03:11:03 GMT  
		Size: 2.2 MB (2177349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5798d1feceed00bcd37397fca012c95a273e6c88c0b5e406b8a3ca6987ac28e0`  
		Last Modified: Fri, 07 Jun 2024 03:11:03 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2421e7790a6445e817b8454f2a6f0418004e9486cac5c2c6b220bd2a853e8236`  
		Last Modified: Fri, 07 Jun 2024 03:11:04 GMT  
		Size: 724.7 KB (724731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903ad1e632effba6b8860c725cd471ff9dd08948dac198c7a9e83293d9e3d914`  
		Last Modified: Fri, 07 Jun 2024 03:11:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a198a49704133fc93a7a684a53b3d09042b15cd19d1e1519c832d7298fd13be5`  
		Last Modified: Fri, 07 Jun 2024 04:50:37 GMT  
		Size: 19.3 MB (19261792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:507105621aa8352ab6449293f01471dd1ef7224ed39b86e2df4fb029908905bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.7 KB (358709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f995ab91ab82bc05eb9cdb1a772357b78f5225ed29f0ec3594f377b82d76b3b3`

```dockerfile
```

-	Layers:
	-	`sha256:3016d4bfbcc70edbe23ba0d6ca0207dd985546a89d53e813d3b6e35012619ff6`  
		Last Modified: Fri, 07 Jun 2024 04:50:35 GMT  
		Size: 327.9 KB (327891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46cfc830345de11bb61b93c53f1552a743a89e94eba14db6deefe2b88d21e0df`  
		Last Modified: Fri, 07 Jun 2024 04:50:35 GMT  
		Size: 30.8 KB (30818 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine3.20` - linux; 386

```console
$ docker pull drupal@sha256:03e44755de39129570584ced1a0e4ee92889e42ac4abd2bee8d324b6ac352ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54694150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f77333b0e5b6c9beb9766b8580b7b9dc46bdcd1feb26875ababf609af4f38ec`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 22:27:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 May 2024 22:27:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 29 May 2024 22:27:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 May 2024 22:27:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 May 2024 22:27:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 May 2024 22:27:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:27:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:27:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 29 May 2024 22:27:11 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_VERSION=8.3.8
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Jun 2024 10:04:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 10:04:54 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 10:04:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 06 Jun 2024 10:04:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Jun 2024 10:04:54 GMT
EXPOSE 9000
# Thu, 06 Jun 2024 10:04:54 GMT
CMD ["php-fpm"]
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV DRUPAL_VERSION=10.2.7
# Thu, 06 Jun 2024 10:04:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /opt/drupal
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00308a417566819cf13e2fb7bf876f51ca8fbd112253d246127bbc33958111f1`  
		Last Modified: Thu, 30 May 2024 00:14:44 GMT  
		Size: 3.3 MB (3318570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7454942da668a8f495b1c84fba87d1e06bc62eaeeb69a615a9c479fa0c391`  
		Last Modified: Thu, 30 May 2024 00:14:43 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c8ef20ed4a8301005b92779aeca9a7af8e5e2ba027ea76bf0ef3c9a5c7e3d3`  
		Last Modified: Thu, 30 May 2024 00:14:43 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce3a84536471279b5b2ccc6f55b61cc73b9af21931f9ca0aaf056555da3d4e3`  
		Last Modified: Fri, 07 Jun 2024 00:09:06 GMT  
		Size: 12.5 MB (12502043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a236ef12c843e25c6ee3c8b43a662f4d2d780d07d305ad36f6cf718daf8bdab`  
		Last Modified: Fri, 07 Jun 2024 00:09:05 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9922d0bddcfd39b959ffa650d62752889cada3ffe8f5a90e381e971234ec0ea`  
		Last Modified: Fri, 07 Jun 2024 00:09:54 GMT  
		Size: 13.4 MB (13425109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f788682b6673f402f82e805954e4c5fda8b99a09cc7fa810bcca5be9ef72df`  
		Last Modified: Fri, 07 Jun 2024 00:09:51 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55338a8ddbe66629f7483fa217ed72abf056c0125b036c5ef193f832d3a12dca`  
		Last Modified: Fri, 07 Jun 2024 00:09:51 GMT  
		Size: 19.7 KB (19694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26fa351a001b8875e1cf3a04a156d109c07ba28e976d80b46428ceb928f41e8`  
		Last Modified: Fri, 07 Jun 2024 00:09:51 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159032cc036d7ae5fd5fa9b9173a27baac69371aa3a8ca44cb3fdddd690eb821`  
		Last Modified: Fri, 07 Jun 2024 01:57:06 GMT  
		Size: 2.0 MB (1961254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9f2f25023fc6ef22e42bd77c0a6b9d9a611ca5971b391a773a217cb99e3357`  
		Last Modified: Fri, 07 Jun 2024 01:57:06 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b817b8b3a25fb90f781f1473409415a9189c3fe693c27c5dbc43daa1da5ca17`  
		Last Modified: Fri, 07 Jun 2024 01:57:06 GMT  
		Size: 724.7 KB (724729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876a98f90758de44ed4545b540e8715c4aa0736712bf44dd1ee70a350cb06a5e`  
		Last Modified: Fri, 07 Jun 2024 01:57:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b7cc2b26fe4b275f584f1eca04de8c8b3b179d616633472fa964f063468ba0`  
		Last Modified: Fri, 07 Jun 2024 01:57:08 GMT  
		Size: 19.3 MB (19261856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:29d6ed8fb8cb66e38ef89c72a84bcd36ce68af5117300d83bd28903d2015fa31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.8 KB (362768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db668f65f93f3cfc44d5c12cdebeef21e122cc86ab4de8d2d3590a7cb5d6a08b`

```dockerfile
```

-	Layers:
	-	`sha256:70af02453a3733632229e0a80c3c98079456d1325d1c3a7597e10ebc76d3020c`  
		Last Modified: Fri, 07 Jun 2024 01:57:06 GMT  
		Size: 330.3 KB (330320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4562e5e5b735f76e2dcb0befc58fe31ab2f2bf1225ed92ce1cd797b4ef4abed2`  
		Last Modified: Fri, 07 Jun 2024 01:57:06 GMT  
		Size: 32.4 KB (32448 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine3.20` - linux; ppc64le

```console
$ docker pull drupal@sha256:07e4becbde99439ebc2fd9a8a5bdad187408efc932a9e6ad348c5d09c4d5e934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54757375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db24ff70286af3264eb8c4d625af386a5b897214d19e21326e3b83ad234c7b6d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 23:01:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 May 2024 23:01:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 29 May 2024 23:01:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 May 2024 23:01:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 May 2024 23:01:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 May 2024 23:01:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 23:01:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 23:01:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 29 May 2024 23:01:59 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_VERSION=8.3.8
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Jun 2024 10:04:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 10:04:54 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 10:04:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 06 Jun 2024 10:04:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Jun 2024 10:04:54 GMT
EXPOSE 9000
# Thu, 06 Jun 2024 10:04:54 GMT
CMD ["php-fpm"]
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV DRUPAL_VERSION=10.2.7
# Thu, 06 Jun 2024 10:04:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /opt/drupal
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e66b0d0146556fc91220949b5af15563e21b230bdaa3c9156ea6266199b48b`  
		Last Modified: Wed, 29 May 2024 23:50:37 GMT  
		Size: 3.4 MB (3395298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8756bd610d512641d28be2382de169df6603336d94be542bd8f86c973a2284d`  
		Last Modified: Wed, 29 May 2024 23:50:35 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d93c90e46e8ace79138019ef1d9c98710d4629fcc6a574f108b62323e9686a`  
		Last Modified: Wed, 29 May 2024 23:50:35 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e531ee4de7d0462d76f4140e9d37c79e42afa661eb5bbc79b0d259b7ea31b9fc`  
		Last Modified: Thu, 06 Jun 2024 21:29:30 GMT  
		Size: 12.5 MB (12502053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed58cf819c472c1f71635cefb2020273363c51d53ffea3187b3bb716d6e2997f`  
		Last Modified: Thu, 06 Jun 2024 21:29:29 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065bf8a6ff52cdd3a89af8b121e93ad868ce93d265b413d62f3d438f5e1fe418`  
		Last Modified: Thu, 06 Jun 2024 21:30:13 GMT  
		Size: 13.6 MB (13590982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5f4b3482c0cb65bb90941276663615ef0537c3a8258566bc085dfc4d0dd9ca`  
		Last Modified: Thu, 06 Jun 2024 21:30:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8432204a5355873ab809118a32663d14fff099b7c282dbe35506276c3a7d5e2`  
		Last Modified: Thu, 06 Jun 2024 21:30:10 GMT  
		Size: 19.5 KB (19476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69ff175e0f6efb8b7183bed64d501d8f88da80b95b9e031ef836a811cbf6d34`  
		Last Modified: Thu, 06 Jun 2024 21:30:10 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d46e0eb694823cd86beb4e00cc937248eced90004cc28db6d57750095321edf`  
		Last Modified: Fri, 07 Jun 2024 02:58:31 GMT  
		Size: 1.7 MB (1679507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee25ac618561598ef558208bcc355f31fa16785c3ece3065aff2eebf328e6a94`  
		Last Modified: Fri, 07 Jun 2024 02:58:31 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9d8eed0e5834de502bc2910fd002990acf7ff77b76172c3430e302b36437cb`  
		Last Modified: Fri, 07 Jun 2024 02:58:31 GMT  
		Size: 724.7 KB (724734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af032523fe4b397ff51dc737601c28b55f24f684bbd4ff3ea2f0988c7da74bd`  
		Last Modified: Fri, 07 Jun 2024 02:58:31 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b6d372969f5f887386c8c676f678a96b188ab6d331276707afd99a90236d05`  
		Last Modified: Fri, 07 Jun 2024 03:43:45 GMT  
		Size: 19.3 MB (19261689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:f459680e16969bbfdebae5f234cf3470e25edea9a15d4d7d469c6e4ba11796cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.2 KB (356184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9caa690bf485beb9e85e4d0bb1c7895b714494cf13fa43764acda853670e4c`

```dockerfile
```

-	Layers:
	-	`sha256:daf798cb9b355b5c93efe8d1469c5f323165f36d98cc4440605666b6c6191dbe`  
		Last Modified: Fri, 07 Jun 2024 03:43:45 GMT  
		Size: 325.9 KB (325891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b114f02e31f11b6b9ff38b2cc57ed620cfa3bb8e817b01837290c13a258358d0`  
		Last Modified: Fri, 07 Jun 2024 03:43:44 GMT  
		Size: 30.3 KB (30293 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine3.20` - linux; s390x

```console
$ docker pull drupal@sha256:a9883e51011197d4f3305b005ec996212bc339f1dc4b11f65ebbf83a9b5c7b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54099835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4bdbe914c8d8f204da27a938c73073ebc7da6a7aaa5b77697146ab1ace26ee`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 22:13:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 May 2024 22:13:57 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 29 May 2024 22:13:57 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 May 2024 22:13:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 May 2024 22:13:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 May 2024 22:13:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:13:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:13:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 29 May 2024 22:13:58 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_VERSION=8.3.8
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Jun 2024 10:04:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 10:04:54 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 10:04:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 06 Jun 2024 10:04:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Jun 2024 10:04:54 GMT
EXPOSE 9000
# Thu, 06 Jun 2024 10:04:54 GMT
CMD ["php-fpm"]
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV DRUPAL_VERSION=10.2.7
# Thu, 06 Jun 2024 10:04:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /opt/drupal
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e59aaf3957408d79830703dc723f179ea56d5e09b1b2358d2a1714ad397bd5f`  
		Last Modified: Wed, 29 May 2024 22:44:35 GMT  
		Size: 3.5 MB (3462557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4bd92d81aa824eaaf12fe4dc2b23834b92dfcb5f95ef3f980bbb78e812f400`  
		Last Modified: Wed, 29 May 2024 22:44:34 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4444860820a15536e66bf9ebb5b9ad505955c852e9a02a4a2aa1afae631eb1`  
		Last Modified: Wed, 29 May 2024 22:44:34 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8caf8029a2d88e6db05c03418f73061e7e27dd65a33326761fbbd2ff0db200`  
		Last Modified: Thu, 06 Jun 2024 22:01:35 GMT  
		Size: 12.5 MB (12502047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f656e043db443494857d3e119f8396e880cdec46fb485cc92a4f874086a914c`  
		Last Modified: Thu, 06 Jun 2024 22:01:34 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1715c1ab5aba997050c6fe5b85399b213c70df7338ec13459044d441c64b9d1`  
		Last Modified: Thu, 06 Jun 2024 22:02:06 GMT  
		Size: 13.1 MB (13058781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74373cf39089e70a1c1928c663d227325f7f799314b6d885df014cd41484789`  
		Last Modified: Thu, 06 Jun 2024 22:02:04 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b750054d25b2cf154b17ef42f91434c64479e7cb6fe468025368d43e847391`  
		Last Modified: Thu, 06 Jun 2024 22:02:04 GMT  
		Size: 19.5 KB (19482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa52651289581383cb3659d15b7885bef309a784003d5ea4c60242131281b45`  
		Last Modified: Thu, 06 Jun 2024 22:02:04 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d628f78287b46e4e7666c57dfc67d5dfebcb7af199be6f7fe5638b99824eb92a`  
		Last Modified: Fri, 07 Jun 2024 02:31:18 GMT  
		Size: 1.6 MB (1596437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce25b1bfc58dc12ace908fdc628f00f0ec00e9a4382082028fda4cf8b1d441e`  
		Last Modified: Fri, 07 Jun 2024 02:31:18 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1135cab434baaccb32e41fce2eed565f4324efc443b900ced5a8f671b44b8086`  
		Last Modified: Fri, 07 Jun 2024 02:31:18 GMT  
		Size: 724.7 KB (724732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a68a419befc76b2a41a377f226c9393cd396d862727ab7afbb076f95832145`  
		Last Modified: Fri, 07 Jun 2024 02:31:18 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bcf4e789c1c45cc582468dc5925ea94117fd762ae6fcc489d5027e9be02928`  
		Last Modified: Fri, 07 Jun 2024 03:02:54 GMT  
		Size: 19.3 MB (19261671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:6f203d894e7e46bc11cfa2baddb7a73b4b18eb96fb485ab81470033036ef2338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.1 KB (356055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be9d2cadd99a75520155463beac7cffadb894d924dc192a07cd165d5ec203b5`

```dockerfile
```

-	Layers:
	-	`sha256:7b852e1ae802b561ed352b3b86f68ab3a057d93245532b9e013534ccd5caa457`  
		Last Modified: Fri, 07 Jun 2024 03:02:53 GMT  
		Size: 325.8 KB (325833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe7eff0f5281191e25b14a915998bea0230d1459376f89053f7ce1ce42984aab`  
		Last Modified: Fri, 07 Jun 2024 03:02:53 GMT  
		Size: 30.2 KB (30222 bytes)  
		MIME: application/vnd.in-toto+json
