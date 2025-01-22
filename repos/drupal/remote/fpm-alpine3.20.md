## `drupal:fpm-alpine3.20`

```console
$ docker pull drupal@sha256:71826e2cd486eb2c92350cc184254b858d48d158a81936a8e12fa75f8788e1f4
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

### `drupal:fpm-alpine3.20` - linux; amd64

```console
$ docker pull drupal@sha256:ab3ec752783bb36b3d12f00aa208c450fa59c78100d305d184663d229ede57e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.3 MB (55320145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0f9f37df8f4664ec3562330e3300a58d0fc82c3f4a9d7316b3710f33027058`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 07 Jan 2025 05:03:34 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
CMD ["/bin/sh"]
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 07 Jan 2025 05:03:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Jan 2025 05:03:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_VERSION=8.3.16
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 Jan 2025 05:03:34 GMT
WORKDIR /var/www/html
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Jan 2025 05:03:34 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 07 Jan 2025 05:03:34 GMT
CMD ["php-fpm"]
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV DRUPAL_VERSION=11.1.1
# Tue, 07 Jan 2025 05:03:34 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 05:03:34 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0bd12e2d550565a06a380ab1e09aa36d15395a876b85cf4bff5b27ec61c546`  
		Last Modified: Fri, 17 Jan 2025 01:33:07 GMT  
		Size: 3.3 MB (3308843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036abaf4d9082d2200b3323ba34436ffcf97c2ecf8a75e1bfccb92297f5b014a`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def4c2f5420656a313550a4564fed8b0c41f50c1eff90800b94218ba22413179`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85716534793b6bcafd45597c4bd7d71c0a9f1b3254d3f097e7280dea1284772`  
		Last Modified: Fri, 17 Jan 2025 01:33:08 GMT  
		Size: 12.6 MB (12565705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3189602c7f7127a2f1df5833c4615e9536d050f2a754004ec9f0a7f5617f16`  
		Last Modified: Fri, 17 Jan 2025 01:33:07 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924ee9f5975cc5f43632fa01042661c6d910d12b815a1b53ba8d1d772507b920`  
		Last Modified: Fri, 17 Jan 2025 01:33:08 GMT  
		Size: 13.1 MB (13109705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bdeba9891c56cd6d1b9cd184f8f9eaa3e7ffd215dec82cdfb5597addc46aba`  
		Last Modified: Fri, 17 Jan 2025 01:33:08 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f8993673358ae85b34f3830200d5fbbd446d00f2a730e8c49ff31abf249760`  
		Last Modified: Fri, 17 Jan 2025 01:33:08 GMT  
		Size: 19.7 KB (19712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c845ac25e3b443e17695c8aeb98873cfece8108bbc0eb6866e66ea110e27615`  
		Last Modified: Fri, 17 Jan 2025 01:33:09 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8a090ed9295f3902f0d8db6b2c13aa2683f39863ed6dc4ed952ccd4cf80ceb`  
		Last Modified: Wed, 22 Jan 2025 00:28:06 GMT  
		Size: 1.9 MB (1902432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd484f4b1c9be68911af65bd18f4aa8c53489c4d5c90595fe55d9468190d284`  
		Last Modified: Wed, 22 Jan 2025 00:28:06 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79224935b409bd2a8791afd6cf3a7f794800376c5dc8ab167d7c10cfb7869c9`  
		Last Modified: Wed, 22 Jan 2025 00:28:06 GMT  
		Size: 740.3 KB (740349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5d02f51108efd6a8224d482b21b2c975f412f7d5bd27522879841213381a5e`  
		Last Modified: Wed, 22 Jan 2025 00:28:05 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160b03630ed1ce9faf9c90e2451dc54f8ab9a41ff68791b22aa93f50150ccad9`  
		Last Modified: Wed, 22 Jan 2025 00:28:08 GMT  
		Size: 20.0 MB (20033415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:8018719a5b3ff18db965def91258dd192136a0a0c15a6bfad9f8042f609e1a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.0 KB (391009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0007598403d8d74badd1fc8b3297900c0a47f85d4ff7cf074f815c8a2854da`

```dockerfile
```

-	Layers:
	-	`sha256:f1119630242e833bc4d607629d0960685672b228d8bd928c009a22bba436bf2c`  
		Last Modified: Wed, 22 Jan 2025 00:28:05 GMT  
		Size: 357.3 KB (357335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19c3af8175f76f509dac3bb93c580d4e81db29e8dbabe00e019a001cfaaa8da3`  
		Last Modified: Wed, 22 Jan 2025 00:28:05 GMT  
		Size: 33.7 KB (33674 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.20` - linux; arm variant v6

```console
$ docker pull drupal@sha256:009dad96d4da405f2cf14c95966a6b8d0cbab300de0df1c3b89258916cbb1290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53360183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c5a4e6f5929b7bf97b8f43874a2a7a859c02543fc9bb71c12b2e2cf1d5736e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 07 Jan 2025 05:03:34 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
CMD ["/bin/sh"]
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 07 Jan 2025 05:03:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Jan 2025 05:03:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_VERSION=8.3.16
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 Jan 2025 05:03:34 GMT
WORKDIR /var/www/html
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Jan 2025 05:03:34 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 07 Jan 2025 05:03:34 GMT
CMD ["php-fpm"]
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV DRUPAL_VERSION=11.1.1
# Tue, 07 Jan 2025 05:03:34 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 05:03:34 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Wed, 08 Jan 2025 17:23:56 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db6ffe3ef654cff5545ca59dc5f06633dd6a45d737ad50c60dbdf1cfaa7c1cd`  
		Last Modified: Wed, 08 Jan 2025 19:01:55 GMT  
		Size: 3.3 MB (3291511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0b3742a8730e352c2d2f9b2b074af69eca367f405a0f860eb4588c6dc8e881`  
		Last Modified: Wed, 08 Jan 2025 19:01:55 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536a818f8e79c0c89eeb3c2062540dc8de02edfa1d91832c4872509e9271ef3c`  
		Last Modified: Wed, 08 Jan 2025 19:01:55 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52811a29757718da98bdf2a496761573a6af4bbd14516a419ff96e3860002e50`  
		Last Modified: Fri, 17 Jan 2025 01:50:41 GMT  
		Size: 12.6 MB (12565695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544f7aa935ba831f707b720bb2f72a76107a8827fb39e1034b823926e6ca5808`  
		Last Modified: Fri, 17 Jan 2025 01:50:41 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d91d3561b9b129ed67ad5914f4606536ac7a1d3d92b0d95a4ad645bf839d887`  
		Last Modified: Fri, 17 Jan 2025 01:54:18 GMT  
		Size: 11.9 MB (11938349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99f22bebddaadee36362536906d6743523bc8e7a6483befdbe868fa0c224448`  
		Last Modified: Fri, 17 Jan 2025 01:54:17 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8899b761e4614ec54a454067334fc68cdd20e180d8f417306d51dcba0917c6a7`  
		Last Modified: Fri, 17 Jan 2025 01:54:18 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65a9d9453c6492775d02f1bc21c30e44cb4fac27703e099b3d260deef575879`  
		Last Modified: Fri, 17 Jan 2025 01:54:18 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447766b86a1e5c5b840d52e594a06fe6f1f62b7546818a1bed4b254894da7651`  
		Last Modified: Fri, 17 Jan 2025 02:19:32 GMT  
		Size: 1.4 MB (1386024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9c8a05f71556227ec79be377799d9f12708bcccadead7198538eb203744c59`  
		Last Modified: Fri, 17 Jan 2025 02:19:32 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63eae7367b0dccfdeccad6392aaa9c5e1b6099afb38c470848e63780c6097b7`  
		Last Modified: Wed, 22 Jan 2025 00:28:25 GMT  
		Size: 740.4 KB (740354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f45a116e0633c5d47e5c246b79ba94ffc5b704944f20650088a60bab50f7b39`  
		Last Modified: Wed, 22 Jan 2025 00:28:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6cd257d090b407e6134dad110ececb7df47730ce60b575efddcde7d2b3f916`  
		Last Modified: Wed, 22 Jan 2025 00:28:26 GMT  
		Size: 20.0 MB (20033540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:ee0a99d5a9fe10aef3101efd05c80b5e69b09ead421676603d0492053d1f2e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.6 KB (33616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a018a975182fb7568bd09661d3c3bad685e1b910074bede78d6315dc662a5aa2`

```dockerfile
```

-	Layers:
	-	`sha256:6d36abf86e902769f3859b30af5294502cd6f7ada56fbc66ebd78e204fc04e5f`  
		Last Modified: Wed, 22 Jan 2025 00:28:23 GMT  
		Size: 33.6 KB (33616 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.20` - linux; arm variant v7

```console
$ docker pull drupal@sha256:aaec57c146bdd1f8ffe29267a584ace7634f3be2cad1e6f82e571fc513591cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (52031777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6771ec7f6207196a93fae8a602b2638ec20b3160a7ebe2b0589110ac445ca12`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 07 Jan 2025 05:03:34 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
CMD ["/bin/sh"]
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 07 Jan 2025 05:03:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Jan 2025 05:03:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_VERSION=8.3.16
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 Jan 2025 05:03:34 GMT
WORKDIR /var/www/html
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Jan 2025 05:03:34 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 07 Jan 2025 05:03:34 GMT
CMD ["php-fpm"]
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV DRUPAL_VERSION=11.1.1
# Tue, 07 Jan 2025 05:03:34 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 05:03:34 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Wed, 08 Jan 2025 17:34:15 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59598ed4d46933f984783e283ed636ac43c785dd3207a5432bcc816f12d3e64`  
		Last Modified: Wed, 08 Jan 2025 19:04:10 GMT  
		Size: 3.1 MB (3098287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395c20ee4940a4e59421ae1219a3af584a15664ef7e2cac6f928fe961a0dbe08`  
		Last Modified: Wed, 08 Jan 2025 19:04:10 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee856b900e721e0ee0e69e264eac4529da212f3087333fa1155fcba6c61c4c7e`  
		Last Modified: Wed, 08 Jan 2025 19:04:10 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a031d0756a83c37d840bf691644b85c9851b65199fde926709c45463477c578`  
		Last Modified: Fri, 17 Jan 2025 02:17:48 GMT  
		Size: 12.6 MB (12565698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2069148be6b188d452019575fb8bb1a3c340a2333b3485659802b8dee476d3a4`  
		Last Modified: Fri, 17 Jan 2025 02:17:47 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1571b43bb5fe0151b2857bccc4f5434e11e0076378bc518fcf8c2f2475dd5636`  
		Last Modified: Fri, 17 Jan 2025 02:21:12 GMT  
		Size: 11.2 MB (11189207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bfff30de19d9d7af8d6cb05f893f5ee19d56cca593581f2cdb93ed5d59b5f8`  
		Last Modified: Fri, 17 Jan 2025 02:21:11 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b124c799a2aa0840a1ec2c3953b6acfc818483825a7ad0f19b619add268eaa17`  
		Last Modified: Fri, 17 Jan 2025 02:21:12 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8811836664b18398100f743ca9bfb2cfbebfdd6a856d989b6b407893a9a728c2`  
		Last Modified: Fri, 17 Jan 2025 02:21:12 GMT  
		Size: 9.2 KB (9175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9879cdcfded06f01bb218eecc62225dd563b912195028f642be92e60e59872`  
		Last Modified: Fri, 17 Jan 2025 03:16:46 GMT  
		Size: 1.3 MB (1276021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d104d6f957f4fa5b1684e5e97e6bca04edb4071d60db9275b256d1d0b9d759d`  
		Last Modified: Fri, 17 Jan 2025 03:16:44 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85e51339a04f05d352b4f0169258f5a9fe27eecb344cc323f08520c9c422a37`  
		Last Modified: Wed, 22 Jan 2025 00:32:08 GMT  
		Size: 740.4 KB (740354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fd71ae185160c1fde9294a39a57de53fa530f589f482e98e1e5ae615a79eca`  
		Last Modified: Wed, 22 Jan 2025 00:32:08 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ed0437c99f0ee54b2548d85bb20abd51c69386f426eec3860254c3621eca5a`  
		Last Modified: Wed, 22 Jan 2025 00:32:09 GMT  
		Size: 20.0 MB (20033453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:5f32c425f1e71809f07333f597f2ac2b422b2522c86f8e9d722666f25416082b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.4 KB (388373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e149d670fb1cbb5b6561f0338337aa7d731d3a77aea38588e8b12c8300bd40`

```dockerfile
```

-	Layers:
	-	`sha256:09c57452e15d65087ae3884c6d571c4d3e56b3ca479ef4523dac4540c3ecd5ab`  
		Last Modified: Wed, 22 Jan 2025 00:32:06 GMT  
		Size: 354.5 KB (354542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edfac6dd4e20f170e53833539f9381bf57f10182d4d2b428661f36831e1f34d8`  
		Last Modified: Wed, 22 Jan 2025 00:32:06 GMT  
		Size: 33.8 KB (33831 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:23fc00d9cce53c58da4c882d28a2afa290d1da1bd27073ee83e0e291d544ad76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56173445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56055ba52c63133d93e86d2411b3e44063994a3452019e1f4a0bc7e4fc7308fa`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 07 Jan 2025 05:03:34 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
CMD ["/bin/sh"]
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 07 Jan 2025 05:03:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Jan 2025 05:03:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_VERSION=8.3.16
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 Jan 2025 05:03:34 GMT
WORKDIR /var/www/html
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Jan 2025 05:03:34 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 07 Jan 2025 05:03:34 GMT
CMD ["php-fpm"]
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV DRUPAL_VERSION=11.1.1
# Tue, 07 Jan 2025 05:03:34 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 05:03:34 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbfea75779fb9f51b30df44aa75d799257f21786a16d817ec263eb6cb4d24df`  
		Last Modified: Wed, 08 Jan 2025 18:59:13 GMT  
		Size: 3.4 MB (3360616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47781173f5085c5bf81fea23c55143896e3f61e88db6ca44fe803f5cff0e87b7`  
		Last Modified: Wed, 08 Jan 2025 18:59:13 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c52892499eb092197769cb95ccbc932a1373115445d0425ff828aa7d428bb5`  
		Last Modified: Wed, 08 Jan 2025 18:59:13 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd329eb147d2c6ae2390acb0cc5aec46916d713f577ffdfdfe9da6eb1a5debd`  
		Last Modified: Fri, 17 Jan 2025 02:14:13 GMT  
		Size: 12.6 MB (12565703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8ca4cda8f6a85b1db076d6a0d363bf3f87382291f8ef1461c95face5f1a5a0`  
		Last Modified: Fri, 17 Jan 2025 02:14:13 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342b7b7bb4ec7adbf471326e5ac36e7dd65d41826c72d1c041794e3a213452dd`  
		Last Modified: Fri, 17 Jan 2025 02:19:02 GMT  
		Size: 13.2 MB (13169389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378dbed123f165f3ea0f94b11a4f51ea38385657716f7f1c93bf6b95d269f7d1`  
		Last Modified: Fri, 17 Jan 2025 02:19:01 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b789d45f8acaa03233d66f07ada4726d63afba9c8202476dd47c4c5cb9451377`  
		Last Modified: Fri, 17 Jan 2025 02:19:02 GMT  
		Size: 19.5 KB (19487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdae7330201c7b293292a6ec8733f0c8e2082d9190b27e3a75e7003ebbf62da`  
		Last Modified: Fri, 17 Jan 2025 02:19:02 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af59a623f7552ba8f46b621b2f7db0c4e82a258e42a2ed01c287448ad4808343`  
		Last Modified: Fri, 17 Jan 2025 03:29:56 GMT  
		Size: 2.2 MB (2179921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0cef8bc0030bf3d00a10c18d85eca5c81fb691da25e76c31bec6a98004bf91`  
		Last Modified: Fri, 17 Jan 2025 03:29:56 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fceb84cd7a17a2518676499973cd5ed0e5d0b56a526be49feb33d3574364e65c`  
		Last Modified: Wed, 22 Jan 2025 00:31:02 GMT  
		Size: 740.4 KB (740351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2232560759eb3cf7647e51433ce2579e3bda0237a5d179ffaca45382a63aabf`  
		Last Modified: Wed, 22 Jan 2025 00:31:02 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5c840572a9a609666670eb0b3587db57d6048616fe5c6241b8e2a6ea9c98ec`  
		Last Modified: Wed, 22 Jan 2025 00:31:02 GMT  
		Size: 20.0 MB (20033474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:bcb6dbcec43c8a91f205ab9607e5918b3291bcaa8a9e8ca2005abd5f269b2e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.5 KB (388461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dddd00b786265a22a4e5e026675178e3c2996e5aebaecdc9178f00699bbbfc1a`

```dockerfile
```

-	Layers:
	-	`sha256:21744766eb443688513ce22a1efc5950b7c953433004306242956898f95b0829`  
		Last Modified: Wed, 22 Jan 2025 00:31:00 GMT  
		Size: 354.6 KB (354578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d941d80934662c6dc9b13be7c18d1dbccbef46ccbef5a5f35ea623b66adfc74`  
		Last Modified: Wed, 22 Jan 2025 00:31:00 GMT  
		Size: 33.9 KB (33883 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.20` - linux; 386

```console
$ docker pull drupal@sha256:99082a267f3c9d4233f6049b7155bfe61ef0bfae40e8ac76c92147da0196037b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55609021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3cb9ec73071885dca0ef3e66e15c4e03c167c5e54e7cdb0594f3dec389db94`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 07 Jan 2025 05:03:34 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
CMD ["/bin/sh"]
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 07 Jan 2025 05:03:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Jan 2025 05:03:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_VERSION=8.3.16
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 Jan 2025 05:03:34 GMT
WORKDIR /var/www/html
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Jan 2025 05:03:34 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 07 Jan 2025 05:03:34 GMT
CMD ["php-fpm"]
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV DRUPAL_VERSION=11.1.1
# Tue, 07 Jan 2025 05:03:34 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 05:03:34 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f7064fa89a18519bf91477498e200680f6de23afc909dec023bec1b31c0fc1`  
		Last Modified: Fri, 17 Jan 2025 01:33:09 GMT  
		Size: 3.4 MB (3359980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177406ff305f7d837df996477a848025d50b16a1c606ae965995e021954d5a0d`  
		Last Modified: Fri, 17 Jan 2025 01:33:09 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00c02ebe93fdff428781a32441995e9ae26c3e8f7dd007963d4cb3613c83dae`  
		Last Modified: Fri, 17 Jan 2025 01:32:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0416d003a4b1717abb5b41bb0bf08d1aaf28a2a6d2dfe4b49cddf66ce219f9f4`  
		Last Modified: Fri, 17 Jan 2025 01:33:10 GMT  
		Size: 12.6 MB (12565695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac45802f824e4108ee8815231dd479bcae43055ac16fd5dd32a14d0da79f1118`  
		Last Modified: Fri, 17 Jan 2025 01:33:10 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65222880906111f0f1c90aa3abc667c0755362f4069da4bf2d0525f201b07882`  
		Last Modified: Fri, 17 Jan 2025 01:33:10 GMT  
		Size: 13.4 MB (13441784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff1444d8cb84263ae9c53dce06fd1fe9c17066f24303289cc5065b3bf69eeb0`  
		Last Modified: Fri, 17 Jan 2025 01:33:10 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3b22d85b247f64fec6c99d235e0bead037048de74a3e76afa1e2884aba59b7`  
		Last Modified: Fri, 17 Jan 2025 01:33:11 GMT  
		Size: 19.7 KB (19720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b9f0dac6f7326fcc645559b331092fed97d3e4bbc7dfa4f4d4465ae62cb857`  
		Last Modified: Fri, 17 Jan 2025 01:33:11 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b63b90aff4f544a0c748df33409370eabf0d5858312d0c86a952ef68e1bb81b`  
		Last Modified: Wed, 22 Jan 2025 00:28:10 GMT  
		Size: 2.0 MB (1963427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaef084efb2d83f696ef5cabda69f2461d1803b64647d4a82b6d3060721fe204`  
		Last Modified: Wed, 22 Jan 2025 00:28:09 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543b09b8b13f311ac374b4858ae78f1f55a55b6ee84bc1d2c3574d05c6029631`  
		Last Modified: Wed, 22 Jan 2025 00:28:10 GMT  
		Size: 740.3 KB (740349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd1c5513776357f60b554e7791ba59069bbacbef1bfd01d13af9427f9ae837a`  
		Last Modified: Wed, 22 Jan 2025 00:28:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d515648308c8796789238514074a74e34e2893284e2be313a75b10bcd803a1`  
		Last Modified: Wed, 22 Jan 2025 00:28:11 GMT  
		Size: 20.0 MB (20033370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:d469318ad73602cdd5b38539d504c75532e7ce6c3be1d89332520c97c6232c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.9 KB (390902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a53c07467b7408fd5122b825679669c254dfcb965f0a69f2331c1d294fca731`

```dockerfile
```

-	Layers:
	-	`sha256:61b095aa09fcceee2bb1a4f999a4d1b6b542ea534cebddfefead924ea84d9b35`  
		Last Modified: Wed, 22 Jan 2025 00:28:09 GMT  
		Size: 357.3 KB (357290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4630131e3acd9fb8eb30e74127ba0fae3d7a8fbac69a78780637a207eb462c59`  
		Last Modified: Wed, 22 Jan 2025 00:28:08 GMT  
		Size: 33.6 KB (33612 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.20` - linux; ppc64le

```console
$ docker pull drupal@sha256:ee46f1e6a5fc20a6b73a88a978cd18d5b14f81139942300447a9cdb6cfaea2c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55674154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a846551c544add6f115dd68fb0d8f7d9515b0d031bfb537458f1bdacf95b835`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 07 Jan 2025 05:03:34 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
CMD ["/bin/sh"]
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 07 Jan 2025 05:03:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Jan 2025 05:03:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_VERSION=8.3.16
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 Jan 2025 05:03:34 GMT
WORKDIR /var/www/html
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Jan 2025 05:03:34 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 07 Jan 2025 05:03:34 GMT
CMD ["php-fpm"]
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV DRUPAL_VERSION=11.1.1
# Tue, 07 Jan 2025 05:03:34 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 05:03:34 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac389e1bad8c901cdd7df01f96be5f8508854f3411c6da9e6e8ef6668f4b16c`  
		Last Modified: Wed, 08 Jan 2025 18:46:53 GMT  
		Size: 3.4 MB (3435551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b7f9d7dcac76616498febca2aa6101a5ff06711026417e0332b7700a8e89f8`  
		Last Modified: Wed, 08 Jan 2025 18:46:52 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bef84277af6646e9da0330c1f81457cb9ace93a33c43f40275eb914946791c`  
		Last Modified: Wed, 08 Jan 2025 18:46:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7071b031605efab7212139d1110709838fa850367092f8ef91e00e5ef4e725`  
		Last Modified: Fri, 17 Jan 2025 01:50:27 GMT  
		Size: 12.6 MB (12565713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d909e9fff43185a21843c11f244a73f1ee288501278159590ea9e95a2444de`  
		Last Modified: Fri, 17 Jan 2025 01:50:26 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b5a1a8ea82b0686c57feff8ba1efe99d5a1313eecf05ba68b62a157e7047e5`  
		Last Modified: Fri, 17 Jan 2025 01:53:32 GMT  
		Size: 13.6 MB (13610536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d815146a8fb85300df17ecac244e27c884dd0d0c2eda4bc535a9ffd2b9387ad9`  
		Last Modified: Fri, 17 Jan 2025 01:53:31 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da23371d764ae70dadfc66c2bb4ece2482f99429d8ab833f1d4011a640065f8`  
		Last Modified: Fri, 17 Jan 2025 01:53:31 GMT  
		Size: 19.5 KB (19487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd0ac6d6cd7e19616a045dddb916736e1c4bd221734a4f307ae24770d23df49`  
		Last Modified: Fri, 17 Jan 2025 01:53:32 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbb4ce1c3fb598253a64722778a58850d3f97659b098fef825a78ed847fd36f`  
		Last Modified: Fri, 17 Jan 2025 02:32:44 GMT  
		Size: 1.7 MB (1680731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d475eb065a38ffdb167a86dde96d27d3b8465500a7643e38788ac98e9f7a5ed9`  
		Last Modified: Fri, 17 Jan 2025 02:32:43 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ad5d5f8963e1d3e013f479711efc7b2d9779763b5c4dcd6576d9b7a232dd7c`  
		Last Modified: Wed, 22 Jan 2025 00:30:31 GMT  
		Size: 740.4 KB (740351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9546302765d20014f738fe07b4611efdcb332524d6006653fc5c341cf21ad8`  
		Last Modified: Wed, 22 Jan 2025 00:30:30 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa7007e383726d58c59273a0640248087f982575fb1728adaa8daa507a3be45`  
		Last Modified: Wed, 22 Jan 2025 00:30:32 GMT  
		Size: 20.0 MB (20033633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:55c15fe849f858c91f30d8a3f0f1cfec3a781b04d0d0d25d6b3ed6c26c15550d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.3 KB (386338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfcffc9740d2b2b8805ae7e23090f295b054720ee84abee9e2a640e9174b2c7b`

```dockerfile
```

-	Layers:
	-	`sha256:8d21c077f2343546b4eff7bb5da8a839c038fd645ef0b0d8d4d27ab77a72549f`  
		Last Modified: Wed, 22 Jan 2025 00:30:30 GMT  
		Size: 352.6 KB (352581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f82b2e47d97b1dce6cad6f0f1df0656a28f0472ffe1587714f928993268beda0`  
		Last Modified: Wed, 22 Jan 2025 00:30:29 GMT  
		Size: 33.8 KB (33757 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.20` - linux; riscv64

```console
$ docker pull drupal@sha256:a4617763682d3a6a36af62b21af4e4801ef03857489cf62bb57dc95ad16a1711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54331192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8dcdbd05c26f36700a3c823d58e1ef60868c5301ffae1c57396369739014bd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 07 Jan 2025 05:03:34 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
CMD ["/bin/sh"]
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 07 Jan 2025 05:03:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Jan 2025 05:03:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_VERSION=8.3.16
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 Jan 2025 05:03:34 GMT
WORKDIR /var/www/html
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Jan 2025 05:03:34 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 07 Jan 2025 05:03:34 GMT
CMD ["php-fpm"]
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV DRUPAL_VERSION=11.1.1
# Tue, 07 Jan 2025 05:03:34 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 05:03:34 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Wed, 08 Jan 2025 17:49:41 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ec415e9e84f4fbfdf631ed4f49ea5fc3b66ea4fc7dde02b872f6bf80473254`  
		Last Modified: Thu, 09 Jan 2025 02:22:49 GMT  
		Size: 3.4 MB (3428298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7afa983c26aef0c7fdf0b220c994bbc1954adaf863d01d1a09ad7b531a485c`  
		Last Modified: Thu, 09 Jan 2025 02:22:48 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d306623b924639b3cc48ee24fd37021ee4b75400a0afd7d21003ec0fced66d79`  
		Last Modified: Thu, 09 Jan 2025 02:22:48 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c72e05aeaece2f9593e9ea8e88095c7de654bfdb144e7f921c7c3f8ba5e441f`  
		Last Modified: Fri, 17 Jan 2025 05:08:50 GMT  
		Size: 12.6 MB (12565705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ff74cc236318854e9d412a0075895d62aef3200169c91390cf0ea5d85367ff`  
		Last Modified: Fri, 17 Jan 2025 05:08:48 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6915b828db22d22a03fc8b558c4b07781c28228e4d34d9e2d780df8b2f4a2aea`  
		Last Modified: Fri, 17 Jan 2025 06:00:15 GMT  
		Size: 12.7 MB (12674659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a092d6f542b7073a583fec771c62288ba4a29bab3e092477eba10af403672a`  
		Last Modified: Fri, 17 Jan 2025 06:00:13 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134c9326105f9646fcbb9d5caa6613f42904fb33281f469442969e016f678ee4`  
		Last Modified: Fri, 17 Jan 2025 06:00:14 GMT  
		Size: 19.5 KB (19505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0950e2bc41ba4c2f78942a3514583458beee0699206a2bd30f538f6c13fb543d`  
		Last Modified: Fri, 17 Jan 2025 06:00:14 GMT  
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
	-	`sha256:6d10789240032738e576815f7989208b869ebffff994058fd7486a55472ad090`  
		Last Modified: Wed, 22 Jan 2025 00:33:23 GMT  
		Size: 20.0 MB (20033688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:42ae70ba125cdf99afc97c09829e43748da172bafa91f8477e6e2106497a6cf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.3 KB (386334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2c82d052ddd3dbab0e605132f7b1b1a44724b277623b8d58b2d65144734bd4`

```dockerfile
```

-	Layers:
	-	`sha256:8be43e11b721f853393c6023ddbe3999079a966267a29ec85157601235561af0`  
		Last Modified: Wed, 22 Jan 2025 00:33:19 GMT  
		Size: 352.6 KB (352577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:333158682d6125512c4ef98a2ca9c666184779646d2c4ec743faa437fa4230ba`  
		Last Modified: Wed, 22 Jan 2025 00:33:19 GMT  
		Size: 33.8 KB (33757 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.20` - linux; s390x

```console
$ docker pull drupal@sha256:4b5254f0c7520a7c7fb3f2ed0ff7e1d1274f17a84da89b68024ec0e39fb99d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55006658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e536002007b51b69f3bd2bb6304bd17916c8e4f6ee6bc126161b4b03969175bd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 07 Jan 2025 05:03:34 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
CMD ["/bin/sh"]
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 07 Jan 2025 05:03:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Jan 2025 05:03:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_VERSION=8.3.16
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 Jan 2025 05:03:34 GMT
WORKDIR /var/www/html
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Jan 2025 05:03:34 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 07 Jan 2025 05:03:34 GMT
CMD ["php-fpm"]
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV DRUPAL_VERSION=11.1.1
# Tue, 07 Jan 2025 05:03:34 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 05:03:34 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Wed, 08 Jan 2025 17:25:57 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f228edf04a39559d957ef5581b08c9a7d393dc64a098575e63c061140ae78557`  
		Last Modified: Wed, 08 Jan 2025 18:50:04 GMT  
		Size: 3.5 MB (3501854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3a938ef64c5dda4d67df22456ef7b998d8d733e6b109f8565eae8077a42767`  
		Last Modified: Wed, 08 Jan 2025 18:50:04 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8665be221001567b6093cf5d6fd1080ca3c33832bf4656568c06b3f7959c83`  
		Last Modified: Wed, 08 Jan 2025 18:50:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d360f2c571fe68967d2a3dbfac8206dbd420826318956200f9ef355d1cc31fb0`  
		Last Modified: Fri, 17 Jan 2025 01:59:29 GMT  
		Size: 12.6 MB (12565691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d530de939b52d180fd39cc1973ee04a30523a74e2e168cdec5eb0563d15208`  
		Last Modified: Fri, 17 Jan 2025 01:59:29 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7470d8ea16a3d84bc182531c21efc7bc1b5cd8e6881a3aff31a1208513da7e`  
		Last Modified: Fri, 17 Jan 2025 02:03:20 GMT  
		Size: 13.1 MB (13071761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2884ce42bb39a139e69d580f615c12ac0e5e4603ead9501f8fb2b532806dd150`  
		Last Modified: Fri, 17 Jan 2025 02:03:19 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469a936cf9a2cdfc71e0a1ccc9d0a857528a0c054444586d4b750eae9bf86141`  
		Last Modified: Fri, 17 Jan 2025 02:03:19 GMT  
		Size: 19.5 KB (19498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607d341afa3f4a08bf48af4347faae7bce3fcfe70d6d20b7b7c93108cd4d54f1`  
		Last Modified: Fri, 17 Jan 2025 02:03:19 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194f36d9b3ba61d76a4f7b2d12639124fd916964c31356de71f10feb36125361`  
		Last Modified: Fri, 17 Jan 2025 02:39:34 GMT  
		Size: 1.6 MB (1597353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ce5cc1229a0d83e1024afe0801fe1b85a0aa76c30a37f562b091f598784f63`  
		Last Modified: Fri, 17 Jan 2025 02:39:34 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d1d417a184ae26f9dd3bd8bdfdd1b1fa3c29c012f5e4307d9cdf03b251d96d`  
		Last Modified: Wed, 22 Jan 2025 00:30:14 GMT  
		Size: 740.4 KB (740352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcb8a84bf02d80549cbc604a67e6ae3575c37b8ab35dd17a73b88a5f4d7df7f`  
		Last Modified: Wed, 22 Jan 2025 00:30:14 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4a38db897f6fb0cac6c2977f8bf26e8627be6d4ad0a1efaaba2da986b147f8`  
		Last Modified: Wed, 22 Jan 2025 00:30:15 GMT  
		Size: 20.0 MB (20033084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:3141face3b34d0d7af72c560d3682014b0906e76358fba8a38ec091743475f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.2 KB (386197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f4a99ccc80ff34180065bb9f68fdbb1225c5a47bc3b5c075b938e5c4715da21`

```dockerfile
```

-	Layers:
	-	`sha256:f4f4944709ca8928d77695c17f2dac29d22aba36d6263e6c15efd4ecfcba8daa`  
		Last Modified: Wed, 22 Jan 2025 00:30:13 GMT  
		Size: 352.5 KB (352523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9e11c90e907ff5c7cd29319cfd45eb8328d8cd28459097c3ad3115b8001f3e5`  
		Last Modified: Wed, 22 Jan 2025 00:30:13 GMT  
		Size: 33.7 KB (33674 bytes)  
		MIME: application/vnd.in-toto+json
