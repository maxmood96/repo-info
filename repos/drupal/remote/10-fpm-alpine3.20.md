## `drupal:10-fpm-alpine3.20`

```console
$ docker pull drupal@sha256:8dcc810612e7c9f1f4d3aaa27b82e35cb4e7c23dff0d5922ae298eb1bd85f771
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

### `drupal:10-fpm-alpine3.20` - linux; amd64

```console
$ docker pull drupal@sha256:f1ec673ba5f28947adb6a7b5e689f8f7514d5e10061e171760ee70884ee87530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56768392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6d0a51b59ae57e85b3e45c42bb922c2aa2c9b700a997ba2c77730aacaa52a3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 06 Feb 2025 04:56:28 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 06 Feb 2025 04:56:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Feb 2025 04:56:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_VERSION=8.3.17
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /var/www/html
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Feb 2025 04:56:28 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 06 Feb 2025 04:56:28 GMT
CMD ["php-fpm"]
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV DRUPAL_VERSION=10.4.2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a4ec0a6feb139f2cf3d03bd73a59533aa96e36659bbd289ec0771c24c9f917`  
		Last Modified: Fri, 14 Feb 2025 21:11:21 GMT  
		Size: 3.3 MB (3313889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e26e0c36c4b302fba3179f931a2faf690df3c495a7fecacae76c0c37f5a883`  
		Last Modified: Fri, 14 Feb 2025 21:11:20 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89004d98ef49a7ef1083e06c3a3ebacf0a3c64478ed95d5a1e495504cc3efd6`  
		Last Modified: Fri, 14 Feb 2025 21:11:20 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c0647dd90cd70e5a14a43a350d601927d2442a5697812f978eca8fa57684bb`  
		Last Modified: Fri, 14 Feb 2025 21:11:20 GMT  
		Size: 12.6 MB (12562317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741f16f3c97e4ea0175ec4235f3b064d81a582ef9593f896d9e1a5c346416d07`  
		Last Modified: Fri, 14 Feb 2025 21:11:19 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62ddfd52c12720a58b968440d87a63aaf8d54b1b49ce4802dd1f96a5709a613`  
		Last Modified: Fri, 14 Feb 2025 21:11:21 GMT  
		Size: 13.1 MB (13111736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f473455a9723bfac7b115ded3b2ac6543e6e5d6d20f765ee5cc1226491e6dbd`  
		Last Modified: Fri, 14 Feb 2025 21:11:19 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cc1ab93a49053dd51d97b70b723a3e55425165be9e607114d81c7761a7be8f`  
		Last Modified: Fri, 14 Feb 2025 21:11:19 GMT  
		Size: 19.7 KB (19701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bade6a7973484de8f8d633c3b41888c6e04c0ab53d04819bdc62512195877d`  
		Last Modified: Fri, 14 Feb 2025 21:11:19 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9deef83d91c881f9b228c047d946adb4f85266c3d1ce1d4f5c9b874c278f2281`  
		Last Modified: Sat, 15 Feb 2025 07:27:39 GMT  
		Size: 1.9 MB (1902150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ca64a4ccf923f473aaddc05b31e203e0ad0a29a658d798907c1a820e289d7f`  
		Last Modified: Sat, 15 Feb 2025 07:27:37 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7781d8dc73cdef2bd4b960862a6af767641af7643c82db390981279c2f403912`  
		Last Modified: Sat, 15 Feb 2025 07:27:38 GMT  
		Size: 740.3 KB (740347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3cd7158283ee04400e931878b9f2654203b9e15692a3fe66e269bda8488587`  
		Last Modified: Sat, 15 Feb 2025 07:27:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c65a9617a3efbfbcff3fc2bb99044e53aca9d67c93820517b6c462c74056677`  
		Last Modified: Sat, 15 Feb 2025 07:27:42 GMT  
		Size: 21.5 MB (21477625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:a309012ae834736bccc2d0bbd0623cc0b10eb35e643aab1923625a92b93f2894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.6 KB (373619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e5349e686c7e69dd3f6cc9dac76f42b52039d65279e960b4740391722e8af1`

```dockerfile
```

-	Layers:
	-	`sha256:690cd1817b64d1ec0dc458404bc3d9da01c963b5691fea55a66c46987ae51335`  
		Last Modified: Fri, 14 Feb 2025 23:54:08 GMT  
		Size: 340.6 KB (340587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b770e4023d370e80fe84f210dfd731353a7553647242fdb578c0e367887cdf35`  
		Last Modified: Fri, 14 Feb 2025 23:54:08 GMT  
		Size: 33.0 KB (33032 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.20` - linux; arm variant v6

```console
$ docker pull drupal@sha256:0011120636fe5fb54edd4b952ef65fe607b63adee9a72131922e2c0857d069cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58140367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf8c36af8d61b2fa29f0b9fa8ed8f535a36458167f2174202fb43dcae729284`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 06 Feb 2025 04:56:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Feb 2025 04:56:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_VERSION=8.3.17
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /var/www/html
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Feb 2025 04:56:28 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 06 Feb 2025 04:56:28 GMT
CMD ["php-fpm"]
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV DRUPAL_VERSION=10.4.2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Tue, 14 Jan 2025 20:34:27 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db6ffe3ef654cff5545ca59dc5f06633dd6a45d737ad50c60dbdf1cfaa7c1cd`  
		Last Modified: Wed, 15 Jan 2025 01:17:12 GMT  
		Size: 3.3 MB (3291511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0b3742a8730e352c2d2f9b2b074af69eca367f405a0f860eb4588c6dc8e881`  
		Last Modified: Wed, 15 Jan 2025 01:17:14 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536a818f8e79c0c89eeb3c2062540dc8de02edfa1d91832c4872509e9271ef3c`  
		Last Modified: Tue, 14 Jan 2025 21:51:58 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc83e196ff43747c3b6cea1d0bd3b0f493fe67f13868a59e30f6e8ddde016a18`  
		Last Modified: Fri, 14 Feb 2025 06:03:08 GMT  
		Size: 12.6 MB (12562319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd1e85543727782dfd4603324031cb2850077346337a7c9bb01c14e23bcf300`  
		Last Modified: Fri, 14 Feb 2025 06:03:07 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d24ce4b30bec69a8280cadbcc8150b51ec6a44373584076a1f14f84ff33281`  
		Last Modified: Fri, 14 Feb 2025 06:05:03 GMT  
		Size: 15.3 MB (15278204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb52e760290eb7e06eb08ca6d21fe47b7f571d22fa384a3e525fb1546fc39e10`  
		Last Modified: Fri, 14 Feb 2025 06:05:03 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6497eb79d72aefb89bfe1f975c98b41109efa7dfcdd19f39f0ac2777d61215b2`  
		Last Modified: Fri, 14 Feb 2025 06:05:03 GMT  
		Size: 19.5 KB (19538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576c74db8da69c59a387196cf67351839e7099efaa0aa47c5cb8697e6c9ed631`  
		Last Modified: Fri, 14 Feb 2025 06:05:03 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72558ad1e0ae8342900ea75c887f54c9f437af82456054dcc378e43b45cadd11`  
		Last Modified: Fri, 14 Feb 2025 08:55:21 GMT  
		Size: 1.4 MB (1385508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53894508cfb9717d1222a798ec1781fcb549512eaba67ebfc30bdd8ef4858b6`  
		Last Modified: Fri, 14 Feb 2025 08:55:21 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a267be4cebb16d2a6c087423724708f6e75e65852cdd26e397be3202e8ca93`  
		Last Modified: Fri, 14 Feb 2025 08:55:21 GMT  
		Size: 740.3 KB (740348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4788b28e3857d64e397d62feebdf9618b667d747b17b933b38ddee884c87abb8`  
		Last Modified: Fri, 14 Feb 2025 08:55:21 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be05b9a9cfee1da38b07a364acae3fd6c03824a155743a5abcb513a3967f37f1`  
		Last Modified: Fri, 14 Feb 2025 08:55:22 GMT  
		Size: 21.5 MB (21477732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:ede93b062713fde069e194722f073050d8dfc2a541f05a8aa5e3d2e87243be3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 KB (32957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94800aa14f7c06ca92a03a883b06000e8d88000a1425119d4b32b74606a187cd`

```dockerfile
```

-	Layers:
	-	`sha256:b49b2ce21c6dfc5d3bab3145c0c504f5077ee8002d255d1c86533df03b8ac817`  
		Last Modified: Fri, 14 Feb 2025 08:55:01 GMT  
		Size: 33.0 KB (32957 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.20` - linux; arm variant v7

```console
$ docker pull drupal@sha256:610a32a4eae98fb891c96285b0b7f1a70df6ae0ec9ae916cc229832f975c0065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56571566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7885d1ce233d4f7c8df2687e1d6d18fd35470c47fb29277d56eb480950f35543`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 06 Feb 2025 04:56:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Feb 2025 04:56:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_VERSION=8.3.17
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /var/www/html
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Feb 2025 04:56:28 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 06 Feb 2025 04:56:28 GMT
CMD ["php-fpm"]
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV DRUPAL_VERSION=10.4.2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Tue, 14 Jan 2025 20:45:20 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59598ed4d46933f984783e283ed636ac43c785dd3207a5432bcc816f12d3e64`  
		Last Modified: Wed, 15 Jan 2025 01:17:13 GMT  
		Size: 3.1 MB (3098287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395c20ee4940a4e59421ae1219a3af584a15664ef7e2cac6f928fe961a0dbe08`  
		Last Modified: Tue, 14 Jan 2025 21:51:56 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee856b900e721e0ee0e69e264eac4529da212f3087333fa1155fcba6c61c4c7e`  
		Last Modified: Wed, 15 Jan 2025 01:17:10 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7859bf5ceab99e08f56fab223e441e8384e5e6f1230553cd3a9f54789e8dce`  
		Last Modified: Fri, 14 Feb 2025 14:03:56 GMT  
		Size: 12.6 MB (12562318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a146affdee6ec5d9e8a3913be4585c560688447416ed017d910a741085258a`  
		Last Modified: Fri, 14 Feb 2025 08:23:15 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6872ffd3b54fa4f6db105e06204b07ea083fb7a807a8aa126f8346648addf6ce`  
		Last Modified: Fri, 14 Feb 2025 14:23:59 GMT  
		Size: 14.3 MB (14288674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad63f2b22781eba9ef863d8feca02cac787f6d8348d0e5ed19cc1306ac1e686`  
		Last Modified: Fri, 14 Feb 2025 08:23:17 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f1e1e5385b5da5a48e7455b7aed09a59b7ad23be5fa7ef974336ce7b5ddeb5`  
		Last Modified: Fri, 14 Feb 2025 14:23:58 GMT  
		Size: 19.5 KB (19542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6e7583af15f6c93c280340797bc1c621c085a58359b4937daeab5a8da8f0a3`  
		Last Modified: Fri, 14 Feb 2025 14:23:57 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1705170ff1518dd1a4ac511686b2b0fb9e1f2f1a89181547f4b0e34713f5fb57`  
		Last Modified: Fri, 14 Feb 2025 08:23:01 GMT  
		Size: 1.3 MB (1275763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd0579400b55bbee00a411ac0b586512af0d98ee37397f108f420288619dd35`  
		Last Modified: Fri, 14 Feb 2025 08:23:00 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd762cb630e6b7fcbe32ab266cac7939610a67008973fca410e47fb5928b448`  
		Last Modified: Fri, 14 Feb 2025 08:23:20 GMT  
		Size: 740.3 KB (740347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ad6368b555e9d436a34a6b4ed27d2fd2a17adb326e53b2267141321d2d5cdb`  
		Last Modified: Fri, 14 Feb 2025 08:23:01 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27589cded3f799d489e08d8cf75b21a9d1992e6c86817bce87185947a27850e`  
		Last Modified: Fri, 14 Feb 2025 08:36:47 GMT  
		Size: 21.5 MB (21477390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:1446d38bae01d5c26ecdab98e2ff4666cc6ee1138d77328179f027ddb3262d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.1 KB (382072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb47e2b8aa8a1512f5941225ca903e214ffb1050bd30256da722fb8e7242992`

```dockerfile
```

-	Layers:
	-	`sha256:b5009e92d7abe55be8a9fc94a6b787493ece3c7cf72392da840645d6efaea7bf`  
		Last Modified: Fri, 14 Feb 2025 11:54:05 GMT  
		Size: 348.9 KB (348899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f879d3993ba8d0a0357c9cc9b3b6a6d7f8fbd354448197e12be7bdb2424a5af3`  
		Last Modified: Fri, 14 Feb 2025 11:54:05 GMT  
		Size: 33.2 KB (33173 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:cf80cc7fb623e6b5a38f89a2881d21925f76ed1bfc84ba067f1824ab02566d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60733946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c7d0a93b9a01b9703f98557960f24774efc22dda91f13479dc2aaeca150fe1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 06 Feb 2025 04:56:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Feb 2025 04:56:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_VERSION=8.3.17
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /var/www/html
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Feb 2025 04:56:28 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 06 Feb 2025 04:56:28 GMT
CMD ["php-fpm"]
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV DRUPAL_VERSION=10.4.2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a012054b09a479da7b89fdfed6a406dc49bbddfe6ede01999030c5686ef77ec5`  
		Last Modified: Fri, 14 Feb 2025 06:13:26 GMT  
		Size: 6.1 MB (6056911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae576db5a5893e862707f340f7cfb3cc47181a191637fa70a356b06367f08e2`  
		Last Modified: Fri, 14 Feb 2025 06:13:24 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d903f55b816dbb102327032041ddc48a91a8fb0084e5befa8e51b90b602a6e`  
		Last Modified: Fri, 14 Feb 2025 06:13:24 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3d3e1c8f45a761ba15dadc184ad88451eeed3cec044730a14568cf8d2fbea2`  
		Last Modified: Fri, 14 Feb 2025 06:15:48 GMT  
		Size: 12.6 MB (12562316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f35df0519eff35e764a7b74ee28c58261e792fc729e25995e17429de9cf8fb`  
		Last Modified: Fri, 14 Feb 2025 05:11:12 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc65c407a748f576ac3cbda1c9694b49b7fdfd1022876c19fc92df6fedaab66`  
		Last Modified: Fri, 14 Feb 2025 06:15:49 GMT  
		Size: 13.6 MB (13593811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc256ae81d89801226b32ffdd9bf4fa846d7742cca86a05d04a81582f797ffbb`  
		Last Modified: Fri, 14 Feb 2025 05:11:14 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19344d2b4f6f2fae0ced57fc4ce075387d006cccfedef320a05b25c0050a49db`  
		Last Modified: Fri, 14 Feb 2025 06:15:49 GMT  
		Size: 19.5 KB (19521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614da42c534dc4b248d5694111ce51892a8410c44735bfc35ddf480329c16c26`  
		Last Modified: Fri, 14 Feb 2025 06:15:50 GMT  
		Size: 9.2 KB (9174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002f25fc5733d7a7730b5f62c3381ba77bdeed05e1802f3e829ae9b6e0aed663`  
		Last Modified: Fri, 14 Feb 2025 17:39:38 GMT  
		Size: 2.2 MB (2178841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92cbe169df19b9f2affb1959551d139f9fd5596c8da042b660186f75818aa88f`  
		Last Modified: Fri, 14 Feb 2025 17:39:38 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38421ee5bbcdcfc727f7947ceada9d843061c568e63c5b6649a8d4d538e25644`  
		Last Modified: Fri, 14 Feb 2025 17:39:38 GMT  
		Size: 740.3 KB (740348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a487d07c5184341c71810c91f04365df4acd8e6cbd06061ae4dee3d849c84a86`  
		Last Modified: Fri, 14 Feb 2025 17:39:40 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb4235854ab8be4ebf18683958cb39a5e55a102872de3d6baf19f8c885c0fda`  
		Last Modified: Fri, 14 Feb 2025 20:26:45 GMT  
		Size: 21.5 MB (21477707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:759846e41823014a001aef28eec834ace047aa69c09d3429d59c1123ba834f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.1 KB (382144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4e9a989d298efd59bb908867ad833d1d8c852bea39ab9b95f2f925a6132613`

```dockerfile
```

-	Layers:
	-	`sha256:4f9143f4159d91edad382d8df264e325b1fb1715cf23510f4b084cf972162bdf`  
		Last Modified: Fri, 14 Feb 2025 08:55:04 GMT  
		Size: 348.9 KB (348927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87645621aabd793a4e6cfc259d9b232c17a3d4a97626e221a4047a32029a876d`  
		Last Modified: Fri, 14 Feb 2025 08:55:04 GMT  
		Size: 33.2 KB (33217 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.20` - linux; 386

```console
$ docker pull drupal@sha256:290d296782036514ce4456423bbb797ca7907bd893a62a3df9ab1860b12dfc16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57057262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97f30ef14ba4d6f3ba18bee6759741b951cf59ce41412cb2cfd68e18ea20297`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 06 Feb 2025 04:56:28 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 06 Feb 2025 04:56:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Feb 2025 04:56:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_VERSION=8.3.17
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /var/www/html
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Feb 2025 04:56:28 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 06 Feb 2025 04:56:28 GMT
CMD ["php-fpm"]
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV DRUPAL_VERSION=10.4.2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 14:36:27 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be7da3a37896810032471dca61d7b37df7b82457048f54f6857c6918382b177`  
		Last Modified: Fri, 14 Feb 2025 21:11:32 GMT  
		Size: 3.4 MB (3365476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97109000417d533271fc4a2ad66346eafdeb62d23b78492e509c5dee65477df`  
		Last Modified: Fri, 14 Feb 2025 21:11:31 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655f47680e3f316fbc69faf89c019af79f97048b1cff0ebd5efcf425c80ea144`  
		Last Modified: Fri, 14 Feb 2025 21:11:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1a828ef6fc1feab03b2544b1151ca2247678e13a86f2c65c55ad19dd45b2a9`  
		Last Modified: Fri, 14 Feb 2025 21:11:31 GMT  
		Size: 12.6 MB (12562316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1374639b2645c4bd99c538944d5f7374533071cab15baa4b3a15e473219e1b6a`  
		Last Modified: Fri, 14 Feb 2025 21:11:31 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08734cb6e9d3e38397b7c399a6f9d58adc20bd6e8eb5010c59ff6bb0746395e2`  
		Last Modified: Fri, 14 Feb 2025 21:11:32 GMT  
		Size: 13.4 MB (13443434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe0e8ab3968e3b6625e61ddc5bac9884b4787bd9f852b38a8c9ab8b7c00c373`  
		Last Modified: Fri, 14 Feb 2025 21:11:31 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dc4d43e032a6375b8c1646fac4f59afd274d643f956b440fd14cac827f800d`  
		Last Modified: Fri, 14 Feb 2025 21:11:31 GMT  
		Size: 19.7 KB (19705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394ab8140e6bd38c624efcc05f3133e7d26dab76a940d4532bcde8f6303f055f`  
		Last Modified: Fri, 14 Feb 2025 21:11:31 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab4dcb5e734447ad3df2778a1bd69d3a6088de9ed4266c50cfeeb6adaa134dc`  
		Last Modified: Fri, 14 Feb 2025 21:14:44 GMT  
		Size: 2.0 MB (1962884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583fb80556c5e6518acecac775825f55e29f502c9a4d3297d7209a5ed4364b09`  
		Last Modified: Fri, 14 Feb 2025 21:14:44 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc9b24c9c06a1ee6364b4ca1e9f9be395867b881a1c383cceec84fc999f8208`  
		Last Modified: Fri, 14 Feb 2025 21:14:44 GMT  
		Size: 740.3 KB (740347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a275d9bec0f470c66d8ba72199528d27e54a0cb81a81b4e6b410e162c13649`  
		Last Modified: Fri, 14 Feb 2025 21:14:44 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5aee9770ee1bbc73f2dd47ad0a886fdde558a3dbc62b3ef1d5ffd6ec11b8d86`  
		Last Modified: Fri, 14 Feb 2025 21:14:45 GMT  
		Size: 21.5 MB (21477695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:e02394581111d74125eb5117b01f1648496d4cc70f4dfd431475f964794db647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.5 KB (373531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d665a4b780c7c01945ce2befcbdf8c48d070630bf073e0c7d6c313da921a73`

```dockerfile
```

-	Layers:
	-	`sha256:85c04da7b84c3dfb0104b2e5cae572e847cdcddb226d59ea5d5bef3282163e72`  
		Last Modified: Fri, 14 Feb 2025 23:54:13 GMT  
		Size: 340.6 KB (340552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9634b0febb763059cb22596c12839684dd80056fc0cd8b10109399671629235b`  
		Last Modified: Fri, 14 Feb 2025 23:54:13 GMT  
		Size: 33.0 KB (32979 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.20` - linux; ppc64le

```console
$ docker pull drupal@sha256:0adf4d36f0b1118b787a195aea0d509ba581e513401c62cc614e1a292ca352a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57119119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10218e37c6c9a8782f302c1303c1d5da5eafed4e944d1d80784af85bc9467b57`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 06 Feb 2025 04:56:28 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 06 Feb 2025 04:56:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Feb 2025 04:56:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_VERSION=8.3.17
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /var/www/html
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Feb 2025 04:56:28 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 06 Feb 2025 04:56:28 GMT
CMD ["php-fpm"]
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV DRUPAL_VERSION=10.4.2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 14:35:49 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718db6fd9663f5523b8df9dc0bcd9d39b076fe66cbf8b070276f7f03946d69a3`  
		Last Modified: Sat, 15 Feb 2025 02:57:24 GMT  
		Size: 3.4 MB (3440270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a6b0a520a6ed496f43bb191ac088029379c10ac94401a28b7441591d37bfae`  
		Last Modified: Sat, 15 Feb 2025 02:57:16 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d31ee6d075a91e74c7b2a672c463e871265f9016719d4905ed788b321d083a2`  
		Last Modified: Sat, 15 Feb 2025 02:57:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9cc3628bfe7b1fbfbf739a83197658f2c1dc93e5c9f1fc86bfc586bc2072c6`  
		Last Modified: Sat, 15 Feb 2025 03:17:26 GMT  
		Size: 12.6 MB (12562323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee5f188ccc6aa29ccd00dd57fb19498f57a80acae57aeaf4b987d620ed0ad2e`  
		Last Modified: Sat, 15 Feb 2025 03:17:24 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9b7deb94ccbefba8a53022413eeb67ed1f124e18cbb24d6d9c6ed956fa146d`  
		Last Modified: Sat, 15 Feb 2025 03:25:49 GMT  
		Size: 13.6 MB (13609603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f834236f7326a0cdc1d61cc9c4406edc62db6464cd263e3827f680e2c0b1f81`  
		Last Modified: Sat, 15 Feb 2025 03:25:39 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0877d4c45d2eefbd9fac9ea9f7da19a475223a854f0f480927cceb775f6970`  
		Last Modified: Sat, 15 Feb 2025 03:25:40 GMT  
		Size: 19.5 KB (19478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a232f6c5243e6d7a522883f9be6b2f4b7dba17a809201a745b9f8763bed289fc`  
		Last Modified: Sat, 15 Feb 2025 03:25:08 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594b8f15d28753769866ce76acda7534ebc09425b0683d652fbb2c0db4c915a6`  
		Last Modified: Sat, 15 Feb 2025 04:46:05 GMT  
		Size: 1.7 MB (1680202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffaf22f7316701c61d505727d53fd8f5b481dcc1250fcf593b55770881ac6f21`  
		Last Modified: Sat, 15 Feb 2025 04:46:05 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c1e3a6760cbd96c0c4951bdbf9c118cae799f8c7be14c4ef0e9a3ff303e146`  
		Last Modified: Sat, 15 Feb 2025 04:46:05 GMT  
		Size: 740.4 KB (740351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad30715fafe74db204332589fe0ed84c871d4364b4e09dba8f88efd1875cf1f3`  
		Last Modified: Sat, 15 Feb 2025 04:46:05 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea36cdb3c1a94590e8601e8e0844149c7f8f86d59b5d854796c4349ce138dc1`  
		Last Modified: Sat, 15 Feb 2025 04:58:47 GMT  
		Size: 21.5 MB (21477468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:9cb95754f6fc6c5e4d85f92d723ddaf67ae609d650133b6e6da1b530746a4bfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.0 KB (379023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a243103a6791896954c576257db81d93958d57294681c0ec20d31c74ee5e6d48`

```dockerfile
```

-	Layers:
	-	`sha256:32b532de2a815562f74b25fedc0c9e89c9ca7016f6f742880ca683ae5304ebdc`  
		Last Modified: Sat, 15 Feb 2025 05:53:42 GMT  
		Size: 345.9 KB (345921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be298259e0a0ffd3d7b58ee958cb9dddb76fe0d655b8a268a4c331d33628619e`  
		Last Modified: Sat, 15 Feb 2025 05:53:42 GMT  
		Size: 33.1 KB (33102 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.20` - linux; riscv64

```console
$ docker pull drupal@sha256:32cc93da9835e1c37829b189c0c9617a115ea56ca593e425ce257f5aac218ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55775530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1db2f6f11c9426db134f4049eaa4608854e6a01eda1568f525375005c161fb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 16 Jan 2025 17:19:20 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Jan 2025 17:19:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_VERSION=8.3.16
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Jan 2025 17:19:20 GMT
WORKDIR /var/www/html
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
STOPSIGNAL SIGQUIT
# Thu, 16 Jan 2025 17:19:20 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 16 Jan 2025 17:19:20 GMT
CMD ["php-fpm"]
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV DRUPAL_VERSION=10.4.2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Tue, 14 Jan 2025 20:50:16 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ec415e9e84f4fbfdf631ed4f49ea5fc3b66ea4fc7dde02b872f6bf80473254`  
		Last Modified: Wed, 15 Jan 2025 01:17:11 GMT  
		Size: 3.4 MB (3428298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7afa983c26aef0c7fdf0b220c994bbc1954adaf863d01d1a09ad7b531a485c`  
		Last Modified: Wed, 15 Jan 2025 01:17:46 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d306623b924639b3cc48ee24fd37021ee4b75400a0afd7d21003ec0fced66d79`  
		Last Modified: Wed, 15 Jan 2025 01:17:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c72e05aeaece2f9593e9ea8e88095c7de654bfdb144e7f921c7c3f8ba5e441f`  
		Last Modified: Sat, 08 Feb 2025 09:58:28 GMT  
		Size: 12.6 MB (12565705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ff74cc236318854e9d412a0075895d62aef3200169c91390cf0ea5d85367ff`  
		Last Modified: Sat, 08 Feb 2025 09:58:27 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6915b828db22d22a03fc8b558c4b07781c28228e4d34d9e2d780df8b2f4a2aea`  
		Last Modified: Mon, 10 Feb 2025 09:58:33 GMT  
		Size: 12.7 MB (12674659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a092d6f542b7073a583fec771c62288ba4a29bab3e092477eba10af403672a`  
		Last Modified: Mon, 10 Feb 2025 09:58:32 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134c9326105f9646fcbb9d5caa6613f42904fb33281f469442969e016f678ee4`  
		Last Modified: Sun, 09 Feb 2025 09:58:33 GMT  
		Size: 19.5 KB (19505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0950e2bc41ba4c2f78942a3514583458beee0699206a2bd30f538f6c13fb543d`  
		Last Modified: Sat, 08 Feb 2025 09:58:30 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4042894d7fa82543456394f2be9fba90ac8329d99b3e81b8d9a378e73abe97f6`  
		Last Modified: Fri, 17 Jan 2025 07:48:58 GMT  
		Size: 1.5 MB (1483307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062461ae42c12f602c9465ce0e18f96437600a34be3bc3200d7be13ddb40626c`  
		Last Modified: Fri, 17 Jan 2025 07:48:57 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff9377f7ffc37b9db7b153c93dbe0dbaf6c74fe72381c531bbbdad7390f0963`  
		Last Modified: Wed, 22 Jan 2025 00:33:21 GMT  
		Size: 740.4 KB (740353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d6405c4c2d32b019ee95b5cbb4f6f7ae28a8bcf19fed53444f7a612b9daa4c`  
		Last Modified: Wed, 22 Jan 2025 00:33:20 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738d9d2cbdae40389a1719032b9c0499adb2e66c7964515c1f749808883decdf`  
		Last Modified: Fri, 07 Feb 2025 00:49:03 GMT  
		Size: 21.5 MB (21478026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:885b78e0ad7bb130ee4a120dc7da0e8a48dcadbe2123f4d00aadbffeb63a62f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.0 KB (379020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9634fdea7626d75cc38c397521489946da2009544b3181ae0d77ae941fc84b2`

```dockerfile
```

-	Layers:
	-	`sha256:a0835e82e624ea815c5165200bf6d33d14f755ed180ffbebe78282c734ae5f4c`  
		Last Modified: Fri, 14 Feb 2025 08:55:09 GMT  
		Size: 345.9 KB (345917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2ffa3e1f15bb4ace3ab6c6626912700ae2ea999bd73bcd0617e89fe81ce3d83`  
		Last Modified: Fri, 14 Feb 2025 08:55:10 GMT  
		Size: 33.1 KB (33103 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.20` - linux; s390x

```console
$ docker pull drupal@sha256:113fdb3d2407aeee4abaa10a4d2f3a6ca6d8fc0fc9641b183bdac095aa36e1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58932824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93e1a1a1bffb11fbcb89f9166b8b9c46526d15e3758cd08629199251b276bc4f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 06 Feb 2025 04:56:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Feb 2025 04:56:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_VERSION=8.3.17
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /var/www/html
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Feb 2025 04:56:28 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 06 Feb 2025 04:56:28 GMT
CMD ["php-fpm"]
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV DRUPAL_VERSION=10.4.2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Tue, 14 Jan 2025 21:25:41 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ecaef0d937f8f44f5017ca7434ceed25aca975e17c25c88d775e4d21c82d1b`  
		Last Modified: Fri, 14 Feb 2025 14:04:07 GMT  
		Size: 5.5 MB (5540736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd12500978718dcc411c7c16a51cfd5c01a014f06442078ee5faa87690b46e1`  
		Last Modified: Fri, 14 Feb 2025 14:04:05 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfe074ab17faa218470d2ac5bd465667ebc44aa16124dc08938103b283e6b15`  
		Last Modified: Fri, 14 Feb 2025 14:04:06 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597c8c0a09894c330bf8fe6ac7f3d3e054bf35efce0306061ebecfb75e65dd5f`  
		Last Modified: Fri, 14 Feb 2025 14:04:06 GMT  
		Size: 12.6 MB (12562319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d988b1a8a4e40a4991caec31bdd63cd6b57bb286e1f2b2cea36246b67084b42f`  
		Last Modified: Fri, 14 Feb 2025 12:23:12 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66764dd236ecd514937927f64f6e449aa3af0349d650fc2b1e1198ba0ecbe674`  
		Last Modified: Fri, 14 Feb 2025 14:24:08 GMT  
		Size: 13.5 MB (13518357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6888fb4acfdc50e26fb97bc88b5e7069fedb990c2362fba12bbffa61c30b6c7b`  
		Last Modified: Fri, 14 Feb 2025 12:23:15 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800bc5807b4545096eacb1f4e882e5eddb125852d95773813fba030098593972`  
		Last Modified: Fri, 14 Feb 2025 14:24:08 GMT  
		Size: 19.5 KB (19526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf67f0c6bba01f8879c9c4a6275ecbc8c11c295ef5226001b56d5e58db4ace7`  
		Last Modified: Fri, 14 Feb 2025 14:24:07 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40e1429019ab430be779eea17fb093d45ec19db3ac002ea293faad3316593cd`  
		Last Modified: Fri, 14 Feb 2025 10:25:28 GMT  
		Size: 1.6 MB (1596816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b563e55861dd05eddb515c1f49015390ef0e07f588ec9b4440f291730fffe27`  
		Last Modified: Fri, 14 Feb 2025 10:25:28 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ed3180c7d97baa13be3b03c6d9a1f001451702e353e85961eb44be41c9f6d3`  
		Last Modified: Fri, 14 Feb 2025 12:23:19 GMT  
		Size: 740.3 KB (740349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41faee2811b041ebb6dad5b25a531677428f98c38162e2b08bc9f321dcff6a38`  
		Last Modified: Fri, 14 Feb 2025 10:25:28 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bf13cde983afc4082ac4aa2556dbc78cc27142dc049760e8dea6b1db97c7f4`  
		Last Modified: Fri, 14 Feb 2025 10:39:54 GMT  
		Size: 21.5 MB (21477658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:f1edb97c5c688ec99b95548bbe22c4021eeb5c5ddce786c669a5e3a3bbaf22d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.9 KB (379929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba58f477a7c9084489c622d5b1bc91fec17865e23fb89ef10f3829eaa89af60`

```dockerfile
```

-	Layers:
	-	`sha256:de9cf49db8900dcae194d2958271ba34fe3c61ffa231e734c078e81cc6e3cfc0`  
		Last Modified: Fri, 14 Feb 2025 11:54:12 GMT  
		Size: 346.9 KB (346896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2eb50b3f807f36d7907bb38edca50dd50a6828d8b34874df1203f7fce17038`  
		Last Modified: Fri, 14 Feb 2025 11:54:12 GMT  
		Size: 33.0 KB (33033 bytes)  
		MIME: application/vnd.in-toto+json
