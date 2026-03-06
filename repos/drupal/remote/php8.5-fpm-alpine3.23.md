## `drupal:php8.5-fpm-alpine3.23`

```console
$ docker pull drupal@sha256:f9a133eff4de09d5dea3f73bcc3ac82b64b7a1ac1b2c3a056e1e29369b107fce
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
$ docker pull drupal@sha256:d8fd8f591befaeb7e3eb4c1bdce5d3d58c334c2f262debf4ce7132e786b62211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62163461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4a494f5278a5b0748c9a62d76a8879f769ff7c7c328fcd75baedbfcb267b6f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Feb 2026 18:32:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 13 Feb 2026 18:32:20 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 13 Feb 2026 18:32:20 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 13 Feb 2026 18:32:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Feb 2026 18:32:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Feb 2026 18:32:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:32:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:32:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Feb 2026 18:32:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 13 Feb 2026 18:32:20 GMT
ENV PHP_VERSION=8.5.3
# Fri, 13 Feb 2026 18:32:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Fri, 13 Feb 2026 18:32:20 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Fri, 13 Feb 2026 18:32:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Feb 2026 18:32:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:35:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:35:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:35:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:35:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:35:45 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 18:35:45 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 13 Feb 2026 18:35:45 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 Feb 2026 18:35:45 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 13 Feb 2026 18:35:45 GMT
CMD ["php-fpm"]
# Fri, 06 Mar 2026 18:32:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 06 Mar 2026 18:32:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 06 Mar 2026 18:32:34 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 06 Mar 2026 18:32:34 GMT
ENV DRUPAL_VERSION=11.3.5
# Fri, 06 Mar 2026 18:32:34 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 06 Mar 2026 18:32:34 GMT
WORKDIR /opt/drupal
# Fri, 06 Mar 2026 18:32:44 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Mar 2026 18:32:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d08381aed3df3cc18dc2a1286530620d30922ef5b78c6f7e07f42c726cec050`  
		Last Modified: Fri, 13 Feb 2026 18:35:52 GMT  
		Size: 3.6 MB (3591773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd132acfd6293c426673796aed4f02499778b0d9be7002e80614d7ecefa80b2`  
		Last Modified: Fri, 13 Feb 2026 18:35:52 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac96957003c84deb1b639dd662bd0d111f010ae2d93a22a821577446322768ce`  
		Last Modified: Fri, 13 Feb 2026 18:35:52 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bef48143f7805b61e273dbd328ae9c26fbdf52e51c7ab9e6c96be7c00aae80d`  
		Last Modified: Fri, 13 Feb 2026 18:35:53 GMT  
		Size: 14.4 MB (14357393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53028713d2a062411c7c65b27f141e7b5238377064cc5fa7cd4cfb7e134ab0c4`  
		Last Modified: Fri, 13 Feb 2026 18:35:53 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73e48de0faf93a58f51c7b2ad81f5faf3a26c6bfcc0937360c13357ccf00aa4`  
		Last Modified: Fri, 13 Feb 2026 18:35:53 GMT  
		Size: 16.6 MB (16626007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b2bf6f403a7398e8568844ac3dcfff4b68bbe9d7cd6dcf627a9696ee203914`  
		Last Modified: Fri, 13 Feb 2026 18:35:53 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d2841834ee65510df6e5be43b59cd963dcac2d122ba5ab7ed9febec3880543`  
		Last Modified: Fri, 13 Feb 2026 18:35:54 GMT  
		Size: 23.5 KB (23489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2965d3291e2b3007b1e0ecd6ae7680d1fc0522fd57a9ac578b8fcb1c3f767396`  
		Last Modified: Fri, 13 Feb 2026 18:35:54 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bf316659e35ca5243298e0b43882dc3283fcee00802651f28e7b5cf75d33d2`  
		Last Modified: Fri, 06 Mar 2026 18:32:56 GMT  
		Size: 1.6 MB (1585063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbdbfbd32a315cf79d9ac87b053cc133b852a80b2351c8e1790eb1c3a3228061`  
		Last Modified: Fri, 06 Mar 2026 18:32:56 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf5831419f6414be4d392e06f52ad15173bba6f0e08c8982de61337203e0cb5`  
		Last Modified: Fri, 06 Mar 2026 18:32:56 GMT  
		Size: 777.5 KB (777539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e01cec4173df3ad4381833dcf3183f86c0a844eb54fea5fa808b50f7843e47d`  
		Last Modified: Fri, 06 Mar 2026 18:32:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e7bea5ca3404bc3df1e52bd534a1814ac58d2bac379bf15cceb06ebe6bb126`  
		Last Modified: Fri, 06 Mar 2026 18:32:57 GMT  
		Size: 21.3 MB (21326565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.23` - unknown; unknown

```console
$ docker pull drupal@sha256:cc87faaddc49e19aa162fef27b5a106acccef57b14b6507ba3ae53bcf4d0a1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.2 KB (411242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa16a1245128221c4ca61c1bc5ed0053d3b051f0ec0f38766cea379078df56dc`

```dockerfile
```

-	Layers:
	-	`sha256:004dd596ab84875b6aea4f4603c520f4f38fdd0598204eeb9c85518a61eb6f28`  
		Last Modified: Fri, 06 Mar 2026 18:32:55 GMT  
		Size: 377.7 KB (377663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e2c13ec4f7f639d1a9631cda0f6c3e887c37cbcc0792acab7d0b5cfd5a56464`  
		Last Modified: Fri, 06 Mar 2026 18:32:55 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.23` - linux; arm variant v6

```console
$ docker pull drupal@sha256:eaf4894625ea75f0fe14a98eb53e3ffee0ff495ed69419662b5984720aff9235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59581904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4bdb8df781f4afa40ceb63576fcef5b16bffcba97552ce6ad4ffb45d46466b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 13 Feb 2026 18:39:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 13 Feb 2026 18:39:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 13 Feb 2026 18:39:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 13 Feb 2026 18:39:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Feb 2026 18:39:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Feb 2026 18:39:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:39:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:39:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Feb 2026 18:39:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 13 Feb 2026 18:39:03 GMT
ENV PHP_VERSION=8.5.3
# Fri, 13 Feb 2026 18:39:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Fri, 13 Feb 2026 18:39:03 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Fri, 13 Feb 2026 18:39:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Feb 2026 18:39:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:42:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:42:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:42:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:42:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:42:18 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 18:42:18 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 13 Feb 2026 18:42:18 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 Feb 2026 18:42:18 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 13 Feb 2026 18:42:18 GMT
CMD ["php-fpm"]
# Fri, 06 Mar 2026 18:58:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 06 Mar 2026 18:58:03 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 06 Mar 2026 18:58:03 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 06 Mar 2026 18:58:03 GMT
ENV DRUPAL_VERSION=11.3.5
# Fri, 06 Mar 2026 18:58:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 06 Mar 2026 18:58:03 GMT
WORKDIR /opt/drupal
# Fri, 06 Mar 2026 18:58:13 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Mar 2026 18:58:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9fdf4a543005231a2e330f75d6941d46fd9fff0d94252dafc7812870f00eab9`  
		Last Modified: Fri, 13 Feb 2026 18:42:24 GMT  
		Size: 3.5 MB (3548751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38446ab5421277ffc9431086ff830e41898a7fc828e855ad8bb6eeecc34c84a9`  
		Last Modified: Fri, 13 Feb 2026 18:42:19 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c74fcd02fe8af9ea7f4c80f949e6c129e6ece440d3ef5ad8204994e8e0323ce`  
		Last Modified: Fri, 13 Feb 2026 18:42:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6d1052e9729683f3084079b0d4ae58ad21e70e3c1210a5e6c4ebfe6e4843a2`  
		Last Modified: Fri, 13 Feb 2026 18:42:20 GMT  
		Size: 14.4 MB (14357412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bcd36ef31606201980b65b9029ceb2ef7da0f77eacf3edd806199691387420`  
		Last Modified: Fri, 13 Feb 2026 18:42:20 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5a45cfdbe7dad0b6fb1536c3192fe371289aa45315b956dff0a401a28efd27`  
		Last Modified: Fri, 13 Feb 2026 18:42:24 GMT  
		Size: 14.6 MB (14573358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9330d3f68ee3a041b468c98bd4b9aedd56652d159d21e9214ee38f638a809ce9`  
		Last Modified: Fri, 13 Feb 2026 18:42:24 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8276200ad89316517db9f6978262eb7e0a3bcfe0ac7e1626cfc7dbd096935f83`  
		Last Modified: Fri, 13 Feb 2026 18:42:24 GMT  
		Size: 23.3 KB (23315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e50d48e43b1a3b04618b6b3c0470e55f90ebcab850bec3a44b79711de970d83`  
		Last Modified: Fri, 13 Feb 2026 18:42:25 GMT  
		Size: 9.3 KB (9260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfb093146e436572921332dd90fea7260ad59f57a68908d4ef10784adbee74c`  
		Last Modified: Fri, 06 Mar 2026 18:58:20 GMT  
		Size: 1.4 MB (1391151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206a18f7b2ee07db16cb8cc60b5727c77c65b8b7749cea4f9c43f9e9d220141b`  
		Last Modified: Fri, 06 Mar 2026 18:58:20 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7232cac84e1fbcbb923784cfa8737f0e2b20a27b8df3e9e8caf28a3761aaa5f9`  
		Last Modified: Fri, 06 Mar 2026 18:58:20 GMT  
		Size: 777.5 KB (777537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d704c387ef9e7ed0469915559d3e073f0d8f4050d2f9c68ec6d72813fe8dc0`  
		Last Modified: Fri, 06 Mar 2026 18:58:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5faa2b605f2d1b1ac9eebc485087f3b8c3c1b1ed558ab3796bf52081b200d9c`  
		Last Modified: Fri, 06 Mar 2026 18:58:22 GMT  
		Size: 21.3 MB (21326742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.23` - unknown; unknown

```console
$ docker pull drupal@sha256:5004f0a85f61154bf5eee557b2eb1a9ef8b4c62a6943c38b5e89c68ec9b6d2ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 KB (33524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa0cfbc5cc9e5eb9bd2c57be1c90c6dc88f74191ae26d2d05d0261eb78e0421`

```dockerfile
```

-	Layers:
	-	`sha256:414d6ba47c5cafd545da4ca1697af2eb189913cf05debc431860cc5448f794b0`  
		Last Modified: Fri, 06 Mar 2026 18:58:20 GMT  
		Size: 33.5 KB (33524 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.23` - linux; arm variant v7

```console
$ docker pull drupal@sha256:5f1c8d2c6e2a3bd3523da6d560765c431c906542c06b0083072afd1a83d34d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58183974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494f7896d54ea88a3878f3bd0bb4c64afc9414c3f7672c940688e7f3d35d3869`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Fri, 13 Feb 2026 18:31:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 13 Feb 2026 18:31:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 13 Feb 2026 18:31:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 13 Feb 2026 18:31:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Feb 2026 18:31:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Feb 2026 18:31:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:31:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:31:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Feb 2026 18:31:43 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 13 Feb 2026 18:31:43 GMT
ENV PHP_VERSION=8.5.3
# Fri, 13 Feb 2026 18:31:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Fri, 13 Feb 2026 18:31:43 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Fri, 13 Feb 2026 18:31:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Feb 2026 18:31:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:34:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:34:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:35:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:35:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:35:00 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 18:35:00 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 13 Feb 2026 18:35:00 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 Feb 2026 18:35:00 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 13 Feb 2026 18:35:00 GMT
CMD ["php-fpm"]
# Fri, 06 Mar 2026 18:53:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 06 Mar 2026 18:53:19 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 06 Mar 2026 18:53:19 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 06 Mar 2026 18:53:19 GMT
ENV DRUPAL_VERSION=11.3.5
# Fri, 06 Mar 2026 18:53:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 06 Mar 2026 18:53:19 GMT
WORKDIR /opt/drupal
# Fri, 06 Mar 2026 18:53:28 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Mar 2026 18:53:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3d38f50db7f432e97c4e121a0cdf5599b147cde3093d591bb748e58cb74c5e`  
		Last Modified: Fri, 13 Feb 2026 18:35:07 GMT  
		Size: 3.3 MB (3347473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8476f1b19567a6289588b14c1e17e3922dd63933451b23b717f06e9b8e18a0`  
		Last Modified: Fri, 13 Feb 2026 18:35:07 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c2622f1c5586fd059ed2218ce0e421eef6b10e77f992a7d45deaf6580e866e`  
		Last Modified: Fri, 13 Feb 2026 18:35:07 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84eb5cb37b72af05c2ff03fcb7f04ca2c2134713c7a355595b2b5119f6cb13fb`  
		Last Modified: Fri, 13 Feb 2026 18:35:07 GMT  
		Size: 14.4 MB (14357399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15ba4cb7fa1e8916cb82719f035734aa9d233214c47d33c067473f352cf7df7`  
		Last Modified: Fri, 13 Feb 2026 18:35:08 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f667c178956c7b28f1b24217c0e95a4c0b0089b650304b23f68fb24e87cd37`  
		Last Modified: Fri, 13 Feb 2026 18:35:08 GMT  
		Size: 13.8 MB (13767620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756576ca4dc2bf9cf520314d48b821c49f7c8a94ab3209cf4e7634e05ee19b09`  
		Last Modified: Fri, 13 Feb 2026 18:35:08 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304b2f8311f9b785ab230c96a64d48eea49dfd3a88184bd122eb68b382294eb0`  
		Last Modified: Fri, 13 Feb 2026 18:35:08 GMT  
		Size: 23.3 KB (23325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4112a98a732dc5ba956fce8042af7cb290b2994ba500bf3120672cfb934230a`  
		Last Modified: Fri, 13 Feb 2026 18:35:09 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597473f2ad78ee18fdf4d9282b0eb9c7d321ff676c8bb64333433fe46dd17116`  
		Last Modified: Fri, 06 Mar 2026 18:53:41 GMT  
		Size: 1.3 MB (1288342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d3eb871f52ee5320b818b865e8ab9d871bc106252d48fac78c243c1ec8227e`  
		Last Modified: Fri, 06 Mar 2026 18:53:41 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3541699aee873373843f2f25cc70874be3cb93bca8b5417f3c5fd6bd0dfbe5`  
		Last Modified: Fri, 06 Mar 2026 18:53:42 GMT  
		Size: 777.5 KB (777534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9027441b6dad86fbafa222545f04c7f2adbeb46c033b9453971daca943f4d33d`  
		Last Modified: Fri, 06 Mar 2026 18:53:41 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29821868460d4c4df6dfbfe8496f9953e8b1f9f3541bac337fafa77a0621235a`  
		Last Modified: Fri, 06 Mar 2026 18:53:43 GMT  
		Size: 21.3 MB (21326756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.23` - unknown; unknown

```console
$ docker pull drupal@sha256:80b847b493997ea942c1eb1b6d4fcbcccd32811ac76a52cb7ee12575154d03a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.8 KB (407830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f0c1c0df93e96f076a91c0434190dbc6059120fa972e1376bdc75914da0d0c`

```dockerfile
```

-	Layers:
	-	`sha256:9b8a9a2e96d20c1f60f7e519c654fb6170a164be0420e4c99c1e7d26e2833788`  
		Last Modified: Fri, 06 Mar 2026 18:53:41 GMT  
		Size: 374.1 KB (374091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18488b79a32655f47156f6f7f367b5ad46b3854f9446fb9e0d5f45e715fb45c7`  
		Last Modified: Fri, 06 Mar 2026 18:53:41 GMT  
		Size: 33.7 KB (33739 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:687c049cefb9c31fc94a02f42bac6054896d61d332a6231989f01baa9054afe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61869157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede6d0f84a38fe58e96e6a5edcc1561f487aa7cc1e3fbcede866b23dc33211a6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 13 Feb 2026 18:33:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 13 Feb 2026 18:33:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 13 Feb 2026 18:33:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 13 Feb 2026 18:33:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Feb 2026 18:33:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Feb 2026 18:33:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:33:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:33:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Feb 2026 18:33:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 13 Feb 2026 18:33:28 GMT
ENV PHP_VERSION=8.5.3
# Fri, 13 Feb 2026 18:33:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Fri, 13 Feb 2026 18:33:28 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Fri, 13 Feb 2026 18:33:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Feb 2026 18:33:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:37:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:37:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:37:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:37:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:37:00 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 18:37:01 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 13 Feb 2026 18:37:01 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 Feb 2026 18:37:01 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 13 Feb 2026 18:37:01 GMT
CMD ["php-fpm"]
# Fri, 06 Mar 2026 18:56:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 06 Mar 2026 18:56:35 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 06 Mar 2026 18:56:35 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 06 Mar 2026 18:56:35 GMT
ENV DRUPAL_VERSION=11.3.5
# Fri, 06 Mar 2026 18:56:35 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 06 Mar 2026 18:56:35 GMT
WORKDIR /opt/drupal
# Fri, 06 Mar 2026 18:56:42 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Mar 2026 18:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8416410f3f4a9bd036fa55d01c1365804ea59dedd5190aebcaa6e7dcabda34b9`  
		Last Modified: Fri, 13 Feb 2026 18:37:08 GMT  
		Size: 3.6 MB (3601855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96992df102a35a56ef4ea8cb97e6a4d1a88d40e1aaef9e6d6a475c2e43907ece`  
		Last Modified: Fri, 13 Feb 2026 18:37:07 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c05e4ecfd89aabc29d1d1275097afe9be4a6d80b9480c180c056ffbcfb4f719`  
		Last Modified: Fri, 13 Feb 2026 18:37:08 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2d056589815b2cc4f1c4fc11a3a914f9916ef5ebd98356e54ee8011a6c378a`  
		Last Modified: Fri, 13 Feb 2026 18:37:08 GMT  
		Size: 14.4 MB (14357398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99cace4137df23fc07d42e32784f6b19b32e8b3c2b9020b858b80b95659d9c2d`  
		Last Modified: Fri, 13 Feb 2026 18:37:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143eef3b52bd0adb05c83c9633a9369402eb02b33bbdd0194411ce3d2bc516f2`  
		Last Modified: Fri, 13 Feb 2026 18:37:09 GMT  
		Size: 16.0 MB (16036797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08e47851147ea6ed20133cc6550783c86e85d867f6ee21f1d1e6537ac71ee4a`  
		Last Modified: Fri, 13 Feb 2026 18:37:09 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd5f108e0fac24e3db94f57f318c6b34aa942f58e267d0a276f5d848f5b5846`  
		Last Modified: Fri, 13 Feb 2026 18:37:09 GMT  
		Size: 23.3 KB (23348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80a8506175bb65db47d1e4603e3716af95b38e5e4843e9c20c61230abecf210`  
		Last Modified: Fri, 13 Feb 2026 18:37:10 GMT  
		Size: 9.3 KB (9263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47bff82b288c909238f6564f475e09176bb3a1576ad010357849a8c788af041a`  
		Last Modified: Fri, 06 Mar 2026 18:56:56 GMT  
		Size: 1.5 MB (1534766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b7a5f7eacf3b6f32d6b559caa6bddc9e06c4aa7686b27bb27bb4ecd3131013`  
		Last Modified: Fri, 06 Mar 2026 18:56:56 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d6d9453077a0ead35b7cdd12f1c5610defb3c7e8312d4b22c7e84835a32aa5`  
		Last Modified: Fri, 06 Mar 2026 18:56:56 GMT  
		Size: 777.5 KB (777536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295694776cffb5122f843ffe432fa9c939385024bcb47936508e073b8a9dbf04`  
		Last Modified: Fri, 06 Mar 2026 18:56:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8bc0e65fad9c026ab8e8afaaa37d11bb562a460ba178a716f37909cd9ac008`  
		Last Modified: Fri, 06 Mar 2026 18:56:57 GMT  
		Size: 21.3 MB (21326561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.23` - unknown; unknown

```console
$ docker pull drupal@sha256:2532994b4d89713c868979fddccd0c832fc33e220a8a3a4d7c5cf74f3912264b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.9 KB (407914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f225fa51bd9aac57cb864d60e326be5fab7a179ac77f7b66f1b6e112fe0bdf8`

```dockerfile
```

-	Layers:
	-	`sha256:d6e228dd1a460ef00c4a4fd77f4082f828f534c17075d9f316bcddd08e63aafd`  
		Last Modified: Fri, 06 Mar 2026 18:56:55 GMT  
		Size: 374.1 KB (374127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b17b705e747382ba418e607b836df5c2413528a44cad518654e46c24bd0f6531`  
		Last Modified: Fri, 06 Mar 2026 18:56:55 GMT  
		Size: 33.8 KB (33787 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.23` - linux; 386

```console
$ docker pull drupal@sha256:49cd953923a773250698e14967fba0993f0d1903110714c5ed4f456ee742ea99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62460584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e877b5e54f557c20248d4afbc34840e7812868baf1122baf4c9368e0e51351e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Fri, 13 Feb 2026 18:33:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 13 Feb 2026 18:33:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 13 Feb 2026 18:33:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 13 Feb 2026 18:33:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Feb 2026 18:33:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Feb 2026 18:33:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:33:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:33:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Feb 2026 18:33:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 13 Feb 2026 18:33:49 GMT
ENV PHP_VERSION=8.5.3
# Fri, 13 Feb 2026 18:33:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Fri, 13 Feb 2026 18:33:49 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Fri, 13 Feb 2026 18:33:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Feb 2026 18:33:53 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:37:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:37:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:37:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:37:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:37:33 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 18:37:33 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 13 Feb 2026 18:37:33 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 Feb 2026 18:37:33 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 13 Feb 2026 18:37:33 GMT
CMD ["php-fpm"]
# Fri, 06 Mar 2026 18:34:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 06 Mar 2026 18:34:44 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 06 Mar 2026 18:34:44 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 06 Mar 2026 18:34:44 GMT
ENV DRUPAL_VERSION=11.3.5
# Fri, 06 Mar 2026 18:34:44 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 06 Mar 2026 18:34:44 GMT
WORKDIR /opt/drupal
# Fri, 06 Mar 2026 18:34:51 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Mar 2026 18:34:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46d8d5b7c7c9adf624cc6f15d0c8559403075bdcb8a91392e0bbc43762511a5`  
		Last Modified: Fri, 13 Feb 2026 18:37:40 GMT  
		Size: 3.6 MB (3629389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73bbf9f138b79d24ea2c60d0995e5f282452862f6698d03b1efa6b4551bf61e`  
		Last Modified: Fri, 13 Feb 2026 18:37:40 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e79e2f475a7872c42ebbadaa105ba8cc953bd1ccb41a0f1dc666ea6ee8d1d84`  
		Last Modified: Fri, 13 Feb 2026 18:37:40 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fe40182eebce531801bdd6fd935c54a8ab9df3497474559a22d6403d63b0e6`  
		Last Modified: Fri, 13 Feb 2026 18:37:41 GMT  
		Size: 14.4 MB (14357384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae80a1897b465e1d67e4fc40c8101b1ae303ec49fd41fc4b55c6bb385779171`  
		Last Modified: Fri, 13 Feb 2026 18:37:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec2b0cc4bfe550c8e7db2d2a47b0b418ef7c53a6bd84d0782c29e8fe3658dfb`  
		Last Modified: Fri, 13 Feb 2026 18:37:41 GMT  
		Size: 17.0 MB (16962319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8bb02d6ee45b65e26b83007d99313166ecc943bd58ca4b0dba525c5a5874f2`  
		Last Modified: Fri, 13 Feb 2026 18:37:41 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b52d27506bf89bdf4319c89b7c07b54b96c8bd9f22b343a1949f72302ae4ecf`  
		Last Modified: Fri, 13 Feb 2026 18:37:42 GMT  
		Size: 23.5 KB (23511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7a487a0abc5efa8758e12e6cfed5bd7e36f398ce5abf1e52864d28d408c75c`  
		Last Modified: Fri, 13 Feb 2026 18:37:42 GMT  
		Size: 9.3 KB (9258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd66ee71cdf45b5e0b60fc400eb9d88f5038daddc282824fcbf0ecb57e0a640`  
		Last Modified: Fri, 06 Mar 2026 18:35:04 GMT  
		Size: 1.7 MB (1683453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbaae7df26c09edcf1b348ddb3558982674e3dac6baf43e26426f50f05a982ca`  
		Last Modified: Fri, 06 Mar 2026 18:35:04 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f32201b396fc4adf4479677a59bce7cad0a3ea4098223ac20dc16d38551eec`  
		Last Modified: Fri, 06 Mar 2026 18:35:04 GMT  
		Size: 777.5 KB (777532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ff9d0061ce292059a582ff2d07f588c2f4d7399565fbc2f3a157de9595d90a`  
		Last Modified: Fri, 06 Mar 2026 18:35:04 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c4318e7c29a713513c49314da12ebd79be84906fb25ab916962a12e572f530`  
		Last Modified: Fri, 06 Mar 2026 18:35:05 GMT  
		Size: 21.3 MB (21326189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.23` - unknown; unknown

```console
$ docker pull drupal@sha256:60c7594b48bf67a73569ce0ba3d5f0f543c084a625027438d41fb3520d183827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.1 KB (411134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cfe0c7d503ef5b987117bf8acb8e03056e54115d4f3897ccbca4df43bfb9e9`

```dockerfile
```

-	Layers:
	-	`sha256:557396052ff4f2708d501ce41ff3fb10ac09988dc1579785784f227c874fc4df`  
		Last Modified: Fri, 06 Mar 2026 18:35:03 GMT  
		Size: 377.6 KB (377618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c25f94c730e2347244303c4739ca4f1dcda01a28e5b071297821a083a542c782`  
		Last Modified: Fri, 06 Mar 2026 18:35:03 GMT  
		Size: 33.5 KB (33516 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.23` - linux; ppc64le

```console
$ docker pull drupal@sha256:47a3baf39463e25bcb4fb5fff4924e3b5a1ae7a2cc5af3875fdbe04eb8144be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62478563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70e42b25d8f1a2befa5dc6d58401ca6fa32b0c49bd4d5062fa39d71857aad0a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 02:38:57 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 02:38:57 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 02:38:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 02:38:57 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_VERSION=8.5.3
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Fri, 13 Feb 2026 19:16:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Feb 2026 19:16:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 19:22:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 19:22:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 19:22:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 19:22:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 19:22:32 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 19:22:32 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 13 Feb 2026 19:22:32 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 Feb 2026 19:22:32 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 13 Feb 2026 19:22:32 GMT
CMD ["php-fpm"]
# Thu, 05 Mar 2026 18:50:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 05 Mar 2026 18:50:26 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 05 Mar 2026 18:50:27 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:50:27 GMT
ENV DRUPAL_VERSION=11.3.5
# Thu, 05 Mar 2026 18:50:27 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Mar 2026 18:50:27 GMT
WORKDIR /opt/drupal
# Fri, 06 Mar 2026 19:11:55 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Mar 2026 19:11:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7dd774a9daa9cc5f74d16d61155e614ceedece1fd19c05044ba6ace37dd4c6`  
		Last Modified: Wed, 28 Jan 2026 02:43:14 GMT  
		Size: 3.8 MB (3768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a002cadcf53d322e552c6a02f973915d8017427dfda71de122592386df6743`  
		Last Modified: Wed, 28 Jan 2026 02:43:14 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210b05b21b742c21780f39ad80c5babf4b1d13a4f41a2726c561bfb0fcc954e0`  
		Last Modified: Wed, 28 Jan 2026 02:43:14 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566f99cafde0f397256493135fb5a020de181b7a90ec95e51a81d8ce54baa1a6`  
		Last Modified: Fri, 13 Feb 2026 19:22:04 GMT  
		Size: 14.4 MB (14357425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c322b30c3b4e11ab429a18376322e0624d845c6d030b0122cf5af57ea1dd0c43`  
		Last Modified: Fri, 13 Feb 2026 19:22:03 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310c0e22a18e8b9edc572f5ca859f692ee500d569ee9130143028f7e1802aec9`  
		Last Modified: Fri, 13 Feb 2026 19:22:50 GMT  
		Size: 16.7 MB (16732276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fbda1e86475651cf4d5ddcdd2b959100e7b252916ec1255a61de776166ea92`  
		Last Modified: Fri, 13 Feb 2026 19:22:50 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad36c15f11b34482944dd80a8e0ae47e8133bd93dc40c828a36011f2f1ab119b`  
		Last Modified: Fri, 13 Feb 2026 19:22:50 GMT  
		Size: 23.4 KB (23353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3400d56a4ba79f95bb453817245a85d646dcbee0ac01a5d62db00d2e798f74`  
		Last Modified: Fri, 13 Feb 2026 19:22:50 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9d52569cd6254126fa788569de9a37bf6f933327a056167ad89507e050def9`  
		Last Modified: Thu, 05 Mar 2026 18:51:14 GMT  
		Size: 1.6 MB (1649207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e0b88fe3f1ff9fa12565226c01e6e766d924b3052f6e0f1e47d7995c7c13a3`  
		Last Modified: Thu, 05 Mar 2026 18:51:14 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f1b4fff83d8368ea08bb7f6036bd6d2bf35eb3787613155dbcdd31913b289a`  
		Last Modified: Thu, 05 Mar 2026 18:51:15 GMT  
		Size: 777.5 KB (777539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bd42a06a88ff7ea53e6843696266be89a69fc524ed44b5d630e56260be298c`  
		Last Modified: Thu, 05 Mar 2026 18:51:14 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d4f6772cb2986c9a73824208696ef672e1d826a305a973ff531992e1e4d1b1`  
		Last Modified: Fri, 06 Mar 2026 19:12:28 GMT  
		Size: 21.3 MB (21326452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.23` - unknown; unknown

```console
$ docker pull drupal@sha256:8e88fc0168a3ee806490fec93e60c160c62a94c74e396a9de0b49b81de350c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.7 KB (407741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579f479b29baca3fb8a2925db58666ed0ae0652bc5cd4750ad003df8b8cc019d`

```dockerfile
```

-	Layers:
	-	`sha256:fedd25b6a0961b82a785306e92f72933e59e2059399b7ec5568faa486ede202a`  
		Last Modified: Fri, 06 Mar 2026 19:12:27 GMT  
		Size: 374.1 KB (374080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdff9403452896bde80649b4111abdd6946f8f77113b119a009acfcce90e60a5`  
		Last Modified: Fri, 06 Mar 2026 19:12:27 GMT  
		Size: 33.7 KB (33661 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.23` - linux; riscv64

```console
$ docker pull drupal@sha256:7f924f6cefc8b5d6eeec0dbf9f1eeb6fbd7443e003d944e6590177a93f5bb3f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60624673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4089bd1f7a12cf0a34f415b64a402ef3adf56234a9bea6450b17d7224a3a198`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 09:13:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 09:13:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 09:13:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 09:13:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 09:13:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 09:13:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_VERSION=8.5.3
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Fri, 13 Feb 2026 22:11:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Feb 2026 22:11:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sun, 15 Feb 2026 05:00:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sun, 15 Feb 2026 05:00:02 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sun, 15 Feb 2026 05:00:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sun, 15 Feb 2026 05:00:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sun, 15 Feb 2026 05:00:07 GMT
WORKDIR /var/www/html
# Sun, 15 Feb 2026 05:00:08 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sun, 15 Feb 2026 05:00:08 GMT
STOPSIGNAL SIGQUIT
# Sun, 15 Feb 2026 05:00:08 GMT
EXPOSE map[9000/tcp:{}]
# Sun, 15 Feb 2026 05:00:08 GMT
CMD ["php-fpm"]
# Thu, 05 Mar 2026 19:01:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 05 Mar 2026 19:01:21 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 05 Mar 2026 19:01:21 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:01:21 GMT
ENV DRUPAL_VERSION=11.3.5
# Thu, 05 Mar 2026 19:01:21 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Mar 2026 19:01:21 GMT
WORKDIR /opt/drupal
# Fri, 06 Mar 2026 18:50:33 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Mar 2026 18:50:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d64a68485fdb9ab2ec4159ac3e04e0bb79d9f1d037e580e928ca2b9604180f`  
		Last Modified: Wed, 28 Jan 2026 10:13:59 GMT  
		Size: 3.7 MB (3741000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b030c1b113432578231e8fe7c8a1bc913f2dc5dcba512e805fa9ab07768c9bd4`  
		Last Modified: Wed, 28 Jan 2026 10:13:58 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32a0e9bcb36b34307b4eada1f50c1cd4244d43d19ee57d962818dcb0ff0b110`  
		Last Modified: Wed, 28 Jan 2026 10:13:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412b57f7ad7c628023df98843825973dce984e7ea7667c91f921b96e2d624b07`  
		Last Modified: Sat, 14 Feb 2026 00:49:10 GMT  
		Size: 14.4 MB (14357412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbee05b580e10b8f85dab99b2f7e4e71e8b15edcf6458d7edbfa1fd600ef2cd`  
		Last Modified: Sat, 14 Feb 2026 00:49:05 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf53b82200310c9ffce767bf4a12c41ac09c1ac2034659edaad4c099129462c8`  
		Last Modified: Sun, 15 Feb 2026 05:01:06 GMT  
		Size: 15.4 MB (15381764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e445d0cae02f0fb63f50a6dc34dcbe2285aee1215609ed41c0c03ee786f4aec`  
		Last Modified: Sun, 15 Feb 2026 05:01:04 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc440f42f2f0b5bb857d9284f277c15326aa7c67e4d8fcc55ba369612fb9017a`  
		Last Modified: Sun, 15 Feb 2026 05:01:04 GMT  
		Size: 23.3 KB (23334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56aa2cfea4f288eaf553579aa88208f2cbfaa049347bfb0c47bf33aaf673d354`  
		Last Modified: Sun, 15 Feb 2026 05:01:04 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58163039e718203c576ac2301824ac9ee64a3ebaf568c2f8319f39faec84e036`  
		Last Modified: Thu, 05 Mar 2026 19:04:38 GMT  
		Size: 1.4 MB (1418549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cff86228d04f2220aba2517d46531ea65d2ca623fda9420a0c724b827c139e5`  
		Last Modified: Thu, 05 Mar 2026 19:04:37 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f64e173cf3554733ee44fbb0d39fe44e0090ab0f899364ecf12194d52b2168`  
		Last Modified: Thu, 05 Mar 2026 19:04:38 GMT  
		Size: 777.5 KB (777529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691d3fecc7aad043b0abbc00383b484b7397028201247e199717683a970eb7e2`  
		Last Modified: Thu, 05 Mar 2026 19:04:37 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7df5c061e84009c92e4df5768964827dca0f0b3f8d52e7d2cc75e8bd0039168`  
		Last Modified: Fri, 06 Mar 2026 18:53:10 GMT  
		Size: 21.3 MB (21325973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.23` - unknown; unknown

```console
$ docker pull drupal@sha256:1207cb1cceb167aca1602e82dd4b454df7d4326790e7761f90802ab4ab661979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.7 KB (407737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862b093b80c7cbb954c089b9a85c052f64b579cb3ced89084466ee9f35f7cfc2`

```dockerfile
```

-	Layers:
	-	`sha256:ef9d8a0008e0a8d5582addc48e4948b3d08d04dad3d1c36cad0884c719412e4c`  
		Last Modified: Fri, 06 Mar 2026 18:53:07 GMT  
		Size: 374.1 KB (374076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64b43fad7c271e3be588febf55499808d0e5aa8611c0a94800a6eb6f138e7251`  
		Last Modified: Fri, 06 Mar 2026 18:53:06 GMT  
		Size: 33.7 KB (33661 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.23` - linux; s390x

```console
$ docker pull drupal@sha256:981addc0fafaee2dcbb63c5f5142dec41ac12cdd97675db7dad9b89cfec8b635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61515663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e08f1523602ae11f2e17f2769b5da68d80451c7dbd553119c6aef7bdb5edb668`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 02:22:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 02:22:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 02:22:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 02:22:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 02:22:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:22:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:22:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 02:22:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 28 Jan 2026 02:22:33 GMT
ENV PHP_VERSION=8.5.3
# Wed, 28 Jan 2026 02:22:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Wed, 28 Jan 2026 02:22:33 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Fri, 13 Feb 2026 18:44:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Feb 2026 18:44:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:50:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:50:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:50:59 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:50:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:50:59 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 18:50:59 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 13 Feb 2026 18:50:59 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 Feb 2026 18:50:59 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 13 Feb 2026 18:50:59 GMT
CMD ["php-fpm"]
# Fri, 06 Mar 2026 18:54:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 06 Mar 2026 18:54:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 06 Mar 2026 18:54:22 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 06 Mar 2026 18:54:22 GMT
ENV DRUPAL_VERSION=11.3.5
# Fri, 06 Mar 2026 18:54:22 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 06 Mar 2026 18:54:22 GMT
WORKDIR /opt/drupal
# Fri, 06 Mar 2026 18:54:29 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Mar 2026 18:54:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cf22f299f5bcaf74fad4af8e728f6e6624c9a610c22221efa870a8765d30d4`  
		Last Modified: Wed, 28 Jan 2026 02:27:03 GMT  
		Size: 3.8 MB (3795102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0814653fdf7094e8d4c40445da0f7faef7d6e1c3470e2400b2c3e23b34824e75`  
		Last Modified: Wed, 28 Jan 2026 02:27:03 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be88a5ab07486c1edbe76d7f40fb614509f04ca091ab87b96dc64e90aff8b8e2`  
		Last Modified: Wed, 28 Jan 2026 02:27:03 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc4de4fb00e841de5cf7c76f94b6a4f904bf9629ae6014dfc6a9e06bffae5c4`  
		Last Modified: Fri, 13 Feb 2026 18:51:16 GMT  
		Size: 14.4 MB (14357407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c24f2891f7326e6a7eac980e62b128dfbc18623025e0679b053c0a15220527`  
		Last Modified: Fri, 13 Feb 2026 18:51:16 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f602e6652dc5ddfd6d89743226e5b1bcfde731aaed7b4e7da8192472a9ffe51e`  
		Last Modified: Fri, 13 Feb 2026 18:51:17 GMT  
		Size: 15.9 MB (15897318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faddf671e2dda791b97a717323a8f8d36b61d7266bf48c77cd4d1d946fdc971`  
		Last Modified: Fri, 13 Feb 2026 18:51:16 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0571a238a47988eaf721f65f03ac9bfafb2aab3943f73ac5354e420b60bd2b`  
		Last Modified: Fri, 13 Feb 2026 18:51:17 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8503564f13a9f04cd2bcbabca1e16a25ed20950d998fdaa08ad001bd700ede`  
		Last Modified: Fri, 13 Feb 2026 18:51:18 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8ff32eb5595deda400b496963f955df89ee8176f0fc284bf86eee848462fe8`  
		Last Modified: Fri, 06 Mar 2026 18:54:49 GMT  
		Size: 1.6 MB (1599325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8823473f7d81f771a6d344a96142e6b93da059f32f31a7af358920dabd1ef2`  
		Last Modified: Fri, 06 Mar 2026 18:54:49 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d20b496b0a372e43e74da7b9ffbe870550cdfa9c8fe4dd00d6edb185113483e`  
		Last Modified: Fri, 06 Mar 2026 18:54:49 GMT  
		Size: 777.5 KB (777543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6cd5a2fd33514b79817f2f8a701d807026aedd45d739296d4fcc2cbe5cb9ef`  
		Last Modified: Fri, 06 Mar 2026 18:54:49 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96a0ecaef64224b435a8709a0c65631a78c6e98349432f126c59a14e5069287`  
		Last Modified: Fri, 06 Mar 2026 18:54:50 GMT  
		Size: 21.3 MB (21326488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.23` - unknown; unknown

```console
$ docker pull drupal@sha256:aa8f454dc8b3796229b19202e0f904ef8e9e11feb5835d53655968d47477f1a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.6 KB (407601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64073dba491320f7c33d391722db3ebfeaaeed8a53b1e61829e76b5cfa3e66a8`

```dockerfile
```

-	Layers:
	-	`sha256:2fc45a04de768114edc10152e20919dde334a0aa0d6d058dc65400c42f271732`  
		Last Modified: Fri, 06 Mar 2026 18:54:49 GMT  
		Size: 374.0 KB (374022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4fb92ed2e5c36eae5121b23e62af291cc71a2a1b03746e9a002ce45b827efa4`  
		Last Modified: Fri, 06 Mar 2026 18:54:49 GMT  
		Size: 33.6 KB (33579 bytes)  
		MIME: application/vnd.in-toto+json
