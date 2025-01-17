## `drupal:fpm-alpine`

```console
$ docker pull drupal@sha256:7435b29db8adaf3b78c00c36a72b04a75247f01dee2d69e293ecd310587a72f3
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

### `drupal:fpm-alpine` - linux; amd64

```console
$ docker pull drupal@sha256:4e09ebb20f8a46fb45ff123aa508de2e090cf79d1f39f3cc5226c722321e984e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55475735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6e8a74020ec5516300fc2b248f53bf6b0e492732134ac499dca79f5d90ad21`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 07 Jan 2025 05:03:34 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae49de6b59a3ada68038915c6ced5c3fe9a4d9734c795f5a290799df9bd4beaf`  
		Last Modified: Fri, 17 Jan 2025 01:33:31 GMT  
		Size: 3.3 MB (3333625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cba018865568c1d0e52317c42c2372693e63212bbfa9fdef74f0c36c092346`  
		Last Modified: Fri, 17 Jan 2025 01:33:31 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8c926c51f944e1f73fd121e3ad6f36a2e3123fc91798822958f3a06b35df2d`  
		Last Modified: Fri, 17 Jan 2025 01:33:31 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a294ad2fc4eb0744141cbe376c87751574ed0855e5b42d9e2387d5eac2b3bfd8`  
		Last Modified: Fri, 17 Jan 2025 01:33:32 GMT  
		Size: 12.6 MB (12565913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40cc7f0f5d0d50ab5cd390cd67c5019f95bc45bbd11f47693935c52fffcc25b4`  
		Last Modified: Fri, 17 Jan 2025 01:33:31 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf65272aeb380d63ca16f6621ea3bc1d8d9030fef6e0ff42c422894fc45c1ab5`  
		Last Modified: Fri, 17 Jan 2025 01:33:32 GMT  
		Size: 13.2 MB (13203109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571b396ed0cd01828f98f7e5a13d4df7250f2e4797a89f0f390ce47365a55a9c`  
		Last Modified: Fri, 17 Jan 2025 01:33:32 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef85654c4194b6058eda05850776a84949d19908ae00916f1633a7d6d173ebc`  
		Last Modified: Fri, 17 Jan 2025 01:33:32 GMT  
		Size: 20.0 KB (20028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e071def809824dc2b374a01f9cb3df2da7b62130b74b519243dba0d7d7b6539`  
		Last Modified: Fri, 17 Jan 2025 01:33:33 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6ae66e3937b4e914036476146047c5d5e830530cad0c1e70d6ae9f9bb1c17f`  
		Last Modified: Fri, 17 Jan 2025 19:10:05 GMT  
		Size: 1.9 MB (1922107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677971f607a4df1cd5f0df3c1671069e116c9f1df5b96e95b5bafcd527c84a68`  
		Last Modified: Fri, 17 Jan 2025 19:10:05 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2e154385cfdff6a052f3ee56cdff5f89e9cbd9e7a1383f73548a3471f8a99a`  
		Last Modified: Fri, 17 Jan 2025 19:10:05 GMT  
		Size: 742.2 KB (742234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5e1987670898231338222b64f2469087bda25e5f294efde9d1f90ff1b0256f`  
		Last Modified: Fri, 17 Jan 2025 19:10:05 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cc8a8d4f4fca416d318b7e2e332fbe7bc9329a88bf5fe22982d8e3d85c7238`  
		Last Modified: Fri, 17 Jan 2025 19:10:07 GMT  
		Size: 20.0 MB (20033281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:5a715ac554f1e665628344fd993eee1996eeff5ad6c48082d1ed7a53c646b6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.1 KB (401053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293152ad0d3de859c4190173434e40348e4766b2bf6ac0357d458d952ec2a06b`

```dockerfile
```

-	Layers:
	-	`sha256:4b084fce154ee608e8125c330b51f720108aa99ea68f3229be963e4dcf8c4aac`  
		Last Modified: Fri, 17 Jan 2025 19:10:04 GMT  
		Size: 364.8 KB (364815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a42a7fe00af7bc92f8ecda7f39fb5846ef3cde0fdc163ec3eb73de287b7921d4`  
		Last Modified: Fri, 17 Jan 2025 19:10:04 GMT  
		Size: 36.2 KB (36238 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine` - linux; arm variant v6

```console
$ docker pull drupal@sha256:f5181dbb9aad7480af061aed06844819cf26ed700826026fea2a049f62dc88e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53371509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f1abf2fbf0518603a1f9bd5ec029dff7a8e67a9f3d264ed8e378a63ae9dd4a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 07 Jan 2025 05:03:34 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27df19b1748e0c5336a2934dab90837cecaea9ecf548f60ec89ced0bb3caa23`  
		Last Modified: Wed, 08 Jan 2025 18:49:59 GMT  
		Size: 3.3 MB (3300488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8c9d60966ee150dd112939c109e4bdb3925301588315d098c22b807f8a62c`  
		Last Modified: Wed, 08 Jan 2025 18:49:58 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af0368056bd9d6658ab6d584d82811582bf7d94d14851784fefbce2ac6bd01`  
		Last Modified: Wed, 08 Jan 2025 18:49:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068b09f0e8dc78e913aaad70d25f734a600d78100c16366fca66a9bebbfe531e`  
		Last Modified: Fri, 17 Jan 2025 01:33:46 GMT  
		Size: 12.6 MB (12565930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2094e59041bb8925e36b0bf995cb79b19941687dede68b21c05e92360173b59`  
		Last Modified: Fri, 17 Jan 2025 01:33:46 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d010aa65b2cf9285c0a86d1caa6a16d913c49c1813858d78b0bd8ccae8437ab7`  
		Last Modified: Fri, 17 Jan 2025 01:39:18 GMT  
		Size: 11.9 MB (11937661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e637602c4e03b081c973998cfe353a12e8c8619843b987558eb9306ebbb1a3`  
		Last Modified: Fri, 17 Jan 2025 01:39:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f971bdca2e24bdbc12572ed7d0d9903e3dee6ffbc43eb5fcde682e21aa8a5e3`  
		Last Modified: Fri, 17 Jan 2025 01:39:17 GMT  
		Size: 19.8 KB (19845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8419b0ac28228fb2d23f9f6c41f2e86f0f12dc80da105999b81667e954196c7a`  
		Last Modified: Fri, 17 Jan 2025 01:39:17 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85506de1354fac92724a2bd2827595a89a84be0d68d3babedaab48974654082d`  
		Last Modified: Fri, 17 Jan 2025 02:18:10 GMT  
		Size: 1.4 MB (1394429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f92c496eb0c4626c86ebac0c43b6bc3d12345384c5f31fc4632c540c742cb4`  
		Last Modified: Fri, 17 Jan 2025 02:18:09 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85105ff232ee5ecaa9de4b78c6e74b33a4e67afeaa88cace1699c8ddad0eb97`  
		Last Modified: Fri, 17 Jan 2025 02:18:10 GMT  
		Size: 742.2 KB (742241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ab4b4152e034dcd99e767f6c2c63a3eefb4d9d85d2718053bdae7467f30189`  
		Last Modified: Fri, 17 Jan 2025 02:18:10 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816b7ca06832cf56e91644950237ac322b4a13e630bf93633a5c493d5dc80df8`  
		Last Modified: Fri, 17 Jan 2025 02:18:11 GMT  
		Size: 20.0 MB (20033305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:74797d159afaea3b282c71a509e62ec46cec47069e5dbee70c5dfdef099c57f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 KB (36243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e19cd1dd4177d40e3fe2670e63ecc36e129f4f0de559e9c989ad222d4d180eb`

```dockerfile
```

-	Layers:
	-	`sha256:e07c0476c3c1aa1c48f934f9a8a2027f769932bdaf00d0ed9d1e7f4e14c50770`  
		Last Modified: Fri, 17 Jan 2025 19:07:46 GMT  
		Size: 36.2 KB (36243 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine` - linux; arm variant v7

```console
$ docker pull drupal@sha256:f2e6afd4a51a3fedb83f705dc8b0544ea5c214d06ba6605a244ac080103f3188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52126499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37e213eb3ad19dfcd50399ffc8f4a76a973d9f606d3db9b456a0ddceb971840`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 07 Jan 2025 05:03:34 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ceb78f083649061e4b802531e1ff0a876077474242c75cfdca63feceddf42`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 3.1 MB (3115360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874d1ba95c5456f76e6eaf3fcad122706769776c7031c7f79e4104de9979281`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b35dc6dca52f50940237e3dd268e0dbbd22216c7d386d5989137c1f820852`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0204e80c0296cdae0cbaa8fe8c132f49b9c6f8c1700e5c9d1b71849266b1c96`  
		Last Modified: Fri, 17 Jan 2025 02:07:11 GMT  
		Size: 12.6 MB (12565935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b976bccfd388504dcb1ae8991cef4eb2890a7d4f843ed9d26528f97837f9da`  
		Last Modified: Fri, 17 Jan 2025 02:07:10 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06915eca9877d9be2e06530e8c442b3a0bea045c98d533126fc6ff2bceee37d4`  
		Last Modified: Fri, 17 Jan 2025 02:10:19 GMT  
		Size: 11.2 MB (11249099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c86c92b496bccd4526be3879519d53e5daa8819acd1e44b18e710d8ac090ca`  
		Last Modified: Fri, 17 Jan 2025 02:10:18 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb1ced4a77966f8850c5fb7d6bfc943c4888012a4921f49b3a3dacc4bc627f7`  
		Last Modified: Fri, 17 Jan 2025 02:10:18 GMT  
		Size: 19.8 KB (19846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3ec4d14ce3d25d025ee7927a6c0d15093dfff4d08c3c458131c6cd56b57bfb`  
		Last Modified: Fri, 17 Jan 2025 02:10:19 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f92d1dc33370a56cab285810f7e36bdd51ed6af6d699c44b04e6a07d2743d57`  
		Last Modified: Fri, 17 Jan 2025 03:15:25 GMT  
		Size: 1.3 MB (1289996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1e49bf25874ffa7c1d3cfcf8bd96cc3967993de15e1c2dd5a0513756119b0e`  
		Last Modified: Fri, 17 Jan 2025 03:15:25 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c506748a54085b0b3d3d12adec165cd0bd66d9bf705f21425c4f025de71134`  
		Last Modified: Fri, 17 Jan 2025 03:15:26 GMT  
		Size: 742.2 KB (742243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca150ed85201faa6272b492d3a11dc8e7322ba52d166718efbc33d51afa094f9`  
		Last Modified: Fri, 17 Jan 2025 03:15:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bf98601110d73887fec0511d31d6488e645fee73f045ad6b367b3c8c17c23d`  
		Last Modified: Fri, 17 Jan 2025 03:15:27 GMT  
		Size: 20.0 MB (20033171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:ba2a071e9113a3f903419e680a30dfeb2a4e18f9daa1edd55d2a8ede22308456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.6 KB (398592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814336e47611b0443ddc8955d94113c64528e50c98820dbc5243c4e2d785eb53`

```dockerfile
```

-	Layers:
	-	`sha256:c1d17a09aa80a726a104d0ef5bf9eb1db968fcbb698b02543b01d091046d2119`  
		Last Modified: Fri, 17 Jan 2025 19:21:05 GMT  
		Size: 362.1 KB (362134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:965b25a2e8636e9da1021803d56ba9c663c445c68938edf8cc548704fc33b328`  
		Last Modified: Fri, 17 Jan 2025 19:21:05 GMT  
		Size: 36.5 KB (36458 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:58f30fa081b58d9856cc380cde672d8a171099b17615c6067d693ed6c1567dfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56078817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048206e85026fea7a4b4fadb00ef6dce9a09140fc0a33d14bb7b86d938d72b5f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 07 Jan 2025 05:03:34 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a259b492a8c3558416dd48f8aad1dda78fda9cef38298295c5e43623b56a18c`  
		Last Modified: Wed, 08 Jan 2025 18:47:48 GMT  
		Size: 3.3 MB (3327674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c6a796a4d698d720516d98efaded2b858014b8a81418484745626b542df1b`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce86ef064edc436017f8d7adf39a34791690aa9358ada4968c2846dc852ca8a5`  
		Last Modified: Fri, 17 Jan 2025 01:59:01 GMT  
		Size: 12.6 MB (12565957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82573dd219577096ad073ab5cc5aec03711465792e841e32a69de3f869ad15db`  
		Last Modified: Fri, 17 Jan 2025 01:59:00 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbbae26bb0f5db0f77bfe9fcba38e8bcc044c378146650d12820205ac9a1e6f`  
		Last Modified: Fri, 17 Jan 2025 02:04:09 GMT  
		Size: 13.2 MB (13193421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c60f0abd9ea38dd6ecb2f0cb65f214d431a2b1baf0daa5356300de042fbf19e`  
		Last Modified: Fri, 17 Jan 2025 02:04:08 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab9b6841504d1eebe9d868b28fbea6b9f043a83188fb388330853ee17ac2a32`  
		Last Modified: Fri, 17 Jan 2025 02:04:09 GMT  
		Size: 19.8 KB (19848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4b77cf854b474df3e3d58c03e8b3ccc81841d1ab6e9539f4d028a1eb69438a`  
		Last Modified: Fri, 17 Jan 2025 02:04:09 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd1712ba4279944c556d38985ddc3948d7ea0b80a75d42c28c2b5918a96d9a3`  
		Last Modified: Fri, 17 Jan 2025 02:49:24 GMT  
		Size: 2.2 MB (2190371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d22bc1f63ba129e98fcc178bd6ab3b759c19f1ac39399a747bd496212266ee8`  
		Last Modified: Fri, 17 Jan 2025 02:49:24 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf76070a6d9a177be5e9a26b0233d0247e6a8cc3bcd83d68194ed746cc1cd38`  
		Last Modified: Fri, 17 Jan 2025 02:49:24 GMT  
		Size: 742.2 KB (742239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb019395d132728243a50f4ea6ae63880148bc04523a6fe4fff7f1920fc32d0`  
		Last Modified: Fri, 17 Jan 2025 02:49:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a467627b6e009a146a90425a2175f7f5aaa27855bf7ce54977124520827d37`  
		Last Modified: Fri, 17 Jan 2025 02:49:25 GMT  
		Size: 20.0 MB (20033214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:dd71a75515f176b2df46777cd1d143e735a621fb37f34dbe141bf0ad1a578629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.7 KB (398744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecabdd4ad36bfc732a986ea0a4832c7fc8b09693c41e761405949bb0815b1b6`

```dockerfile
```

-	Layers:
	-	`sha256:7e5a91b9ede890f263104432108fa62b114d9539f03950e805a7a11c3c1519ce`  
		Last Modified: Fri, 17 Jan 2025 19:11:16 GMT  
		Size: 362.2 KB (362202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f8124962fcdbd6391a7c7ae3fb7524ed047eeda066d12ba6098f2761775897d`  
		Last Modified: Fri, 17 Jan 2025 19:11:16 GMT  
		Size: 36.5 KB (36542 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine` - linux; 386

```console
$ docker pull drupal@sha256:e69a6a0f4d8dbb9d5a7f2d504bcab1b988c15e956385bb2d70c882f6a2c90c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55705554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7cc40d6e08c3a65a6023625d358eefe94f86f3609069d93c5a57c9157f3d6b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 07 Jan 2025 05:03:34 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
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
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7386cf222b0d875e8873ae391fb2d15011557c0a8620c08a86ab8eb339acf635`  
		Last Modified: Fri, 17 Jan 2025 01:33:35 GMT  
		Size: 3.4 MB (3373803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8525db88a29b4c886a172b95463f3cbeb75981b131056a27ec1d34b472f723`  
		Last Modified: Fri, 17 Jan 2025 01:33:35 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8c926c51f944e1f73fd121e3ad6f36a2e3123fc91798822958f3a06b35df2d`  
		Last Modified: Fri, 17 Jan 2025 01:33:31 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bb97ef72591d7a252d2c567d034f1d42c39c517e4bf7b40d76af00388a69a2`  
		Last Modified: Fri, 17 Jan 2025 01:33:36 GMT  
		Size: 12.6 MB (12565914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078c0c085a68b162b4a08ce3f62ee131733144fa995805dcbb1ec1c0bed32d93`  
		Last Modified: Fri, 17 Jan 2025 01:33:36 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a989d28458c66567b0462fb250a097a5e8e43fa6c99db424e0790d2752ee9b`  
		Last Modified: Fri, 17 Jan 2025 01:33:36 GMT  
		Size: 13.5 MB (13508578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccb8157a8df0c5fb29facf095e22d3a5e06bcda653decc4fd9a4c52b6cba26e`  
		Last Modified: Fri, 17 Jan 2025 01:33:36 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02c5080299e22b134ac88f26f4b139c8287e924c496e1df4d2641bcdef65b39`  
		Last Modified: Fri, 17 Jan 2025 01:33:36 GMT  
		Size: 20.0 KB (20027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e332158c0c707083d07db3f2918aa5541ff27a86a7fa5810ed217c892482dee9`  
		Last Modified: Fri, 17 Jan 2025 01:33:37 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3865be4f9df8d660092429c06afa189998e6bbd4ef0c09c0db9928fe311286c`  
		Last Modified: Fri, 17 Jan 2025 19:09:55 GMT  
		Size: 2.0 MB (1984906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a1e1077ca47a78ebaa2deab0a651a6ddb1cc01eb26cb76a05c45714f44419c`  
		Last Modified: Fri, 17 Jan 2025 19:09:55 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682f04c077f09f7d5e010085e21d8ab7ebfa3406b82d9f88576dc8f6d122cd72`  
		Last Modified: Fri, 17 Jan 2025 19:09:55 GMT  
		Size: 742.2 KB (742236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a92d8ffeba6c6a888766e38e35d76e4bf237769cfe2341df84d75897800c46a`  
		Last Modified: Fri, 17 Jan 2025 19:09:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e11b9383b1af5787ac014322ec2ea033b0bb25ef873076a2b0e5bf71b5adb6`  
		Last Modified: Fri, 17 Jan 2025 19:09:57 GMT  
		Size: 20.0 MB (20033235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:91060829d4127c2dca5cb26b411ae3c430c33b56899cb6583567e54c7c8730b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.9 KB (400866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad78f96b7595891996db90864c7e703102f80761998af3430e4092aa3196b44`

```dockerfile
```

-	Layers:
	-	`sha256:ea5c19d9b7c1d9beff7a13aa1c8d5c0ef6469cef68c673165ade185144422288`  
		Last Modified: Fri, 17 Jan 2025 19:09:55 GMT  
		Size: 364.7 KB (364730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d3e8b1e016385b35160954f32eb2a0e01e1a9502bef849ebf5cb705a89b0efb`  
		Last Modified: Fri, 17 Jan 2025 19:09:55 GMT  
		Size: 36.1 KB (36136 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine` - linux; ppc64le

```console
$ docker pull drupal@sha256:74b84d80f11e73635c7d6578d62cb0834676ef7ae5173f0d822fcc009863df9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55793281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c26fc79fc4b29e2514d5db12fc460777ca163208a0ae0fcd5dc32fc2deac4d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 07 Jan 2025 05:03:34 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e937f22521a2c5c57bad977a229d6e9072d584f968720e77c7468f3c07adc51`  
		Last Modified: Fri, 17 Jan 2025 01:40:50 GMT  
		Size: 12.6 MB (12565963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee2fef4b8ba52f45ba1a66f55a24b49b2c1ff5223ab683fe5fafc0545d1749b`  
		Last Modified: Fri, 17 Jan 2025 01:40:49 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad7e358e9c338d3f835700b6f489786f3dcc391427afaa4ab0b9ba7f75dc5f1`  
		Last Modified: Fri, 17 Jan 2025 01:44:02 GMT  
		Size: 13.7 MB (13676174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ac65a743e7d76f558c2bf53b7d11a2802a7e6ce2e55ea2c59bb892dda843fb`  
		Last Modified: Fri, 17 Jan 2025 01:44:01 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f57ceab25bd72011ba80ae068a79d6a6b3a33aead15a7ab9b8dd8ca6feac47`  
		Last Modified: Fri, 17 Jan 2025 01:44:01 GMT  
		Size: 19.8 KB (19848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403622d54d10d493a25581d099ee8432c3185b8b7424313137ed99d2669bb837`  
		Last Modified: Fri, 17 Jan 2025 01:44:02 GMT  
		Size: 9.2 KB (9175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99dda4d478a3c214e71b125ebde9ce9ee27870123296781fe7940ecbdec731d`  
		Last Modified: Fri, 17 Jan 2025 02:30:58 GMT  
		Size: 1.7 MB (1692189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20747467a5493db2ce8be5fc913191612a429bb8780acbfc31d6ab7cd195b3e4`  
		Last Modified: Fri, 17 Jan 2025 02:30:57 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585877577a5ae6e5bec58ffb451ec5a965ce69f317444613d59e6f450016095c`  
		Last Modified: Fri, 17 Jan 2025 02:30:58 GMT  
		Size: 742.2 KB (742241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c0d1d8e71a2494cd1872a1b9dffdad3fdd1b3fb0eb32a34521bf99f6bf1df3`  
		Last Modified: Fri, 17 Jan 2025 02:30:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e33a70fcdd77a95b5b434b9f48b8f00a64a88df283b56e0be9baa2c1324a90`  
		Last Modified: Fri, 17 Jan 2025 02:31:00 GMT  
		Size: 20.0 MB (20033187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:e8725d9bc56ca3526a15e911c5a7ecdd813cf8f64a865b9061a60c9c536ccf23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.5 KB (396526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d21959e4620c39f191f81dd9702d7fd346c70368c5de72b2d675636e09faaf0`

```dockerfile
```

-	Layers:
	-	`sha256:9db9af6cc8cdb11e4c66165454b43e0c2d323851bff11fcebd5eeb4ab0f305fa`  
		Last Modified: Fri, 17 Jan 2025 19:10:37 GMT  
		Size: 360.2 KB (360157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:717abedb88f9848a4a81e8cef9e93ad0a7f80aac4619274f37696f725dc7e2b7`  
		Last Modified: Fri, 17 Jan 2025 19:10:37 GMT  
		Size: 36.4 KB (36369 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine` - linux; riscv64

```console
$ docker pull drupal@sha256:79256a76be6c9670af4eb1eabf7fcd86cdf8bc9fc93df666b03defdcc15de9dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54371758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de6ef6c0ba4ef469a3c5ad4a19065be80b06c92565b924773e132870a4ea94b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 07 Jan 2025 05:03:34 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
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
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743579fbfa9d6a462255cb84fc5b099d3cf542442a9305bc0f96bce81c76e4f3`  
		Last Modified: Wed, 08 Jan 2025 23:26:57 GMT  
		Size: 3.5 MB (3457918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ac1c09c8b9181323bf079ede440cee01f0fec62e09b75afcae7c35627d0e6`  
		Last Modified: Wed, 08 Jan 2025 23:26:55 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0810a5f710bc8b0a06b441c232e302e968233890edb8bd1ae54afee19878e9f1`  
		Last Modified: Wed, 08 Jan 2025 23:26:55 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044c854e2cba647439f26a7d0b24155b340a9a97a8bea54cae4edb04ce316e3b`  
		Last Modified: Fri, 17 Jan 2025 02:24:28 GMT  
		Size: 12.6 MB (12565947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5208dea30f4cbfdbd69272b2539a5aceed97314ced7683c24f4e75682aea69b`  
		Last Modified: Fri, 17 Jan 2025 02:24:25 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec2e737da444f8cf56464c21df42f053a1a20f43f35dd6bc090a31fcf8a950c`  
		Last Modified: Fri, 17 Jan 2025 03:20:33 GMT  
		Size: 12.7 MB (12707916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657257c14b8e54699917dd349034c8d18b16bdc62c1e7f1eb1d680964213e21d`  
		Last Modified: Fri, 17 Jan 2025 03:20:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ebd4c148eccfa2f452d65d0bb8ba957238e07396d52644294130912e21e92f`  
		Last Modified: Fri, 17 Jan 2025 03:20:32 GMT  
		Size: 19.8 KB (19839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65527607b8b35978e44a3d2cf267580ac3f2f6286b5e52995027711f9d36f18f`  
		Last Modified: Fri, 17 Jan 2025 03:20:32 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af60101e28c49adcc45b8f383ec483d7ed0fc132a288d794962779737a78d1d5`  
		Last Modified: Fri, 17 Jan 2025 07:39:55 GMT  
		Size: 1.5 MB (1480350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5217ad15b46bcaf591b62c4cf87133453d2462889abceace8e81b3b78caef7`  
		Last Modified: Fri, 17 Jan 2025 07:39:54 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab8dca57785af2d99c017fa57ff3f0223bc448ccddc3b035e30490fd7bf5f91`  
		Last Modified: Fri, 17 Jan 2025 07:39:55 GMT  
		Size: 742.2 KB (742241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69b0e7d343e23067fa23fa965332e3b1e5ddd928da8b82628f5497ec7820fad`  
		Last Modified: Fri, 17 Jan 2025 07:39:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc4615debcb22b1b053853e0d5b54f166fc2f7e4ac91d15e5de7d4cb852f807`  
		Last Modified: Fri, 17 Jan 2025 07:39:58 GMT  
		Size: 20.0 MB (20033544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:0255ca11fa58e85be9fe603edd9dea03d45f30a45fefc3cab30e796831d78422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.5 KB (396520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1d03bed30ffdbea010833042aa240449eccdcfcbdc2538d3857fb1dae1eda7`

```dockerfile
```

-	Layers:
	-	`sha256:85e1a4baf26d7ebaff81f9302813b24b91dc28f0b01a6f060d99dc5f816a9d6b`  
		Last Modified: Fri, 17 Jan 2025 07:39:54 GMT  
		Size: 360.2 KB (360153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25b5f522aaab6765562b3d809b1f9db19494ffee7f1bbaa8b8589487cf7d4d13`  
		Last Modified: Fri, 17 Jan 2025 07:39:53 GMT  
		Size: 36.4 KB (36367 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine` - linux; s390x

```console
$ docker pull drupal@sha256:335aca1bb0eb586b4f5851be5a02e086f8e4dcfab49545f5368cb75d877a3a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.2 MB (55167345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3234ff01335f034865e165441bb2010179ca781ff2288418dfc75bc92d4dac8d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 07 Jan 2025 05:03:34 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282a4a0a714cd1f4efa558a9c16c549bcb3d98039f808a2da09f37551fac63`  
		Last Modified: Wed, 08 Jan 2025 18:38:12 GMT  
		Size: 3.6 MB (3561274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82035fdc219157bbb0deab69c2a1382fccf8a51ac5b20be190e26173e8a8be95`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31af6d9d81023b2dbb6d6e14114bb3c0a961f429216de8f8cdfd98fb13c317`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e2199922fd8d7b8d2453ad72d0f34a391222745fd39879844966ec900938f5`  
		Last Modified: Fri, 17 Jan 2025 01:47:22 GMT  
		Size: 12.6 MB (12565955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adde8da54c2f0f411f50cf6a809c4a1af1aee5affd7cb940e862bfdca93c3518`  
		Last Modified: Fri, 17 Jan 2025 01:47:22 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f7fb1fc245741323ebc4eb147da95dfcd8a2c6e0bb633d0061f597f51444c1`  
		Last Modified: Fri, 17 Jan 2025 01:51:30 GMT  
		Size: 13.2 MB (13152506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34851439a144f35dca37236ffcb0218a7ba02b3fc0d1b49db93660c3043c71b1`  
		Last Modified: Fri, 17 Jan 2025 01:51:28 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cddda9c549e9df5904213a2c37a90c34f6e4295fb9272bc5fcae0ab585797b5`  
		Last Modified: Fri, 17 Jan 2025 01:51:28 GMT  
		Size: 19.8 KB (19846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbf5ae9a1ef4a2a5234e34dc0987fcc6e4c2424e71f5b50c5cb7d4b4725de4b`  
		Last Modified: Fri, 17 Jan 2025 01:51:28 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a77605fe144fe8f76c70313ac63a9c6d68e34362b9be54d053ceeb180c93fb1`  
		Last Modified: Fri, 17 Jan 2025 02:38:10 GMT  
		Size: 1.6 MB (1611604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0223c6a34b768ce6e07e7ee08b978cc0ecb1a56df7f30f2d7d435b8f53dc45`  
		Last Modified: Fri, 17 Jan 2025 02:38:10 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f841091883967a5ad95522cb762437df83000f97671a7895b0e84a27b216498a`  
		Last Modified: Fri, 17 Jan 2025 02:38:10 GMT  
		Size: 742.2 KB (742239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9537a991c93f101367ddcec7851742bb68b21ecb4a8bdbc03c033ea68b2c63`  
		Last Modified: Fri, 17 Jan 2025 02:38:10 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ba7bae1b77024a2d388c8a097ef3f2924999ba50c44bc03b15c27cd799cc52`  
		Last Modified: Fri, 17 Jan 2025 02:38:11 GMT  
		Size: 20.0 MB (20033317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:b945764c63007793804d1e10f0668aa6acbe288d47ce938f7a95e5eee76a9e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.3 KB (396289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b664897dbd3df38abb9a1e5d625fa3f3dc729caf3a59d8643c135efd1654e2cb`

```dockerfile
```

-	Layers:
	-	`sha256:d797ff6eb7202d8aed8b7283f0ad1227410725a2fcc7f3839c5b78d94f71fbe0`  
		Last Modified: Fri, 17 Jan 2025 02:38:09 GMT  
		Size: 360.1 KB (360051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acb174d8f5651ecd63294975b07466d9ae8811aff08f9a8ca51c299ffbc69059`  
		Last Modified: Fri, 17 Jan 2025 02:38:09 GMT  
		Size: 36.2 KB (36238 bytes)  
		MIME: application/vnd.in-toto+json
