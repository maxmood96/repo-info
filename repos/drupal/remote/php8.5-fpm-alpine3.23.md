## `drupal:php8.5-fpm-alpine3.23`

```console
$ docker pull drupal@sha256:bd69f0c569b3ec959fd00b3e07d22ddcc352528bb1cc0ab28dfed760ab5d90dd
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

### `drupal:php8.5-fpm-alpine3.23` - linux; amd64

```console
$ docker pull drupal@sha256:6f4f108bda4d004884cbdceba44f6b9b51e3db547d913d4c09f32e473fdca9e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68217134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a01444ad5f7ac503ac2cd7b3f544205a40a7a9d8ea8d6a77da7a33583eb3ed`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jun 2026 19:46:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 22 Jun 2026 19:46:37 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 22 Jun 2026 19:46:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jun 2026 19:46:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 22 Jun 2026 19:46:37 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:46:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:46:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jun 2026 19:46:37 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 22 Jun 2026 19:46:37 GMT
ENV PHP_VERSION=8.5.7
# Mon, 22 Jun 2026 19:46:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Mon, 22 Jun 2026 19:46:37 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Mon, 22 Jun 2026 19:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 22 Jun 2026 19:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:49:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 22 Jun 2026 19:49:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:49:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 22 Jun 2026 19:49:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 22 Jun 2026 19:49:45 GMT
WORKDIR /var/www/html
# Mon, 22 Jun 2026 19:49:45 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 22 Jun 2026 19:49:45 GMT
STOPSIGNAL SIGQUIT
# Mon, 22 Jun 2026 19:49:45 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 22 Jun 2026 19:49:45 GMT
CMD ["php-fpm"]
# Thu, 25 Jun 2026 01:23:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 25 Jun 2026 01:23:51 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 25 Jun 2026 01:23:51 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 01:23:51 GMT
ENV DRUPAL_VERSION=11.3.13
# Thu, 25 Jun 2026 01:23:51 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 25 Jun 2026 01:23:51 GMT
WORKDIR /opt/drupal
# Thu, 25 Jun 2026 01:24:02 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 25 Jun 2026 01:24:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a23b72a186cc0b35a47843cb3eb0de3092816ebc3de5e1b274f72fcfa83d78d`  
		Last Modified: Mon, 22 Jun 2026 19:49:51 GMT  
		Size: 3.5 MB (3465276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dd9fad8c5d342665ff2d14ff279bce72a0a4b9fc3aa6f6750b27513fa97641`  
		Last Modified: Mon, 22 Jun 2026 19:49:51 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c5d783984eced39c1ef2862b21787e3c760c098239da114abc8058632ddbcc`  
		Last Modified: Mon, 22 Jun 2026 19:49:51 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893f9131848fdcf163e6f222d7924eb620a139d941282df213575e05f6af2102`  
		Last Modified: Mon, 22 Jun 2026 19:49:52 GMT  
		Size: 14.4 MB (14421098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8ae1a44236fbbc0dce197cbde9e3e644c36b1b76f9b952594ed92c339d246f`  
		Last Modified: Mon, 22 Jun 2026 19:49:52 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6fcd791f7fd3b71abeddea409d1f8f0762205ea5051c284f4b472ad844b650`  
		Last Modified: Mon, 22 Jun 2026 19:49:53 GMT  
		Size: 16.8 MB (16794204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85da6361379631be27a79e34fc5ce7e140e4607681fa45adaa62c831eb8294ea`  
		Last Modified: Mon, 22 Jun 2026 19:49:53 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151ece48701b3c31e9f79e4170cf0fe0593cae06bc425aec1dcec8f9e643ce8d`  
		Last Modified: Mon, 22 Jun 2026 19:49:53 GMT  
		Size: 22.3 KB (22315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0e96d2f940992a56b6711b99d4ca84d2b0208ae62529821a37c3523ae9efbc`  
		Last Modified: Mon, 22 Jun 2026 19:49:54 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b9f2bbe3239363d3c02b132de35783d34d9d1fa922b8c5f7a969491c0c72ed`  
		Last Modified: Thu, 25 Jun 2026 01:24:15 GMT  
		Size: 7.4 MB (7426491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c9d8506de49f962a9d27a572bf936431712432acd0ff18aea08a913bf6cff9`  
		Last Modified: Thu, 25 Jun 2026 01:24:14 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed28b92da4f1f6cf7cdc033d1fe58d641942d00e8e5a61a9168625e76d2f7ce1`  
		Last Modified: Thu, 25 Jun 2026 01:24:15 GMT  
		Size: 823.3 KB (823336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c58a1a27c75046cb7789474f328764c30b63c8b4cbad3979d5d5fad38db7ce3`  
		Last Modified: Thu, 25 Jun 2026 01:24:14 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b1a66b500a392978ddf776ca3416f4ef4a28452ee1af11a1767224a020a54e`  
		Last Modified: Thu, 25 Jun 2026 01:24:16 GMT  
		Size: 21.4 MB (21406189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.23` - unknown; unknown

```console
$ docker pull drupal@sha256:cf3daee1a85bcdacde3bda0e0fdbeb447bf40e0227531374f8f60f2cf9b4109e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.3 KB (401252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31cdd516b9d3c36c105b7fec636b2ff48b1b4750b2ab32a7fd6149c0b5fa0e8c`

```dockerfile
```

-	Layers:
	-	`sha256:d2d30019502ed807fe8c669c88a5e352e7d7d0d17c08c74fc387dae8e22fb188`  
		Last Modified: Thu, 25 Jun 2026 01:24:14 GMT  
		Size: 368.8 KB (368824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55dfb51c1f6008142f13a9acec283eff378e77e9cb8396132acba888efd3d79c`  
		Last Modified: Thu, 25 Jun 2026 01:24:14 GMT  
		Size: 32.4 KB (32428 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.23` - linux; arm variant v6

```console
$ docker pull drupal@sha256:0205e704efa2a14d1e0fa84696393a7741c1d4021664c0f2597e6feb504500b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63094265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:203bb74b00acad2f231f90edb9d765ea19e17a38b8dc2a3e48103c1c1d9c57b6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jun 2026 19:46:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 22 Jun 2026 19:46:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 22 Jun 2026 19:46:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jun 2026 19:46:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 22 Jun 2026 19:46:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:46:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:46:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jun 2026 19:46:10 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 22 Jun 2026 19:46:10 GMT
ENV PHP_VERSION=8.5.7
# Mon, 22 Jun 2026 19:46:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Mon, 22 Jun 2026 19:46:10 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Mon, 22 Jun 2026 19:46:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 22 Jun 2026 19:46:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:49:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 22 Jun 2026 19:49:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 22 Jun 2026 19:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 22 Jun 2026 19:49:32 GMT
WORKDIR /var/www/html
# Mon, 22 Jun 2026 19:49:32 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 22 Jun 2026 19:49:32 GMT
STOPSIGNAL SIGQUIT
# Mon, 22 Jun 2026 19:49:32 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 22 Jun 2026 19:49:32 GMT
CMD ["php-fpm"]
# Thu, 25 Jun 2026 01:26:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 25 Jun 2026 01:26:06 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 25 Jun 2026 01:26:06 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 01:26:06 GMT
ENV DRUPAL_VERSION=11.3.13
# Thu, 25 Jun 2026 01:26:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 25 Jun 2026 01:26:06 GMT
WORKDIR /opt/drupal
# Thu, 25 Jun 2026 01:26:20 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 25 Jun 2026 01:26:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5c1329d7635a097d0990571b83f3fcdfa1b424cb65d5c83cf4fd7bcf4889c3`  
		Last Modified: Mon, 22 Jun 2026 19:49:38 GMT  
		Size: 3.4 MB (3419497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728dfc03b09b66d26f07b1a270ddef20fa7485dc3f0ed2ae091dd088906e36d1`  
		Last Modified: Mon, 22 Jun 2026 19:49:38 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc132c98f7e9376f16fdeeee9e076f7c5d73bc8ce0b3ec9253f1e3d6b05a878`  
		Last Modified: Mon, 22 Jun 2026 19:49:37 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc8cc7d911685f85ea7d559a1ac49f31ea73df91d33b544110a009035257d01`  
		Last Modified: Mon, 22 Jun 2026 19:49:38 GMT  
		Size: 14.4 MB (14421119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfd05a75b4239d617f9a42e0a3108467d2a4c47b84e991bf46e5170bcfbcf9c`  
		Last Modified: Mon, 22 Jun 2026 19:49:39 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb12094b462f4e721818571fadf9ee67b559bf1704814066e5f1e949658cb00`  
		Last Modified: Mon, 22 Jun 2026 19:49:39 GMT  
		Size: 14.7 MB (14686160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9b11642786599fa3beb6a849bcff4ea9593ef25fbbb8b05a8173f0a45e12c0`  
		Last Modified: Mon, 22 Jun 2026 19:49:39 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2df1f85be29b408d8369bd8531ff70d4f97508c0969d1952a0ac26e6d8e240`  
		Last Modified: Mon, 22 Jun 2026 19:49:40 GMT  
		Size: 22.1 KB (22133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0949456d9358953cde5d0ece57c1b363943eadc418144deb6c0a9d7dea740500`  
		Last Modified: Mon, 22 Jun 2026 19:49:41 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587a3f072e14cd9c0c958c286faeb35b4b1cb33bd6bea2d595379243ffff0dbe`  
		Last Modified: Thu, 25 Jun 2026 01:26:28 GMT  
		Size: 4.7 MB (4749282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3faddde033a58fb4e8a37a415c327127827c75042caa72768474c363cbbe5261`  
		Last Modified: Thu, 25 Jun 2026 01:26:27 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f54bf6a388ab24d084784e3e51524098f17d84e1a5f3639e7aad09559322273`  
		Last Modified: Thu, 25 Jun 2026 01:26:28 GMT  
		Size: 823.3 KB (823338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9aa380de864b68b646b277f4f21d3a55ab65066a8ec2e40f2c000375573d09d`  
		Last Modified: Thu, 25 Jun 2026 01:26:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d6b3b446ca65488ea120f8cccad92c22b1757889790171450687b86f5615ac`  
		Last Modified: Thu, 25 Jun 2026 01:26:30 GMT  
		Size: 21.4 MB (21406339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.23` - unknown; unknown

```console
$ docker pull drupal@sha256:459827635249a24aceec7b70f9c076e7d8cc7855f1f2da9793a6d4ec943de024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 KB (32341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1350da697f66122c1e4755fb726f988380b16db84899b9aa0b2fc454b573d2b1`

```dockerfile
```

-	Layers:
	-	`sha256:48cc5b4a07780695bbd36c1445a35bfa86ef9bc60e92471ee0545618d53ba4d1`  
		Last Modified: Thu, 25 Jun 2026 01:26:27 GMT  
		Size: 32.3 KB (32341 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.23` - linux; arm variant v7

```console
$ docker pull drupal@sha256:7b41f55ebe0b90a8488568307a6dd8ea4780d26b767e6d1ff5fe08a4e628a355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62636052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ce3642f8f16ae078595c77c3bfbf0f0a5c8f71a86ddb1d0291b27f59091bde`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:18 GMT
ADD alpine-minirootfs-3.23.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:18 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jun 2026 19:55:44 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 22 Jun 2026 19:55:44 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 22 Jun 2026 19:55:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jun 2026 19:55:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 22 Jun 2026 19:55:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:55:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:55:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jun 2026 19:55:44 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 22 Jun 2026 19:55:44 GMT
ENV PHP_VERSION=8.5.7
# Mon, 22 Jun 2026 19:55:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Mon, 22 Jun 2026 19:55:44 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Mon, 22 Jun 2026 19:55:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 22 Jun 2026 19:55:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:59:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 22 Jun 2026 19:59:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:59:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 22 Jun 2026 19:59:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 22 Jun 2026 19:59:02 GMT
WORKDIR /var/www/html
# Mon, 22 Jun 2026 19:59:02 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 22 Jun 2026 19:59:02 GMT
STOPSIGNAL SIGQUIT
# Mon, 22 Jun 2026 19:59:02 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 22 Jun 2026 19:59:02 GMT
CMD ["php-fpm"]
# Thu, 25 Jun 2026 01:38:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 25 Jun 2026 01:38:48 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 25 Jun 2026 01:38:48 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 01:38:48 GMT
ENV DRUPAL_VERSION=11.3.13
# Thu, 25 Jun 2026 01:38:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 25 Jun 2026 01:38:48 GMT
WORKDIR /opt/drupal
# Thu, 25 Jun 2026 01:39:00 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 25 Jun 2026 01:39:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:177f8e1e6f831989320cf2b59b7eabd21cbf36804c79506912f3a81caff426f2`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcafe990a6cd59758b22d6c2df7ae56442e2f5c0c1e99cdfff027ba5cebab3a`  
		Last Modified: Mon, 22 Jun 2026 19:59:09 GMT  
		Size: 3.2 MB (3229682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845f5c0536d02c235717a7e0e2d666192691ac823def1fb7c890519499cc7c9a`  
		Last Modified: Mon, 22 Jun 2026 19:59:09 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63ed9d84d9c65bad0db65d5985632756094c7b535177f1a2720085d05eee418`  
		Last Modified: Mon, 22 Jun 2026 19:59:09 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35556beb832d839169b97d09fb864dce26d503eb11ecb064474f347cadb5381a`  
		Last Modified: Mon, 22 Jun 2026 19:59:09 GMT  
		Size: 14.4 MB (14421136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1a20816b4e5830ccc0d3b60878dc0ea5821ecd470d0008782b95d6920754a7`  
		Last Modified: Mon, 22 Jun 2026 19:59:10 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1effb3f195583ff0476f5771420308d5a44d5fefceca7e92c0b03a8aaaba0c2a`  
		Last Modified: Mon, 22 Jun 2026 19:59:11 GMT  
		Size: 13.9 MB (13880088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6cf89346f4e465720aac992873a1d8cfbe853c6216182d7c89afa472de86db`  
		Last Modified: Mon, 22 Jun 2026 19:59:11 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bb3686729a271cbd0e13d2ec6245862f2c2e02f23bcd54229dfedb36f1e93c`  
		Last Modified: Mon, 22 Jun 2026 19:59:11 GMT  
		Size: 22.1 KB (22139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4797cddcbdd862d43a9a03d0e6c1f9e8762d604394db016502dfef4b0f4433`  
		Last Modified: Mon, 22 Jun 2026 19:59:11 GMT  
		Size: 9.3 KB (9263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736357bfe58a79bd381e5c25c659803339e895515da9ab1fd1c457a3da8af4dd`  
		Last Modified: Thu, 25 Jun 2026 01:39:14 GMT  
		Size: 5.6 MB (5577855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0641b97eca266bc985f271196b108507b5284bd3d883c295893b8be15a64e04`  
		Last Modified: Thu, 25 Jun 2026 01:39:14 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2655d8e3d4924f7c7be610c8b62fff7a6141fa376c7b3d92087e146eae8b617`  
		Last Modified: Thu, 25 Jun 2026 01:39:14 GMT  
		Size: 823.3 KB (823338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42716af54d25bdb2c2e958a36f224de9515193ccb8a18df158a8c57b793255d3`  
		Last Modified: Thu, 25 Jun 2026 01:39:14 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c445f1e96c5c332d2d43ef0d2272460aa602237352d9b172e91df0081b9099`  
		Last Modified: Thu, 25 Jun 2026 01:39:16 GMT  
		Size: 21.4 MB (21406156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.23` - unknown; unknown

```console
$ docker pull drupal@sha256:cacc56eef958f11c3d19b3a569dc09a9f5feb7cfc9446502b20c29c46127e9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.8 KB (400766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9399d1d828d9798add27bd37f90ff68f0ce9e8294839c792c5befa79e70aa75`

```dockerfile
```

-	Layers:
	-	`sha256:eee1d56721192f0cbc86048ded8565858676b336b5b415f5d0d3940eaaeab04e`  
		Last Modified: Thu, 25 Jun 2026 01:39:13 GMT  
		Size: 368.2 KB (368210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82b15f7834be399973464e4cb182820260cd11414e4b58d2a400d1aa6b2d1339`  
		Last Modified: Thu, 25 Jun 2026 01:39:13 GMT  
		Size: 32.6 KB (32556 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:65b0a949c1e5ee251d94c3d83a14725f71752565d1096d1be4d9331a2c7321ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67742264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca34925364e300175c47c076e42fb827e292e2244fdbcc3373892ebe3b491b2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:47:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jun 2026 19:47:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 22 Jun 2026 19:47:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 22 Jun 2026 19:47:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jun 2026 19:47:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 22 Jun 2026 19:47:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:47:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:47:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jun 2026 19:47:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 22 Jun 2026 19:47:24 GMT
ENV PHP_VERSION=8.5.7
# Mon, 22 Jun 2026 19:47:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Mon, 22 Jun 2026 19:47:24 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Mon, 22 Jun 2026 19:47:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 22 Jun 2026 19:47:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:50:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 22 Jun 2026 19:50:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:50:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 22 Jun 2026 19:50:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 22 Jun 2026 19:50:46 GMT
WORKDIR /var/www/html
# Mon, 22 Jun 2026 19:50:46 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 22 Jun 2026 19:50:46 GMT
STOPSIGNAL SIGQUIT
# Mon, 22 Jun 2026 19:50:46 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 22 Jun 2026 19:50:46 GMT
CMD ["php-fpm"]
# Thu, 25 Jun 2026 01:24:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 25 Jun 2026 01:24:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 25 Jun 2026 01:24:46 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 01:24:46 GMT
ENV DRUPAL_VERSION=11.3.13
# Thu, 25 Jun 2026 01:24:46 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 25 Jun 2026 01:24:46 GMT
WORKDIR /opt/drupal
# Thu, 25 Jun 2026 01:24:57 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 25 Jun 2026 01:24:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2a2b8d44a012f6032e5ffe3fb985a4f936c0c866f2395da59500b74fdd545c`  
		Last Modified: Mon, 22 Jun 2026 19:50:53 GMT  
		Size: 3.5 MB (3476742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ad90e9e21c85e86854d697435d341321994b4a02dc27d10a0a5bac6f74b0fe`  
		Last Modified: Mon, 22 Jun 2026 19:50:53 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ad0b0b0335f61bdba5148552351f81fc75c9cca6f06c42ae551a1ef713de1f`  
		Last Modified: Mon, 22 Jun 2026 19:50:53 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b19c4ca6579c3a662f3d799261b809ab9569e3cb9281eeb3c6794cc271184b3`  
		Last Modified: Mon, 22 Jun 2026 19:50:54 GMT  
		Size: 14.4 MB (14421106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618e557cff32b9381b55b018e18934e3ad260a86283d3c3fc078c43576304a65`  
		Last Modified: Mon, 22 Jun 2026 19:50:55 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cebffb9546c36233e1d4051abd1ffd1e4e33e1144c3f59251b4738f80337532`  
		Last Modified: Mon, 22 Jun 2026 19:50:55 GMT  
		Size: 16.2 MB (16200647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8362a8cb46e3a9e24016337db5329322524942633ddd43d583dff62dd8cd6c8`  
		Last Modified: Mon, 22 Jun 2026 19:50:55 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d111860088fa02380c73bdb9f1cabcb508e0c258dacea94e483cbdc7dfb5d82c`  
		Last Modified: Mon, 22 Jun 2026 19:50:55 GMT  
		Size: 22.1 KB (22130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e054b137afd9ed5d0a656a1555dff519527866bdde0d606dd70b6e347ba614f5`  
		Last Modified: Mon, 22 Jun 2026 19:50:56 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58d4b00ab3034735e20abb2703363aaeb1c0197d638a0d5e4a939bcb9846c06`  
		Last Modified: Thu, 25 Jun 2026 01:25:11 GMT  
		Size: 7.2 MB (7196472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cef294412870b334d0e4c1b6a1bce8fddbf51781a76ccbfb9aca778a77fe664`  
		Last Modified: Thu, 25 Jun 2026 01:25:10 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7651fd9efd5cd0f2a37160b2bde88c6e329ba71e8e8defbfa246963dd104afe`  
		Last Modified: Thu, 25 Jun 2026 01:25:10 GMT  
		Size: 823.3 KB (823337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced7f7249390d932b60648c1f3199c6272f5cdc223e009fa855c417a7e0ffcca`  
		Last Modified: Thu, 25 Jun 2026 01:25:10 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01027de8764611df3980503d076ff8857c7e7e9a52a325f15337e4216a916bdc`  
		Last Modified: Thu, 25 Jun 2026 01:25:12 GMT  
		Size: 21.4 MB (21406170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.23` - unknown; unknown

```console
$ docker pull drupal@sha256:4a41badb592a6d7fd9054f23e3ec25362ad3ada616f547f5798f9595d35a5f0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.8 KB (400818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4deee81f3f064c87bd1b033d0154726c222f49922250dfc45770976303c533`

```dockerfile
```

-	Layers:
	-	`sha256:c5bff55d519922efc632a15512aa49fc6d72125d34d23aca4ceee6b6cc414f9f`  
		Last Modified: Thu, 25 Jun 2026 01:25:10 GMT  
		Size: 368.2 KB (368230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6e1737ed2314f739297ef16fcef3f83eca677edd055b71bf5de6eaa8f374bb`  
		Last Modified: Thu, 25 Jun 2026 01:25:10 GMT  
		Size: 32.6 KB (32588 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.23` - linux; 386

```console
$ docker pull drupal@sha256:27fe43bbb9caea87ac5574882a74c6744ed9f5cb70f481796ee830a191f12976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67314044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbd8cff0e82ccebd04671baf258f3fc1a5be9019a0492435fc040e46672fd71`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jun 2026 19:46:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 22 Jun 2026 19:46:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 22 Jun 2026 19:46:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jun 2026 19:46:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 22 Jun 2026 19:46:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:46:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:46:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jun 2026 19:46:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 22 Jun 2026 19:46:25 GMT
ENV PHP_VERSION=8.5.7
# Mon, 22 Jun 2026 19:46:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Mon, 22 Jun 2026 19:46:25 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Mon, 22 Jun 2026 19:46:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 22 Jun 2026 19:46:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:49:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 22 Jun 2026 19:49:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:49:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 22 Jun 2026 19:49:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 22 Jun 2026 19:49:56 GMT
WORKDIR /var/www/html
# Mon, 22 Jun 2026 19:49:57 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 22 Jun 2026 19:49:57 GMT
STOPSIGNAL SIGQUIT
# Mon, 22 Jun 2026 19:49:57 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 22 Jun 2026 19:49:57 GMT
CMD ["php-fpm"]
# Thu, 25 Jun 2026 01:24:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 25 Jun 2026 01:24:37 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 25 Jun 2026 01:24:37 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 01:24:37 GMT
ENV DRUPAL_VERSION=11.3.13
# Thu, 25 Jun 2026 01:24:37 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 25 Jun 2026 01:24:37 GMT
WORKDIR /opt/drupal
# Thu, 25 Jun 2026 01:24:43 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 25 Jun 2026 01:24:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc3e33701d64475ac87ad6eb30f65becc5296d334977b39765ee2b1e1c5c533`  
		Last Modified: Mon, 22 Jun 2026 19:50:04 GMT  
		Size: 3.5 MB (3495854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbc11376c4eedcffcd34e3cf342607c6b94223fa270b4f884341ba748e6d2ec`  
		Last Modified: Mon, 22 Jun 2026 19:50:04 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefacb912255061c9bbedb22b598aa877a5656cba252da1c591468b1904b17d1`  
		Last Modified: Mon, 22 Jun 2026 19:50:04 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efdab117b8da38d3f192d90d4d0048269e91769631772b97f3542c5cabd1910`  
		Last Modified: Mon, 22 Jun 2026 19:50:04 GMT  
		Size: 14.4 MB (14421074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2ae5b1bc1f12d814ae63232200055d810193a2629dce0c656a2011a779495d`  
		Last Modified: Mon, 22 Jun 2026 19:50:05 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56730b6e8a87b6e34ee67f3a24464ac0ee79b62eb9c0478934e14e5e9bdb8490`  
		Last Modified: Mon, 22 Jun 2026 19:50:06 GMT  
		Size: 17.1 MB (17134219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fe887f426b225162fe7e7503eab5a5bf5e20f7804983ee86487c14872e0ba0`  
		Last Modified: Mon, 22 Jun 2026 19:50:06 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642d9b24733d151e164a75d79754fdfc93dec79048f00dbb6224734b1de4cc00`  
		Last Modified: Mon, 22 Jun 2026 19:50:06 GMT  
		Size: 22.3 KB (22294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ae93799b3bdeb5c1a6c5a299d3694766b489d4848744cdacc9ff3db53693e5`  
		Last Modified: Mon, 22 Jun 2026 19:50:07 GMT  
		Size: 9.3 KB (9269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9c0650d1fa60fd9b29db729357f15af029ba704f30612c34d558012cda3019`  
		Last Modified: Thu, 25 Jun 2026 01:24:55 GMT  
		Size: 6.3 MB (6329369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421b6f71e7197bebc7482530b8e612840e78c9f8a81423d198ffc2a4c0be9985`  
		Last Modified: Thu, 25 Jun 2026 01:24:55 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec48062e98022ac5b89cdf7d841c837df2ecab9e07309c1c37d2b9ba1ef9f30e`  
		Last Modified: Thu, 25 Jun 2026 01:24:55 GMT  
		Size: 823.3 KB (823337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d68cbe6a8c8d2e92d4e1da11ef6741c34b3cac1dbefab0fa803978474fd7703`  
		Last Modified: Thu, 25 Jun 2026 01:24:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596c8d4095012522697fbd1552890b50c3876f5f582d24272557b0f2389db970`  
		Last Modified: Thu, 25 Jun 2026 01:24:58 GMT  
		Size: 21.4 MB (21406095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.23` - unknown; unknown

```console
$ docker pull drupal@sha256:5c5a8f12c0c499a30e0eb5ee66b30c3e7285cbf837a0a6249e54a303e929940c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.2 KB (401184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993619ebd85494b0240c83ca2457e27d7cb855dea61468f71e60c1d1ed4a04f8`

```dockerfile
```

-	Layers:
	-	`sha256:25952aeb680a5a85ab43dd2777885d1b1777da9aab57522cae568775063bbe49`  
		Last Modified: Thu, 25 Jun 2026 01:24:55 GMT  
		Size: 368.8 KB (368799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1e7736b53c20cfd10023057fe3e3f9bd4cea4a03bd0dee131f1d9da4501fc99`  
		Last Modified: Thu, 25 Jun 2026 01:24:55 GMT  
		Size: 32.4 KB (32385 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.23` - linux; ppc64le

```console
$ docker pull drupal@sha256:bdd4dbb3fc622dbd53d29c6e15d0f6d111c7b8347a5ec90a1e7a02412416ca6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68157612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3685d1fd9eb750b08ab42317cab7025ee8bf5e67275301a6ed3df5f91d4c3bc9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jun 2026 19:55:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 22 Jun 2026 19:55:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 22 Jun 2026 19:55:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jun 2026 19:55:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 22 Jun 2026 19:55:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:55:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:55:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jun 2026 19:55:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 22 Jun 2026 19:55:46 GMT
ENV PHP_VERSION=8.5.7
# Mon, 22 Jun 2026 19:55:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Mon, 22 Jun 2026 19:55:46 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Mon, 22 Jun 2026 19:55:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 22 Jun 2026 19:55:52 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:01:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 22 Jun 2026 20:01:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:01:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 22 Jun 2026 20:01:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 22 Jun 2026 20:01:42 GMT
WORKDIR /var/www/html
# Mon, 22 Jun 2026 20:01:42 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 22 Jun 2026 20:01:42 GMT
STOPSIGNAL SIGQUIT
# Mon, 22 Jun 2026 20:01:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 22 Jun 2026 20:01:42 GMT
CMD ["php-fpm"]
# Mon, 22 Jun 2026 21:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 22 Jun 2026 21:56:14 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 22 Jun 2026 21:56:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 21:56:16 GMT
ENV DRUPAL_VERSION=11.3.13
# Mon, 22 Jun 2026 21:56:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 22 Jun 2026 21:56:16 GMT
WORKDIR /opt/drupal
# Thu, 25 Jun 2026 02:34:01 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 25 Jun 2026 02:34:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1c2b8ee17956f259bd90745e13528ff9e462e59d64a1ed6ee0c1189527c623`  
		Last Modified: Mon, 22 Jun 2026 20:01:58 GMT  
		Size: 3.6 MB (3640684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1b6c964853f49997526f30758b273165c99348dfc22cc1c2fafb34d7e98af0`  
		Last Modified: Mon, 22 Jun 2026 20:01:57 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a102c8fc5cb12dd9d7014a9062d35ec9f60b78b90449669541c0b50dd561db`  
		Last Modified: Mon, 22 Jun 2026 20:01:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d8248567f757005fe52972b2afaa430abbf1fef54ad1b4e3c2cb4d9f4533ed`  
		Last Modified: Mon, 22 Jun 2026 20:01:58 GMT  
		Size: 14.4 MB (14421102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad75f483b7c0359e4655c0a7f12c56399735f6c7e0123c4bd81efc7d9f9e0a1e`  
		Last Modified: Mon, 22 Jun 2026 20:01:59 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e60e8c382669ae393d5a554b3cdf203adb8faacbf7285b5c1843ee5db1c9695`  
		Last Modified: Mon, 22 Jun 2026 20:01:59 GMT  
		Size: 16.9 MB (16895794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6fc3c145376ad5a471b58bb7a2eb9cf53f877725e63a8d09c5362b8e93e8a19`  
		Last Modified: Mon, 22 Jun 2026 20:01:59 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd3dc96db01534a8c7e551faa58121121d1b27a22cc6b8ed2370ce72b3895a9`  
		Last Modified: Mon, 22 Jun 2026 20:02:00 GMT  
		Size: 22.2 KB (22152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2efdfa42184d43e1365c606efa4366057e389bca05c63829f2a9e477beaba2e`  
		Last Modified: Mon, 22 Jun 2026 20:02:00 GMT  
		Size: 9.3 KB (9260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b793e81a9bff7160b4eb25f06b8b83a063957049ae95e7b2f961567774d6bf4a`  
		Last Modified: Mon, 22 Jun 2026 21:57:05 GMT  
		Size: 7.1 MB (7122363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e30c7541ca179c8f775511c9fd782f4a8ba6106f78f03948a6c26d1a96ce9a7`  
		Last Modified: Mon, 22 Jun 2026 21:57:05 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8136d197354d98f2f0eafa9553b1815c59a57f8ae6e2f04086dc4fcea4ec9f1f`  
		Last Modified: Mon, 22 Jun 2026 21:57:05 GMT  
		Size: 823.3 KB (823340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae05d5242a2ecbba7a5626f925f30c0a573118b7a389530af11f4f25f7941a72`  
		Last Modified: Mon, 22 Jun 2026 21:57:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0b6a2633931991166a6ce8b6bed2dc3ea870d72eaf2b28844eb1a7c2763ec6`  
		Last Modified: Thu, 25 Jun 2026 02:34:32 GMT  
		Size: 21.4 MB (21406072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.23` - unknown; unknown

```console
$ docker pull drupal@sha256:2ade4dc392a520c2fd817fa399249e0dda2447a234527d74d84fedb89a0e6ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.7 KB (400693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5e981474ef56e6e524b4702db2617fbcd8fd778b498dedd0ff2ec9e54020b1`

```dockerfile
```

-	Layers:
	-	`sha256:05b68da002d34a6b169643e89d5df9c0718bf3b84c0561120f83cb2935cc3096`  
		Last Modified: Thu, 25 Jun 2026 02:34:31 GMT  
		Size: 368.2 KB (368207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:180949a99858edd211d998885cff71e331d509afc666d83bd731c25141662d2f`  
		Last Modified: Thu, 25 Jun 2026 02:34:31 GMT  
		Size: 32.5 KB (32486 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.23` - linux; riscv64

```console
$ docker pull drupal@sha256:08f3bff959b5a57bdcfd2603d4185f8cb06195bea77df7845cbdab657c23aae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64427399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75cdd4b15bbba07c64e6bfa70f2c77b6a5e5da16968900ff993832308b5f078a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 22 Jun 2026 19:30:17 GMT
ADD alpine-minirootfs-3.23.5-riscv64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:30:17 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 21:37:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jun 2026 21:37:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 22 Jun 2026 21:37:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 22 Jun 2026 21:37:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jun 2026 21:37:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 22 Jun 2026 21:37:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 21:37:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 21:37:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jun 2026 21:37:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 22 Jun 2026 21:37:25 GMT
ENV PHP_VERSION=8.5.7
# Mon, 22 Jun 2026 21:37:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Mon, 22 Jun 2026 21:37:25 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Mon, 22 Jun 2026 21:37:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 22 Jun 2026 21:37:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 23:42:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 22 Jun 2026 23:42:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 23:42:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 22 Jun 2026 23:42:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 22 Jun 2026 23:42:55 GMT
WORKDIR /var/www/html
# Mon, 22 Jun 2026 23:42:56 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 22 Jun 2026 23:42:56 GMT
STOPSIGNAL SIGQUIT
# Mon, 22 Jun 2026 23:42:56 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 22 Jun 2026 23:42:56 GMT
CMD ["php-fpm"]
# Wed, 24 Jun 2026 08:37:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 24 Jun 2026 08:37:23 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 24 Jun 2026 08:37:24 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 08:37:24 GMT
ENV DRUPAL_VERSION=11.3.12
# Wed, 24 Jun 2026 08:37:24 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 24 Jun 2026 08:37:24 GMT
WORKDIR /opt/drupal
# Wed, 24 Jun 2026 08:51:22 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 24 Jun 2026 08:51:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8a1e5860a6401101356d3688f519ef896539fceeb0e505b24a7224fe7e76fdb1`  
		Last Modified: Mon, 22 Jun 2026 19:30:41 GMT  
		Size: 3.6 MB (3573240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb42bea68a2af79d3ab5c7d97b0d79df81a465d93a9d7af266e102c3724bb82`  
		Last Modified: Mon, 22 Jun 2026 22:40:47 GMT  
		Size: 3.6 MB (3605582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88f0e7707ae583d6042075063a4c05b2191916232960e9aa4f37a61bde64b0a`  
		Last Modified: Mon, 22 Jun 2026 22:40:46 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a793f7413b68510356f0ff3df3c37f19645827c4d4847cff60fbdcf56de075be`  
		Last Modified: Mon, 22 Jun 2026 22:40:46 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf71615d818600295929d25343ae0e967e94e4a94700932e8227926ad6c07e1`  
		Last Modified: Mon, 22 Jun 2026 22:40:50 GMT  
		Size: 14.4 MB (14421117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba93106dabfd05a46c05e0abe10fe20c7d47040ed6962da905127e7fad6a3ff8`  
		Last Modified: Mon, 22 Jun 2026 22:40:48 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee805258d49316b730df04079ac708a1dfd0942b7bcda20f42a7f4e36bab9b3`  
		Last Modified: Mon, 22 Jun 2026 23:43:54 GMT  
		Size: 15.5 MB (15523659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0029785fd73e882dfc4f03f5d38559601dbd8b8166b500865d796eadfa16b879`  
		Last Modified: Mon, 22 Jun 2026 23:43:51 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e86c635f96f00c00c411f9063cb5f0a68a6a0fb4e1db4606b3292838d7bdf2`  
		Last Modified: Mon, 22 Jun 2026 23:43:51 GMT  
		Size: 22.1 KB (22145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bda1214f8bda1d7d881157976d5c76ff69c8c43378636a2836f2df89d9c21d3`  
		Last Modified: Mon, 22 Jun 2026 23:43:51 GMT  
		Size: 9.3 KB (9260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4345b443246b009d4410f189b1de81201d975c3bb5633005a1c4ab6d9cc4ef`  
		Last Modified: Wed, 24 Jun 2026 08:40:49 GMT  
		Size: 5.1 MB (5066464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5048168bebf43c2e1cb826011bbcbb67f479b23b521d8f53c256e55e71e9ab8`  
		Last Modified: Wed, 24 Jun 2026 08:40:48 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5cc228c3a6a6fcb88892386ec4538de233486de0a019f88f8cba5570cd9119`  
		Last Modified: Wed, 24 Jun 2026 08:40:48 GMT  
		Size: 823.3 KB (823342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ff53d88165b126accace31ac0048a2450af31f5800ed2e78dc0fdad916f3d4`  
		Last Modified: Wed, 24 Jun 2026 08:40:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b25abd4b232f724b4a3d752c8ac81091c524dae62e7db76f300fd393b5c0a12`  
		Last Modified: Wed, 24 Jun 2026 08:53:56 GMT  
		Size: 21.4 MB (21378043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.23` - unknown; unknown

```console
$ docker pull drupal@sha256:21551d5a8747ee552d8d25df2ec22e3711cf4c742096987c8ea3bb04f5d177e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.6 KB (399618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c6729f8b8d7e5a0b9ed7eafb4bb036fbef9c5f92b4700062be1e5c83bd463f`

```dockerfile
```

-	Layers:
	-	`sha256:ff26cb88eeab0afa68a109787ade2fc70f51a09df47fef6b61f298a233a820e0`  
		Last Modified: Wed, 24 Jun 2026 08:53:52 GMT  
		Size: 367.1 KB (367132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38923120b434864f5b16b5e4a701a1357cc5d2f6b4b2e80a03422a0e289e1eeb`  
		Last Modified: Wed, 24 Jun 2026 08:53:52 GMT  
		Size: 32.5 KB (32486 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.23` - linux; s390x

```console
$ docker pull drupal@sha256:b2008447265afc91b315d70b533ca2b480595b6afeb738f5165fe650c32d2594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66906468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be372a4d2e8d40ca6e6a5f5e9df3b795dcdbac290a2636924fc74fc866f94d9b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:47:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jun 2026 19:47:42 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 22 Jun 2026 19:47:42 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 22 Jun 2026 19:47:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jun 2026 19:47:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 22 Jun 2026 19:47:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:47:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:47:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jun 2026 19:47:43 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 22 Jun 2026 19:47:43 GMT
ENV PHP_VERSION=8.5.7
# Mon, 22 Jun 2026 19:47:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Mon, 22 Jun 2026 19:47:43 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Mon, 22 Jun 2026 19:47:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 22 Jun 2026 19:47:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:52:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 22 Jun 2026 19:52:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:52:35 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 22 Jun 2026 19:52:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 22 Jun 2026 19:52:35 GMT
WORKDIR /var/www/html
# Mon, 22 Jun 2026 19:52:35 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 22 Jun 2026 19:52:35 GMT
STOPSIGNAL SIGQUIT
# Mon, 22 Jun 2026 19:52:35 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 22 Jun 2026 19:52:35 GMT
CMD ["php-fpm"]
# Thu, 25 Jun 2026 01:51:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 25 Jun 2026 01:51:36 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 25 Jun 2026 01:51:36 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 01:51:36 GMT
ENV DRUPAL_VERSION=11.3.13
# Thu, 25 Jun 2026 01:51:36 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 25 Jun 2026 01:51:36 GMT
WORKDIR /opt/drupal
# Thu, 25 Jun 2026 01:51:44 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 25 Jun 2026 01:51:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64065cba007ed4059aa87bf9b196f259e7dac197ab2a68314165fd843deef1a8`  
		Last Modified: Mon, 22 Jun 2026 19:52:48 GMT  
		Size: 3.7 MB (3654485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793761850543ff3f05870796504e1b953dd4f56c4459838827b5e9f099b52232`  
		Last Modified: Mon, 22 Jun 2026 19:52:48 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f38d955ee5b01ac2628bf14ec94e39b1b1febf3a3e70e7bcc263e1f1b21ee3`  
		Last Modified: Mon, 22 Jun 2026 19:52:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3ef8163bd2a0c07ae36764fcfb9eaedac3a0f971f37eed4d51c03ef024890c`  
		Last Modified: Mon, 22 Jun 2026 19:52:48 GMT  
		Size: 14.4 MB (14421101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f67fc650ee64d4e0515e9e4bbcb6b8940bbe0b1eb1dddbbcc9938178cb04d7`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68ff950f4a5f99efb30bf18c9f74b8972a6e88ad45caa897abbc52f0542e83c`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
		Size: 16.1 MB (16054100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265550c589890f4f9c9e28ee492ab1daf88bd13c089ff3f6116ad7a3cde35e8e`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3799ec1255a88954b19aa2f16117af42bb50ae4de57a258c11ec287cc4eef934`  
		Last Modified: Mon, 22 Jun 2026 19:52:50 GMT  
		Size: 22.1 KB (22139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e608630b0717e12fb6ccab19d852635830baf59c09e400db2ed58d124b480285`  
		Last Modified: Mon, 22 Jun 2026 19:52:50 GMT  
		Size: 9.3 KB (9260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46423935b90478ca634ef61f4a36111464b35a16c07b64ab2d1d7df88ff7825f`  
		Last Modified: Thu, 25 Jun 2026 01:52:06 GMT  
		Size: 6.8 MB (6803943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca0ec13b633fa82ae975ee7792974bbf4263f1f5a4fcfc109b110610b017f81`  
		Last Modified: Thu, 25 Jun 2026 01:52:06 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ba3556a8a8072facc74ff4f38e3f11dcef30a04ef732d2c03682ef5758b80d`  
		Last Modified: Thu, 25 Jun 2026 01:52:06 GMT  
		Size: 823.3 KB (823340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b50fbeb4e0f6bc047e6332db0a9cd81d93b62ee566b9ee35c63b59e4e5bd35`  
		Last Modified: Thu, 25 Jun 2026 01:52:05 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78befaa6cdee6c07a429975ad69fb26716a83a5da3b68466504b4311d65b1df`  
		Last Modified: Thu, 25 Jun 2026 01:52:07 GMT  
		Size: 21.4 MB (21406299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.23` - unknown; unknown

```console
$ docker pull drupal@sha256:442a89a752d22a9529776e1130e3fb85eee6872649e3b3688be44f663c61ef7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.6 KB (400601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0004abfadba52b44617431d6bcd30d34e7e08b7b1de06aa866806efbfb574d99`

```dockerfile
```

-	Layers:
	-	`sha256:2481aa4790794a68265b2fd1c223ccc845247c85fc89bfb905aa221915639bd6`  
		Last Modified: Thu, 25 Jun 2026 01:52:06 GMT  
		Size: 368.2 KB (368173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfbaa95cfd66cb29a90aaf4f1b06584f0efe06fb35725bedae9f24e7ba12664f`  
		Last Modified: Thu, 25 Jun 2026 01:52:06 GMT  
		Size: 32.4 KB (32428 bytes)  
		MIME: application/vnd.in-toto+json
