## `drupal:10-fpm-alpine3.20`

```console
$ docker pull drupal@sha256:aa3c763d322eedab915f69fc530e1e831fdc45cb870d61c84e687c6fb1fd9252
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
$ docker pull drupal@sha256:ef9c04d3a52e2bf34a3767eaef74323b20c925c6eeca7230685c06d4603ba365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54807601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621731cb3a370cb9a2895e288efad6d943190d86f9fe67760ab25c994b187620`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 06 Feb 2025 04:56:28 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
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
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 19:26:24 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c0f79d4d985a64f9865dca6388accc72536a8134bb71d173eb4214c357889d`  
		Last Modified: Fri, 14 Feb 2025 20:55:09 GMT  
		Size: 3.3 MB (3298263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ffe6d763475cabc6526162b5d931425de2a4941987a9a47a37817994c917fe`  
		Last Modified: Fri, 14 Feb 2025 20:55:09 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82be80b03c756f18e75ec416857bff7aeee3ead6c2ab8410c9194efd506877e5`  
		Last Modified: Fri, 14 Feb 2025 20:55:09 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34217164760f6be22d8ec7735612bc02dd51f5191016895fb2d7461a3a78cfa2`  
		Last Modified: Sat, 15 Feb 2025 00:04:06 GMT  
		Size: 12.6 MB (12562323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fb490e80d16856484e5315f71dd41a682a2e1448cbecd3a25a6edfde94f379`  
		Last Modified: Sat, 15 Feb 2025 00:04:05 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8b230adc77596691c935be252109268dfb10c9ced404fc0075c7233bc09d45`  
		Last Modified: Sat, 15 Feb 2025 00:05:06 GMT  
		Size: 11.9 MB (11937644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e708efe43b818dc378157d0041841e091ce77d47ed34f635e0cdc5c955fdb3`  
		Last Modified: Sat, 15 Feb 2025 00:04:44 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24cae198e1d6234d1c361b16ccb64d213676125f6fa61d359102fb92f3fe00f`  
		Last Modified: Sat, 15 Feb 2025 00:04:44 GMT  
		Size: 19.5 KB (19498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a0b562378dfa4d95fed09d7e93def94b0829837fd7b38e407946c7bacf801e`  
		Last Modified: Sat, 15 Feb 2025 00:04:44 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7cde61f273d2e1ffa4f6bde0a93edc7611e24f632a04c7b76cbf28081c3531`  
		Last Modified: Sat, 15 Feb 2025 11:54:12 GMT  
		Size: 1.4 MB (1385456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ef1be317b0480e349f2703bbd96e21a3939dc7961bea279ddff6d3c5af8dc1`  
		Last Modified: Sat, 15 Feb 2025 11:54:12 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555d35d48d3c57f0b4524efabe211377faa6534b9a4dfb55320e721f163768fb`  
		Last Modified: Sat, 15 Feb 2025 11:54:12 GMT  
		Size: 740.3 KB (740349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7138b48b96cd65e52b7f0ca8bf67e81733725ac03f2747297b3211a21ede1ee`  
		Last Modified: Sat, 15 Feb 2025 11:54:12 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcecab91c515332d606602a05b333335eef211c0544715e0e8020e0aa9013f29`  
		Last Modified: Sat, 15 Feb 2025 11:54:13 GMT  
		Size: 21.5 MB (21477797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:c84c8dacd09604fa9843f8c37d71de799e9049ecfd167d8495fac12ff291be64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 KB (32957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61abae407e8fdbbb3a6bedf53345f65d055a3c089c8eeb5ccce0bba451dc8194`

```dockerfile
```

-	Layers:
	-	`sha256:d5b61c2b3223bea68da844d30f2e3560554a89b4165a674d959bc6754891eb10`  
		Last Modified: Sat, 15 Feb 2025 11:53:50 GMT  
		Size: 33.0 KB (32957 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.20` - linux; arm variant v7

```console
$ docker pull drupal@sha256:d794d0757319719a68abd7a5122c9cb9954a1a93cff207b950a24c737af29315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53479308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4fc715c57ab3f9bc74d1e23c0e28e123f9af2ee12b064ca5c08dd5a1528938`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 06 Feb 2025 04:56:28 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
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
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 14:35:10 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f435e04ea18170faa15db5a195b7a456fd6855803819a3ec1feb1150cc547b`  
		Last Modified: Sat, 15 Feb 2025 02:56:28 GMT  
		Size: 3.1 MB (3104652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6d965c1f9e2eeb816a67542a273f236e46e8776d2aaeabebc43098c502ee68`  
		Last Modified: Sat, 15 Feb 2025 02:56:21 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151a378a33b3d6443d5e2151a40e50e2c7f67f3b501115627d75e1ce417f91c7`  
		Last Modified: Sat, 15 Feb 2025 02:56:23 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b8d9070f2a1427c9c6ad3950e94b3b7173ecbecdc2b824ebc2eed65ed6a594`  
		Last Modified: Sat, 15 Feb 2025 03:16:08 GMT  
		Size: 12.6 MB (12562310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e8c12c8d91a1abcba6e8a4dc60d3df2c2a39eb034789999c4fb75a1dc6e508`  
		Last Modified: Sat, 15 Feb 2025 03:15:55 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483af620c3604af4147591e876d23cc7bb27035c8ef68a58d031a35776d9330e`  
		Last Modified: Sun, 16 Feb 2025 04:31:00 GMT  
		Size: 11.2 MB (11189413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379f9af1d362db038bfbc4afbe58783e5a56614217fca50773e11a2b4a1ffefd`  
		Last Modified: Sat, 15 Feb 2025 12:08:10 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778c21eb7237011a9e94d57bd17229ebe9b9f42f9d6f99bbaa968d703662af35`  
		Last Modified: Sun, 16 Feb 2025 04:30:52 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff406130a3af5939fb66852c9a891250997ed181e8200a727aedfa6cfcdbe8b1`  
		Last Modified: Sun, 16 Feb 2025 04:30:48 GMT  
		Size: 9.2 KB (9175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92941bd4b638601f34c3fe648d94624475b84a80cbfc0e57096f10483dd3810`  
		Last Modified: Sat, 15 Feb 2025 18:19:46 GMT  
		Size: 1.3 MB (1275679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4502310abaa921b858ed94e5bec7487e07b05cf6b7d6d511fcb2ab04ef8e59`  
		Last Modified: Sat, 15 Feb 2025 18:19:40 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffb64693004de8939b5e0c46eea47907905428c805ca612f00f1f3b21b20fb8`  
		Last Modified: Sat, 15 Feb 2025 18:19:45 GMT  
		Size: 740.3 KB (740348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c71c6c74118349ce01250b5061ec311bf6ba319ce83a2be7154a55ea5e34d6c`  
		Last Modified: Sat, 15 Feb 2025 18:19:40 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8ee6185144ba71436f5f4b2c790dbf26a6598e5226cd86ac95d30bc9595530`  
		Last Modified: Sat, 15 Feb 2025 18:33:16 GMT  
		Size: 21.5 MB (21477709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:ee5c30341f40e9a624193f00ae9af53e70448fbfccaa99757bb3dee9517cb497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.0 KB (381049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afac2212ded2a1e1a143fb88819566c21585703db3545fd6e442785eac71c5b`

```dockerfile
```

-	Layers:
	-	`sha256:965c9c676ee33329d5ab39b2df4a05ff735d9096e8b6006b6c16912593a42e0c`  
		Last Modified: Sat, 15 Feb 2025 20:53:40 GMT  
		Size: 347.9 KB (347878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d39030941560e7bd948e5bbb73f2e8845bdc7d3f3f99498c1c0cecd243984bf`  
		Last Modified: Sat, 15 Feb 2025 20:53:40 GMT  
		Size: 33.2 KB (33171 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:5c9a2adf53a8471e233f34c6154a871eff5ab206070d4315ac99b1b8ecde9869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57617311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a52e511d1adeb2f5ab1f017010c16b9f47afcdd05a70f714778b11d144ba521`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 06 Feb 2025 04:56:28 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
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
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64278622ee4008648cd0d08a890af70672bfae53a983eb2b10fe4a65ed3b936`  
		Last Modified: Sat, 15 Feb 2025 00:15:22 GMT  
		Size: 3.4 MB (3365209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95666ce1b88aa4cfd448a2dfecfe7a221115807ae27fb0bd41f2d5920815884`  
		Last Modified: Sat, 15 Feb 2025 00:15:22 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa970535345bac62ab689111e4438c3ed5b2c57f743763f4381c198f307d845`  
		Last Modified: Sat, 15 Feb 2025 00:15:22 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d749b46d4e133af221f9d0cdd8027a5e2e94098522d3d04fdd6713a6ba8921b5`  
		Last Modified: Sat, 15 Feb 2025 00:15:23 GMT  
		Size: 12.6 MB (12562312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09b6c9bd016c4712b17c7f14a3d304159c49236e6b2f4fb7b5b2aad89f12ea3`  
		Last Modified: Fri, 14 Feb 2025 22:39:12 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e989ba145dc6522cfc3d2136b7082224d5cfbdfc3c4307e2695b96f87b5d608`  
		Last Modified: Sat, 15 Feb 2025 00:15:24 GMT  
		Size: 13.2 MB (13168494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1a0336795b9c867ebcb83eaec19767d12ba54cec823bf0da480c572487199f`  
		Last Modified: Sat, 15 Feb 2025 00:15:23 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec31fc86977c0071686e0b96bb01ebb51596d43a25839231038113f360e0652`  
		Last Modified: Sat, 15 Feb 2025 00:15:23 GMT  
		Size: 19.5 KB (19476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7cc5fadae4f289a2c0590e13fe8d44de85c6ad61bf2b9401e4b118a8696369`  
		Last Modified: Sat, 15 Feb 2025 00:15:24 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa2bc2e4f8467fa8e0d27209b49aefb925c934c45ce4a02c9c65b141fa9de0d`  
		Last Modified: Sat, 15 Feb 2025 21:16:03 GMT  
		Size: 2.2 MB (2178824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e9bf0e64686bc527e5e52fc4f2baa7af248f525736bc1e6252fd98c2d279d6`  
		Last Modified: Sat, 15 Feb 2025 21:16:03 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308a3b44e767941777d32e6416cad6342c125970e9474b6a22d8e7bac05454d7`  
		Last Modified: Sat, 15 Feb 2025 21:16:04 GMT  
		Size: 740.4 KB (740351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c2ad8f138ee90bd1472371062cf392118601c0b6a5de4823dd77406540e79c`  
		Last Modified: Sat, 15 Feb 2025 21:16:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfd819c5facf350860042a65ed19922c3d1c7da9b3e471a29be4c883b9d104d`  
		Last Modified: Sat, 15 Feb 2025 22:26:02 GMT  
		Size: 21.5 MB (21477758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:3e921e5c8a85046929f848ac5aa53a460013b5610dbe60ff5007ed1f162252fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.1 KB (381121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c0c2062a267cc403057129e4d92a406171febd4049a7309b9c750100304d0f`

```dockerfile
```

-	Layers:
	-	`sha256:c4624d65ca573c2a0bb9d7ef9c6964ed758bbf8d5253ebb0b32b9cea47bf8b73`  
		Last Modified: Sat, 15 Feb 2025 11:53:53 GMT  
		Size: 347.9 KB (347906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:967f383871be9a98df00105b77afc936ba00eeb338a211142527492486b457de`  
		Last Modified: Sat, 15 Feb 2025 11:53:53 GMT  
		Size: 33.2 KB (33215 bytes)  
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
$ docker pull drupal@sha256:1aca32375d1cc10b79a9f0b50f4ad25d8156c11192d584308732a42de9e8367f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55778347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d25bc08ce92cd0671209ec6575c4fa0969b67dbf0d8413e589c5c2e67c4e614`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 06 Feb 2025 04:56:28 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
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
	-	`sha256:69ccf1207daf2e3c381041f63cfe024189987fde3b1e97110475a71eac2581ba`  
		Last Modified: Fri, 14 Feb 2025 19:30:36 GMT  
		Size: 3.4 MB (3373232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f78faa668cf7c574dd9c2d56f59a6bc250dc74af7e4e18fd9791effe1480d2a`  
		Last Modified: Sat, 15 Feb 2025 14:08:16 GMT  
		Size: 3.4 MB (3433648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb3f638d71f849a7c907c65e1460552ada965ad760ca4f24c59cf89e1f65e23`  
		Last Modified: Sat, 15 Feb 2025 14:08:16 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87af6ac6ee454c1a8ef152ca8385e86f0d68ce72adae1c15b5ce36f9a3634e22`  
		Last Modified: Sat, 15 Feb 2025 14:08:16 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d84700f6490a1fd53d640e854d1bf0dab8bad442da594ee21e668e6724b269`  
		Last Modified: Sat, 15 Feb 2025 14:08:20 GMT  
		Size: 12.6 MB (12562321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23699771066adcd77eb5e57e69b7c10efc3098c075bf8a4fbf82058231fc11ba`  
		Last Modified: Sat, 15 Feb 2025 10:07:56 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e385f85a50b7a40cc81ea17fffdaa894fca4439673804e5be19dabfae6040e87`  
		Last Modified: Sat, 15 Feb 2025 14:09:32 GMT  
		Size: 12.7 MB (12674598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc176eb1269f3b74b384e367002c22f8ab18c5470df2ef0603d3a609b6015a2`  
		Last Modified: Sat, 15 Feb 2025 10:07:59 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddc27d9273296296ee7bdf5e9cbc1bb45c909707acf1f7eef9721e7028c8048`  
		Last Modified: Sat, 15 Feb 2025 14:09:32 GMT  
		Size: 19.5 KB (19499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51e3cc958698520e44563eaadaada66b69c0901298d044bd0781697e6b7c9b4`  
		Last Modified: Sat, 15 Feb 2025 14:09:31 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c8ef26bc3f6f7f7ac14bf81e80777a5cbeae2108a729db12a0a2e5e544cba0`  
		Last Modified: Tue, 18 Feb 2025 16:49:45 GMT  
		Size: 1.5 MB (1482883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26b959e9161430d0ba900ca8fb4b78582e46767c12335505c5c8d7ecbc9337e`  
		Last Modified: Tue, 18 Feb 2025 16:49:44 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536b8a4a772876492f5f0c00172b17ab4fe34f3a0184bad62d008b7b2195908b`  
		Last Modified: Tue, 18 Feb 2025 21:01:46 GMT  
		Size: 740.4 KB (740350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67038f142c0c9d867446ebf56f72c67bfed465a5fadb4494d41fd20a53f1310c`  
		Last Modified: Tue, 18 Feb 2025 16:49:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ca759edab6384a29c4e2fb03559b1e9d4cbb12862cef60aa58fdb0038daaf8`  
		Last Modified: Tue, 18 Feb 2025 17:12:47 GMT  
		Size: 21.5 MB (21478063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:252a1698bb5697a504e2f855138336dd90ed6dea4225983226bdae460842ced2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.0 KB (379019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288c91f2cdcf5d3285e6ae40007f3bfb9a73f2b89b1a3731d1283d365b7ff4b0`

```dockerfile
```

-	Layers:
	-	`sha256:c93225a1997469bc4d3b35884c877c73bb4c72e0c82745c0922fad41f40874c1`  
		Last Modified: Tue, 18 Feb 2025 20:53:42 GMT  
		Size: 345.9 KB (345917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daf92dadc6fcbe4957a4c2feba6a57761c8aeeb8e64cd9901b106bb3b2dc91b1`  
		Last Modified: Tue, 18 Feb 2025 20:53:42 GMT  
		Size: 33.1 KB (33102 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.20` - linux; s390x

```console
$ docker pull drupal@sha256:5b7cbd57db2f8e9544841d8c8970f9b864c1c4e8de1f38d36674b6b02edf926d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56453884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22818697667add2cda4158af3339591221e1c2054732eb0c94c70a3e6898eb4a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 06 Feb 2025 04:56:28 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
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
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 14:36:22 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4683ab30aba68efec0e2ca4cbd43732f742f065f5166f0823fccc53a1442ec2b`  
		Last Modified: Sat, 15 Feb 2025 02:57:59 GMT  
		Size: 3.5 MB (3507248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51174c28ade76e443d57a717e1e8717bf8083c3163cd3db4d02012e3c317ecc1`  
		Last Modified: Sat, 15 Feb 2025 02:57:47 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b8be851aac921eca8fd7c62858736f1ef819ffbcf1db33078cfa5c544a77a1`  
		Last Modified: Sat, 15 Feb 2025 02:57:50 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad6da25422170c4eb7ec0ab8d65395c8bef2c8dd4fa8b32bf7894f876d7b973`  
		Last Modified: Sat, 15 Feb 2025 03:16:59 GMT  
		Size: 12.6 MB (12562308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b265ed5607bd963bea16ae9a9a01686d5c7c2aff2cf3a240cf8cd6f2d042ed0`  
		Last Modified: Sat, 15 Feb 2025 03:16:55 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9863110ffce96e5542d8bc1181eb3b2e2189843ffef535feef62b25e94fc1a9`  
		Last Modified: Sat, 15 Feb 2025 03:26:02 GMT  
		Size: 13.1 MB (13072226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b743e98f3582b1b0b15617a9ca92a385b5321a59cddd6ce098e800c6b11aabfb`  
		Last Modified: Sat, 15 Feb 2025 03:26:01 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3270805a23d0d645b194009fb507b84cd4a0bad4c679c1c05f4e42861ec07137`  
		Last Modified: Sat, 15 Feb 2025 03:25:09 GMT  
		Size: 19.5 KB (19484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcffd3b35b2f0476c1672f2a79f6d96b432ee0f9cc50d5d78ff53e5c673b2dad`  
		Last Modified: Sat, 15 Feb 2025 03:25:07 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785d1858819497b26dd028b0efe06858de2b3b54091798154dc38f744e7b3c2c`  
		Last Modified: Sat, 15 Feb 2025 11:12:05 GMT  
		Size: 1.6 MB (1596761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042183a14925334c7e4a16f5744214305e1521d36aaad7511c106a56fd56a5cd`  
		Last Modified: Sat, 15 Feb 2025 11:12:05 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e678e072711b40ddb7800f9afdc022dbd6c3588468a4a073d25fce8ffd366f`  
		Last Modified: Sat, 15 Feb 2025 11:12:05 GMT  
		Size: 740.4 KB (740350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdd91c6b330437b62c7c9698e8bb8b2cefb29fa38cddaa86b1b0272caee16b7`  
		Last Modified: Sat, 15 Feb 2025 11:12:05 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385bfe68b7d46414629413aef54d692d771e8dddd0bd182c08a418a498f480d0`  
		Last Modified: Sat, 15 Feb 2025 11:24:07 GMT  
		Size: 21.5 MB (21477645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:894a91600d64004b6e69ce13bec4dadb611e8635134911606b372f61b47a8316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.9 KB (378907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394c0a76fc6d190f78c67b4fd81b5f0b301e991dd9d08c7e32c4eff4f6d768c5`

```dockerfile
```

-	Layers:
	-	`sha256:8689d5512834abbf79c2291f1033ea4624d6c1f73b788425d5fdc946db52b38d`  
		Last Modified: Sat, 15 Feb 2025 14:53:48 GMT  
		Size: 345.9 KB (345875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04e5212d05c8cd32115ce789ddb9c7cc4562d539e9befe9a52631f58b2a1d6e9`  
		Last Modified: Sat, 15 Feb 2025 14:53:48 GMT  
		Size: 33.0 KB (33032 bytes)  
		MIME: application/vnd.in-toto+json
