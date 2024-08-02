## `drupal:rc-fpm-alpine3.20`

```console
$ docker pull drupal@sha256:3a2a2b28d9c005a09eab76f9c478d2b521ea7810a45fa26b5e29f7ae0e12ff78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `drupal:rc-fpm-alpine3.20` - linux; amd64

```console
$ docker pull drupal@sha256:b4fe3e5038e8ccd1edc09c3ff3a476b839be4a30b64f32ff993279d320882975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53747488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc984867337a60a90b5f58f1a95e6c8b81b69e6f13cb7088c8d83fa35f3f8519`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 12 Jul 2024 03:27:25 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 12 Jul 2024 03:27:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Jul 2024 03:27:25 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_VERSION=8.2.21
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 12 Jul 2024 03:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Jul 2024 03:27:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Jul 2024 03:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 12 Jul 2024 03:27:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Jul 2024 03:27:25 GMT
EXPOSE 9000
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["php-fpm"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae0d9dfc4dada15e6a030ba7b9c9a3b16f9f5a7597a4d46ff24226e91b91db7`  
		Last Modified: Tue, 23 Jul 2024 03:55:04 GMT  
		Size: 3.3 MB (3272601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce295ca8623e5dc914104e970c5496db996db5f2abb336389bcbadd10465d21d`  
		Last Modified: Tue, 23 Jul 2024 03:55:03 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d3eb99f3c122bc8d6c22107602ed9c22fce771289b54bb2598142d1626f693`  
		Last Modified: Tue, 23 Jul 2024 03:55:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635d128c0149d90bf6bbcb68374d62ce105a32b887d578601aa6e7b832951332`  
		Last Modified: Tue, 23 Jul 2024 04:02:14 GMT  
		Size: 12.1 MB (12128103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fe58b8606cc2aac914e87f8692813b7730d574986a38fc967e4303f33d19c8`  
		Last Modified: Tue, 23 Jul 2024 04:02:13 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b7faae5cc87a3901fcef80dd34f41dc6d2c982374080ed3b289c5266131393`  
		Last Modified: Tue, 23 Jul 2024 04:02:37 GMT  
		Size: 12.9 MB (12864632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6684dca35c367fc188c759725c96a45fca0cc024d494305019d5065594371600`  
		Last Modified: Tue, 23 Jul 2024 04:02:35 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73658442ebe0c8dd02f493221a263ce0e60b4fa69c3052b63204140cad922cb8`  
		Last Modified: Tue, 23 Jul 2024 04:02:35 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed939a767db3984f698c00bf8783c05913cdb843e62711921b08be3863bfb29`  
		Last Modified: Tue, 23 Jul 2024 04:02:35 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1fd8ca8fef20703181296743abac4714a8ebb6f97d9612c4078fa98159f41d3`  
		Last Modified: Tue, 23 Jul 2024 07:18:47 GMT  
		Size: 1.9 MB (1897731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b7eebe31b8d2d5a516de693e07ae34d2663896b099eefeadab9190d731793a`  
		Last Modified: Tue, 23 Jul 2024 07:18:47 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfe659897e5c569ed44a5c077c739be8133b80ebd0e7a1d69885d6693144e1b`  
		Last Modified: Tue, 23 Jul 2024 07:18:47 GMT  
		Size: 726.3 KB (726332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e18f4bb6f3e495c524ad1e443da3fc5494e1e86aefb02961c604ab09711ebc`  
		Last Modified: Tue, 23 Jul 2024 07:18:47 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9387d6721839edff1c4a1a906e963b0f8b70368fb66373c343b9ac27655108ab`  
		Last Modified: Tue, 23 Jul 2024 07:18:48 GMT  
		Size: 19.2 MB (19201787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:cec9b0e991e1c0df479e8c5f9d9c3239727b6fa63b781f9ac0366891efcb0e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.1 KB (384077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c09aa2a4b7637629bd9f8a35be1efe1aa64e76158af07fbf547ce3348522fd`

```dockerfile
```

-	Layers:
	-	`sha256:b240417c613f16eccbaf2182d0964fddaa76f9953e85842d77c4bfa3e1d2697a`  
		Last Modified: Tue, 23 Jul 2024 07:18:47 GMT  
		Size: 350.1 KB (350131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93d17c03b7853eefef2d75ded3f383e70ea09df97b69ceb3a9bc21f501994243`  
		Last Modified: Tue, 23 Jul 2024 07:18:47 GMT  
		Size: 33.9 KB (33946 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-fpm-alpine3.20` - linux; arm variant v6

```console
$ docker pull drupal@sha256:419506ce94da8e30b473c4d08db4559dc5b90e9b73e20babd5acaddd4bdf5eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52267196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f00f2da67e140803da14ab640c148e969062448de30e1d87b613e58f2810f39`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 12 Jul 2024 03:27:25 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 12 Jul 2024 03:27:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Jul 2024 03:27:25 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_VERSION=8.2.22
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.22.tar.xz.asc
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_SHA256=8566229bc88ad1f4aadc10700ab5fbcec81587c748999d985f11cf3b745462df
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 12 Jul 2024 03:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Jul 2024 03:27:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Jul 2024 03:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 12 Jul 2024 03:27:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Jul 2024 03:27:25 GMT
EXPOSE 9000
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["php-fpm"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b041a1a670328abed5fe2b73e068aba477e969ddbfe65c606c8054a4c36067b2`  
		Last Modified: Tue, 23 Jul 2024 01:00:35 GMT  
		Size: 3.3 MB (3263638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51daa6109cd19af541c6fc2600ad5a2f2382e50d3938e2b51f30d24df583fee`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b57c8706e4f06f42a10294d5c9eef985613e48298dedb390c6e6816b60a8f78`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54378782a1f23617a5d40ab59b6f6247627b453d519d5346104a898fd0457cbf`  
		Last Modified: Thu, 01 Aug 2024 22:32:16 GMT  
		Size: 12.1 MB (12120803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257efc279eea16df6922fc972f944d533f067d468fe8fa50878b71a34333be48`  
		Last Modified: Thu, 01 Aug 2024 22:32:15 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b5653d15a831ee2a4b042e857d9aa61fcb491850e385b41b7e6bea83f7dba2`  
		Last Modified: Thu, 01 Aug 2024 22:32:40 GMT  
		Size: 12.2 MB (12174293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2df7e1d29952fb5354821e31034dba11ea16a4eafaea29b72a3dbbc32737d1`  
		Last Modified: Thu, 01 Aug 2024 22:32:38 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae730ea2087e6e4dc5c732cd707085fbf2af4e6fd06dd2cb333aada93e86638`  
		Last Modified: Thu, 01 Aug 2024 22:32:38 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f609b60ed9ac0a04dbf381ce60711ee8becfde6c2ee33ca91bf2c5248880fe7f`  
		Last Modified: Thu, 01 Aug 2024 22:32:38 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c46c24bc71fde8d8f0de72420ea520518a9587b40743c454bb754fe0f9afb5`  
		Last Modified: Thu, 01 Aug 2024 23:53:49 GMT  
		Size: 1.4 MB (1382258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b5639117867759b98207faee935e23f6609287121f777b483b066d81d3aba3`  
		Last Modified: Thu, 01 Aug 2024 23:53:48 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c6adbce7093ffd8c166e248ac626f98ddd303384370006f7025f2f68cd84a3`  
		Last Modified: Thu, 01 Aug 2024 23:53:49 GMT  
		Size: 726.3 KB (726334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9538623e0e0f86a9ffcdb482d1aa94cbd610005c31114797b4507f6fbbac27a`  
		Last Modified: Thu, 01 Aug 2024 23:53:49 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb74d30872b3a5e9c7bc2c0536f21586fea06bd2ec5a1e2eb03646b62bbb6fa`  
		Last Modified: Thu, 01 Aug 2024 23:53:50 GMT  
		Size: 19.2 MB (19201468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:c7c7822632023fc4d17fa1fae499b57c4b4a3f75da24589b622d6e413b4b1dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 KB (34023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e48d7fc24ba6bcf756451e0651cd282881c40c32ccae2f921c38c31516050b4`

```dockerfile
```

-	Layers:
	-	`sha256:32d60e7326b276acb2afafc3f31fe8607248955372142fd0c9d1296c1909b3cb`  
		Last Modified: Thu, 01 Aug 2024 23:53:46 GMT  
		Size: 34.0 KB (34023 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-fpm-alpine3.20` - linux; arm variant v7

```console
$ docker pull drupal@sha256:1e5bc1273d182c3c07c3ee90db8aeb842818a0f692a9b77bf20fda4d37ea8ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50925971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06cc84e21e563c4192201eaeb66697f964aca3621827de1d31da1151056f4c3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 12 Jul 2024 03:27:25 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 12 Jul 2024 03:27:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Jul 2024 03:27:25 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_VERSION=8.2.22
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.22.tar.xz.asc
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_SHA256=8566229bc88ad1f4aadc10700ab5fbcec81587c748999d985f11cf3b745462df
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 12 Jul 2024 03:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Jul 2024 03:27:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Jul 2024 03:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 12 Jul 2024 03:27:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Jul 2024 03:27:25 GMT
EXPOSE 9000
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["php-fpm"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57db3d4836535044109c42cf341df21ab1def6a06fecbaf98ffac833b47f15b`  
		Last Modified: Tue, 23 Jul 2024 01:14:20 GMT  
		Size: 3.1 MB (3073093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7991e70be4838afae3979e2bef4b2a7682dffac44793431e072ffbc9fc1686e5`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3967a6fef2cedd5f47096963a74875b542f5e4f6667543712aa16505b281dcf7`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180cacd553caf3105e2789da4e96b6baf6c08c56bc611414731c44b274a4a0bc`  
		Last Modified: Thu, 01 Aug 2024 22:47:21 GMT  
		Size: 12.1 MB (12120811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d072216e350e288ce6ae22b78c5e5c16625582cfbc6c595e467e413fda580bf4`  
		Last Modified: Thu, 01 Aug 2024 22:47:20 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4386b01c59f3b65dd0e40be63e7cab161b888470a10f952e1b8f8f7e6da87168`  
		Last Modified: Thu, 01 Aug 2024 22:47:44 GMT  
		Size: 11.4 MB (11402641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31443b9505643672cb6993dacb497e3e2fbd3dbc9386c404c413c96dcae2aac9`  
		Last Modified: Thu, 01 Aug 2024 22:47:42 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d76958aee596e88de26363a2088f0297b97ad374e1d70c774cb20257001ce39`  
		Last Modified: Thu, 01 Aug 2024 22:47:42 GMT  
		Size: 19.5 KB (19510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386d07e6df4c914defb485785b5c5d459815570afba6050393742c674642b6fb`  
		Last Modified: Thu, 01 Aug 2024 22:47:42 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fe73aa559ab12c31b64502d1946d55105a5b29cdd6c8e318ec2c79944ec776`  
		Last Modified: Fri, 02 Aug 2024 00:54:37 GMT  
		Size: 1.3 MB (1273266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7369aa657fe31fbb9711c23cd0a61577d1e8b569dab2eb3d45ef2beb5b5cd1be`  
		Last Modified: Fri, 02 Aug 2024 00:54:38 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3a93d3a27c15a9d5ce09bb43ba19445506248b0582b944c1725e187b92d6d4`  
		Last Modified: Fri, 02 Aug 2024 02:51:22 GMT  
		Size: 726.3 KB (726338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9486d547988726d5598d42ac25272ecfd30054b0f398b654af699b24c6da512`  
		Last Modified: Fri, 02 Aug 2024 02:51:21 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c11df5f48b308c864e8b293eb339b664dc496e5dc63e501918e9b0af2874e1b`  
		Last Modified: Fri, 02 Aug 2024 02:51:22 GMT  
		Size: 19.2 MB (19201634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:907697092a595344371438c7c7d6a47992392c32ef50ad7f27aba41ed17f78ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.6 KB (381609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0737ba82c4aebbf1e78857eaed35b533faf9c364a043c6e5e40fdb50b57c334`

```dockerfile
```

-	Layers:
	-	`sha256:4b0051a1338138618f5439209d08830bca33fe83610952feae9252ac3d97a187`  
		Last Modified: Fri, 02 Aug 2024 02:51:21 GMT  
		Size: 347.4 KB (347367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55f1c45ec803a89ebbec64cbbeffdf369c8aed56eae86727a7717d6abc82edb9`  
		Last Modified: Fri, 02 Aug 2024 02:51:21 GMT  
		Size: 34.2 KB (34242 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-fpm-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:d690b5150961450556264061194bb5a2832c487010d73322babe1523dcfc4466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55076053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2359c925ad9c52f2ebb510386c9bc99113c95a8a9860c6d4ef4dd0ee6ff0c812`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 12 Jul 2024 03:27:25 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 12 Jul 2024 03:27:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Jul 2024 03:27:25 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_VERSION=8.2.22
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.22.tar.xz.asc
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_SHA256=8566229bc88ad1f4aadc10700ab5fbcec81587c748999d985f11cf3b745462df
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 12 Jul 2024 03:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Jul 2024 03:27:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Jul 2024 03:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 12 Jul 2024 03:27:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Jul 2024 03:27:25 GMT
EXPOSE 9000
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["php-fpm"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f069fb86c015646c4497d6fa3beaf8bd3f9f04d8f77a1a865ff47fc9922c27e3`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 3.3 MB (3324720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298458c1fe168646ba7edf3e03804ff1a01f1fac6b41ef2a94ef5bf333311f2b`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f71c5e072e5141e780c5bbd4c1e2a34f9248a4b4a0983717a6c98be7560b899`  
		Last Modified: Tue, 23 Jul 2024 02:00:04 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901556881923d3ee3266136ed06b034383a9d38ad7d937c37381a7458a8125de`  
		Last Modified: Thu, 01 Aug 2024 22:47:38 GMT  
		Size: 12.1 MB (12120811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997a20a4d3113dce8effb585857f904c2bbcacae113abbc1cb5ffdb832f558d2`  
		Last Modified: Thu, 01 Aug 2024 22:47:37 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93aa54dbb64b8631459d1e79c6f62e87e0ea6acb8b611ccbaec572bd4f66f08b`  
		Last Modified: Thu, 01 Aug 2024 22:48:00 GMT  
		Size: 13.4 MB (13408538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9f97a2946a00a7a73c6bc8dc1635988a3f2bd17408a4bf00b3be52e1ce7528`  
		Last Modified: Thu, 01 Aug 2024 22:47:58 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb814eb8c1cd63a9da526dc8d0a7e6c0ee59f4721e19d6dea2b340b6a44df46`  
		Last Modified: Thu, 01 Aug 2024 22:47:58 GMT  
		Size: 19.5 KB (19495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c70069d52006c0db22bca449b277318f6e2ed628ef885153baf4cb4fa8e5767`  
		Last Modified: Thu, 01 Aug 2024 22:47:58 GMT  
		Size: 9.2 KB (9174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6573889c85d0bee782a556b149340d621fb27a7deeffc1fb7fa774f4ff1410e`  
		Last Modified: Fri, 02 Aug 2024 03:42:10 GMT  
		Size: 2.2 MB (2173871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581db0a7a8d9b53d7d48a81d9e8e75ccc54bd62c3006f1b1e3d8562f17c6f8c0`  
		Last Modified: Fri, 02 Aug 2024 03:42:10 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9375f75a5120a7f0de1358d94df5ed693fac8aa4f7adda03b6018a5d35e974ed`  
		Last Modified: Fri, 02 Aug 2024 05:22:07 GMT  
		Size: 726.3 KB (726343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c8d206a5344ec470c012cdc8b2e4eb47fea94e0373f7da77e9a63f694d7cc5`  
		Last Modified: Fri, 02 Aug 2024 05:22:07 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91764b6c51ddd37cd19f617b98e14c43a5a8add3416fa08a72b41e9617930f19`  
		Last Modified: Fri, 02 Aug 2024 05:22:08 GMT  
		Size: 19.2 MB (19201636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:adc527309edfc33ca3d8cf1a3356af3c4d27b413015051192628241b7ea077de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 KB (382208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ccdd46a4500048b02050aa4420ac77113aca901375879a9cc909ffc82ba249`

```dockerfile
```

-	Layers:
	-	`sha256:a9f77af6a8eafa46725a04dc78c4253c4cdc63e7789f1b11104f9d763c4c6a4e`  
		Last Modified: Fri, 02 Aug 2024 05:22:07 GMT  
		Size: 347.4 KB (347419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4f7fb02cc5c0451d6f57313897a7f41f73223d3ecf11c80ee85b14b52a68a79`  
		Last Modified: Fri, 02 Aug 2024 05:22:07 GMT  
		Size: 34.8 KB (34789 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-fpm-alpine3.20` - linux; 386

```console
$ docker pull drupal@sha256:d99fb7cb940b0b1380c4f67b4cf0a35aeced82603aac566a92cf6b10d6d0a881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54054073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c34d48e95ad80b992e2da49c8bd37b19898db1517f87d9e8141226fd5354fc`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 12 Jul 2024 03:27:25 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 12 Jul 2024 03:27:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Jul 2024 03:27:25 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_VERSION=8.2.21
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 12 Jul 2024 03:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Jul 2024 03:27:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Jul 2024 03:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 12 Jul 2024 03:27:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Jul 2024 03:27:25 GMT
EXPOSE 9000
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["php-fpm"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3702ede31b739c37f265c096aaa90041a249a222cf13f8141408974d1da345`  
		Last Modified: Tue, 23 Jul 2024 02:14:27 GMT  
		Size: 3.3 MB (3322587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd32fd053b31656313ffe5c4d6a711c2bdfbac32689ec3ed4eb1993c89d7c5cf`  
		Last Modified: Tue, 23 Jul 2024 02:14:26 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c734d1f76ba06cf1de68095cf88223f8aecf6242e60ae0985e4b555bd937308d`  
		Last Modified: Tue, 23 Jul 2024 02:14:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026eb322efcacb831c27011c0f90fd5920de0b2120c904655f7c7c02a98e884a`  
		Last Modified: Tue, 23 Jul 2024 02:22:14 GMT  
		Size: 12.1 MB (12128091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f907fb9c2f3b799862f22c94b1ead9391401132c0687ebb7f7651dfea4cf23d`  
		Last Modified: Tue, 23 Jul 2024 02:22:13 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1388c6bc98d51ab61804b1bb9b57fb687c42271d4cd3a88b01af2e5534e19c1`  
		Last Modified: Tue, 23 Jul 2024 02:22:40 GMT  
		Size: 13.2 MB (13216001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9821fd4a5c882f8f311347f174532e93295422f1d63b3c0b31160c28f696943`  
		Last Modified: Tue, 23 Jul 2024 02:22:37 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ccf650bb503ab4f6fd0024eee4474d320b032402471c780098d366e0262aa7`  
		Last Modified: Tue, 23 Jul 2024 02:22:37 GMT  
		Size: 19.7 KB (19700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f78bc73f2db98c5f356a48ae9ec2ac50578808e252494c754ea6454912cc7d`  
		Last Modified: Tue, 23 Jul 2024 02:22:37 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3771726e8c36c267ba0761d6d7e49325d12e96c126dcb4588e4607b8b635a66`  
		Last Modified: Tue, 23 Jul 2024 06:09:58 GMT  
		Size: 2.0 MB (1957785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65094bd7081de350be9f0792fd52e1e748f0db8a5170152e7f07c36b27c40c42`  
		Last Modified: Tue, 23 Jul 2024 06:09:58 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4782e71c9993bf0261b32b85f02bc73338c016c58e0baa4facf823da3ca1c4f`  
		Last Modified: Tue, 23 Jul 2024 06:09:58 GMT  
		Size: 726.3 KB (726333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecab36548cf6811a6b87f9c8da7f18d2c039f9edf88892ad596d2fdfc0beb99`  
		Last Modified: Tue, 23 Jul 2024 06:09:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c6d4c7750e61e6656b2bdb7514754d871b5e8b8b3ff9b7d13f54bbbc036a68`  
		Last Modified: Tue, 23 Jul 2024 06:09:59 GMT  
		Size: 19.2 MB (19201793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:df04e1caeecd786d9d65aa0ab428bdddac5a665695446f41597edbf503f4466a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.0 KB (384016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61094d6feb68f3ca8d39194ae19554cd8f279d832a002056af207c690b752f61`

```dockerfile
```

-	Layers:
	-	`sha256:74a59adeafbf34e189d232e751b287f39b53ccb523b6bb30bb62b13cfd20d4a4`  
		Last Modified: Tue, 23 Jul 2024 06:09:58 GMT  
		Size: 350.1 KB (350066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d365702276f9a4b42cf660c9d7b09f47aec9175a31778d41fb5e7e5f639fd880`  
		Last Modified: Tue, 23 Jul 2024 06:09:58 GMT  
		Size: 34.0 KB (33950 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-fpm-alpine3.20` - linux; ppc64le

```console
$ docker pull drupal@sha256:3a3762cb8161ed675d602a8f0cd6e7179d321978d74b62ff160a4801190fea4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54100556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94de794f5f12c2b40996433452f74ed5b808ce815c164f8cd20b2e051dd74cd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 12 Jul 2024 03:27:25 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 12 Jul 2024 03:27:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Jul 2024 03:27:25 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_VERSION=8.2.21
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 12 Jul 2024 03:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Jul 2024 03:27:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Jul 2024 03:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 12 Jul 2024 03:27:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Jul 2024 03:27:25 GMT
EXPOSE 9000
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["php-fpm"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3b3ac21bbea54c953ea1f2d18929d69c201c50acbb70a6157944a16d881644`  
		Last Modified: Mon, 22 Jul 2024 23:40:54 GMT  
		Size: 3.4 MB (3400973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ab89bd2c65997355b0f8d6c170e8ada77fc5d87ae04f4e525032aad1d1c519`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9ea05d06440c67793ed8359925d4dcf5e15c76e0e78b5d20fad34b553a253f`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d608da0b181d57e9570a699b449d18c04a8255e34520d2707efff0252029457`  
		Last Modified: Mon, 22 Jul 2024 23:48:01 GMT  
		Size: 12.1 MB (12128104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f293df01cfb4d63fcbc604bb535676a2d6ed21395af27420815a4966bbf4fbc9`  
		Last Modified: Mon, 22 Jul 2024 23:48:01 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c0ee6f4bd2e455ccd8c443a9a0a07d2c1528d12232ba4edc51481926296fa3`  
		Last Modified: Mon, 22 Jul 2024 23:48:25 GMT  
		Size: 13.4 MB (13359544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a7914c89760d1599fe07a2636efca208f73a3affb7c3487fd03abb52ac583a`  
		Last Modified: Mon, 22 Jul 2024 23:48:23 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7dd04fefd263b819d5702a93acb8fe8153097aa6b907b5b66f5c01ab50e3c6e`  
		Last Modified: Mon, 22 Jul 2024 23:48:22 GMT  
		Size: 19.5 KB (19483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e4b4e4573fc2e3c6182207ea0d7d654e73bbbdb6f8339353ea59f76064df96`  
		Last Modified: Mon, 22 Jul 2024 23:48:23 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44dc11501140a97015e50246069f1680bc2772c9c3f19dc8a9c0d2973a3eca05`  
		Last Modified: Wed, 24 Jul 2024 13:01:12 GMT  
		Size: 1.7 MB (1678883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc389c4d30181c30038c5d4158f7bba95ab0d93d76a4ffe2e60cdde552fe81f`  
		Last Modified: Wed, 24 Jul 2024 13:01:11 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e8ceeac0fa3476382eb7945298c2e08e6327a404e4b6dab3d19e3a0414b0b4`  
		Last Modified: Wed, 24 Jul 2024 13:01:12 GMT  
		Size: 726.3 KB (726347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd4fd8d55b2cf488fceef454d0d6ca44d27cc7ac0cc3e107a0d8a1a81bd6840`  
		Last Modified: Wed, 24 Jul 2024 13:01:12 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef88cd4d3390d5f15c1f91bc1e7a7d2387988b994f49da675296ac53796bb014`  
		Last Modified: Wed, 24 Jul 2024 13:01:13 GMT  
		Size: 19.2 MB (19201952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:30226a6936ea29d443e9baeb895710cb997904609c141f35f9a2cea21ef6cb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.6 KB (379555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e5eaf0779fc00a45d45c9593a79fb13c2cc0215be9289fa7eee01469fe713c`

```dockerfile
```

-	Layers:
	-	`sha256:af6b5e0adfe84761363aa657a3f741254c981d2607e4eb2b8740adcb36b4f61c`  
		Last Modified: Wed, 24 Jul 2024 13:01:11 GMT  
		Size: 345.4 KB (345395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29010033baaca039fdda8673b81127c780ae135e92999c0cdf30bf0d951c28ab`  
		Last Modified: Wed, 24 Jul 2024 13:01:11 GMT  
		Size: 34.2 KB (34160 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-fpm-alpine3.20` - linux; riscv64

```console
$ docker pull drupal@sha256:f0f6205461abb384f287dcae3fb497adeee46ac7f68b6787c17de1825951ebd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52556523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517162e79fc9a7e185bf6a812c8f6e83e7427abe3243106ff5e3ac3c3d09fb19`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 12 Jul 2024 03:27:25 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 12 Jul 2024 03:27:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Jul 2024 03:27:25 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_VERSION=8.2.22
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.22.tar.xz.asc
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_SHA256=8566229bc88ad1f4aadc10700ab5fbcec81587c748999d985f11cf3b745462df
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 12 Jul 2024 03:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Jul 2024 03:27:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Jul 2024 03:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 12 Jul 2024 03:27:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Jul 2024 03:27:25 GMT
EXPOSE 9000
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["php-fpm"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2d0e03d7a4d4766a64c04a50abfb02e217be153dd68888273b46568c4cac04`  
		Last Modified: Tue, 23 Jul 2024 12:29:02 GMT  
		Size: 3.4 MB (3397181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56268c2d820d6bf5bbf0e86c5bc55e50edc209a552c0844c6a9f787a880a2c6`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05d3b9188b0e4a61167b2493ce280347bad9dfe72e9ecf4c18c5572f2cb6719`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e2d9485d0a2716d7e24ddfd4cd99998480bc594d4435d34aa9faa254a91e8`  
		Last Modified: Fri, 02 Aug 2024 01:32:04 GMT  
		Size: 12.1 MB (12120806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6ec01bccd4f7ed959676eb7dc010e0bce387541308c7002b426daef6f4c993`  
		Last Modified: Fri, 02 Aug 2024 01:31:59 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d649a9c54a434d93bddaf3b707e62cb354f00c46ecaae84c4a871cdfca10d2f5`  
		Last Modified: Fri, 02 Aug 2024 01:32:52 GMT  
		Size: 12.2 MB (12225653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11720b3797eb494d5691af3a8a1d83c04567ee0261a1e6a2a030ecdf2f002ba`  
		Last Modified: Fri, 02 Aug 2024 01:32:41 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afbfc941da118624f03c70ca8260c0616613d1ea29be0bc23488bb9dd5fe53c`  
		Last Modified: Fri, 02 Aug 2024 01:32:41 GMT  
		Size: 19.5 KB (19494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a94cf69e546c51d1951c7815bb0322fa9428452a2134c76bab0042711476af8`  
		Last Modified: Fri, 02 Aug 2024 01:32:41 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c62586ee338265a7090585cb3f8b231427990fa5826412689c3214cd231fad`  
		Last Modified: Fri, 02 Aug 2024 04:57:46 GMT  
		Size: 1.5 MB (1480257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380debda5f03c116c810d6efc3a53c482778ef9bf039362a7c51c6e6694950c4`  
		Last Modified: Fri, 02 Aug 2024 04:57:46 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef413e64d8a0c454ba55854271f36afefbfac0f26e6d7b0065a4bba28d4efed0`  
		Last Modified: Fri, 02 Aug 2024 06:14:08 GMT  
		Size: 726.3 KB (726344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e715bf5f7039aceba175bafd1e554e4704be28c219f44f308851b7c3056a4a`  
		Last Modified: Fri, 02 Aug 2024 06:14:08 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d860957cbbc11e660d1d0b4d5c64c3473463f448875345b7cfc68b8dac3b53`  
		Last Modified: Fri, 02 Aug 2024 06:14:11 GMT  
		Size: 19.2 MB (19202393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:9df29c8e63f8c7e85ce7f6eb4483226a007ae7ace0e54f3de4df937d5b6fcf6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.6 KB (379551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32b846fd58f4b197b52f075891da7da6b4efc12ed7144931e66acb34a307ce9`

```dockerfile
```

-	Layers:
	-	`sha256:99b1cbc23f4b106406dd2d05059b2d7a72bbb0f10ff7fed6355a5c112ec0aff2`  
		Last Modified: Fri, 02 Aug 2024 06:14:08 GMT  
		Size: 345.4 KB (345391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fb766e7e8e3bca7e342d81f7bfbb1794ac8642d77c6c223138815623ed047b2`  
		Last Modified: Fri, 02 Aug 2024 06:14:07 GMT  
		Size: 34.2 KB (34160 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-fpm-alpine3.20` - linux; s390x

```console
$ docker pull drupal@sha256:e3946bc25e552e86eaaa43b90c51bc809b6a11d5bbf286b4d777ddc4159f82bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53444923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02604e3eb952affa6e97421477089bfab0f3b061076024956dd0ef31783fa772`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 12 Jul 2024 03:27:25 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 12 Jul 2024 03:27:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Jul 2024 03:27:25 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_VERSION=8.2.21
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 12 Jul 2024 03:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Jul 2024 03:27:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Jul 2024 03:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 12 Jul 2024 03:27:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Jul 2024 03:27:25 GMT
EXPOSE 9000
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["php-fpm"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bee85c5a5fc33ed0d0f61a077ed76c922b87c42c5cb3a4dbba408dd62a64def`  
		Last Modified: Tue, 23 Jul 2024 00:56:03 GMT  
		Size: 3.5 MB (3467756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1505ad7d669e91b715e2a1bc7ec0c52dd53433332ad45653571cbe2c3643d5`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d87c5417e12df9b44287d4f554dd37d0b5b446d100409e5c49a17ac509a5b2`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374940251c96227ae3adf2bad443c359a20ef5321e9057bf683d253fba1d2630`  
		Last Modified: Tue, 23 Jul 2024 01:01:38 GMT  
		Size: 12.1 MB (12128089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8ebb7abac7a24e2d8fb7944fe87e80186ab315c98d78b9409850c9e8147ba0`  
		Last Modified: Tue, 23 Jul 2024 01:01:36 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba79bc740af05e09acf16941d7ef4a728915e1c43257f3f14c79939eea1fa1ec`  
		Last Modified: Tue, 23 Jul 2024 01:01:57 GMT  
		Size: 12.8 MB (12832054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0baeb056dd2eb9a7f9e06347347013c1ba245213d1ccf11810442f70ed48fd64`  
		Last Modified: Tue, 23 Jul 2024 01:01:55 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a52cbd190580caf51802be5413ba0862b22e590e72794e2076d419f856e5f3`  
		Last Modified: Tue, 23 Jul 2024 01:01:55 GMT  
		Size: 19.5 KB (19486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444cca5cdd7c1269939ba68597f6bbd5a1106cb7007ed1759cd7d1fe8f9d7c81`  
		Last Modified: Tue, 23 Jul 2024 01:01:55 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be56f8cf38a7f347ee8fe083241e5766ec401798caea190e28b27dcf7873196`  
		Last Modified: Wed, 24 Jul 2024 12:42:49 GMT  
		Size: 1.6 MB (1594847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b3fc7e6566d04c020a7349d7d5281ae62346d4175259b647e01ef313073280`  
		Last Modified: Wed, 24 Jul 2024 12:42:49 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45399380ba330c38dec64a69b52f0fb5c7a59b69b68909fc7ba6044a3f600bf7`  
		Last Modified: Wed, 24 Jul 2024 12:42:49 GMT  
		Size: 726.3 KB (726337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822acb47f39499818fc5a9790c9bd8ec24ca75a7b7f0496441aa84c3d4e0d273`  
		Last Modified: Wed, 24 Jul 2024 12:42:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfbd87aae813cb2ca4f2b4c89c7c905c377ac5a827c089b9413a89f4134e4a1`  
		Last Modified: Wed, 24 Jul 2024 12:42:51 GMT  
		Size: 19.2 MB (19201575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:06c21a4c21bea9a5fbe20abd39985d17003bd70126131c5e44331a9f15a9d57d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.4 KB (379373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48f5cb0cbb14c7ce67f14c39bfb548c104b905fd5cd7419d2e80c5e40f83b88`

```dockerfile
```

-	Layers:
	-	`sha256:307820c5827a17fc7e745597a2df9850e0093243bdb536377d150a41563f0de8`  
		Last Modified: Wed, 24 Jul 2024 12:42:49 GMT  
		Size: 345.3 KB (345313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c76b6da02e1b2bfdd69afa892b6d3852173f72d961f63c9eed4c8f43f9be88ca`  
		Last Modified: Wed, 24 Jul 2024 12:42:49 GMT  
		Size: 34.1 KB (34060 bytes)  
		MIME: application/vnd.in-toto+json
