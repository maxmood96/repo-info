## `php:8-fpm-alpine3.20`

```console
$ docker pull php@sha256:5f6c116c7f4ac2cd8e23c2f94bcff487351e0591d1813e4c6d38bff2c0563c5a
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

### `php:8-fpm-alpine3.20` - linux; amd64

```console
$ docker pull php@sha256:e1db80be68f6f35d1d15f04c244a1f4d8682a2cacfa265e4ca498acb6671f3ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36098002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c58a6d485609e5467145f4ee966ebd8a2a13c7e3c5dd15ffe1691e6aa62b3f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2653fa3038fc4ab32e96dc90c8c646a14d0c790441a08eb91c21f131df2eff`  
		Last Modified: Tue, 04 Feb 2025 10:25:08 GMT  
		Size: 3.3 MB (3308837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1995fb12acb1fb9e116cab9f0cccdcb87b7043cae421bcec83ab9f9061e4f872`  
		Last Modified: Tue, 04 Feb 2025 08:00:11 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc06457927d7986a57a15ceb853fb7b9e252d322679e56fd42b9fb9e6439d4d`  
		Last Modified: Tue, 04 Feb 2025 06:17:15 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b664dbfe93331eee78709d3638a8596017c9a8e2efc474e375801484c4d9b95`  
		Last Modified: Tue, 04 Feb 2025 07:25:08 GMT  
		Size: 13.6 MB (13591311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f2a25968f2f1054f1ffdabb66cc90a1e6aae34afb41a702aa93b3a0abdfc13`  
		Last Modified: Tue, 04 Feb 2025 02:46:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1e9a93f8ff12cd68bb9b65f1981146237ddab2447c0122dafef61745a785b9`  
		Last Modified: Tue, 04 Feb 2025 00:14:23 GMT  
		Size: 15.5 MB (15538568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869474d63d39992409ddcd8ebbee979abfc43803dbb34536cb1e58f28e451518`  
		Last Modified: Tue, 04 Feb 2025 07:31:42 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d18c6f0186968eac71b948e7a5b26a766f856168b7fc96df0d2ecb8fee7c6fa`  
		Last Modified: Mon, 03 Feb 2025 20:53:49 GMT  
		Size: 19.7 KB (19711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c702e01c2ffd0c154fd9764db95a46ebde52214ae6275bdac53f7bf70900f1`  
		Last Modified: Tue, 04 Feb 2025 08:55:37 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:dbca3375523f2106f4f6cd4d947b01bd9fa8271a470b3baf92e1dba13c88d23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 KB (310635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00c047d162b370fca5a8ac4272d6b669248aaa05986297575efb758ec48a262`

```dockerfile
```

-	Layers:
	-	`sha256:2e682b64d8718895cf0b77e7ea51178379861cfed4378d78b9513285de8cbc97`  
		Last Modified: Fri, 17 Jan 2025 17:34:35 GMT  
		Size: 263.0 KB (262999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a9003573c59eb0a576d7fb8bf0bd3737a4cc96a61aa3ce0c970465c80a8e7d0`  
		Last Modified: Fri, 17 Jan 2025 17:34:35 GMT  
		Size: 47.6 KB (47636 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-fpm-alpine3.20` - linux; arm variant v6

```console
$ docker pull php@sha256:e972134f570490ae997a989af6b7cfe6db024d93b9e40e74841decf4c3e6e416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34458571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61cf4e8b536cbef898b64209c3657941d33c4de205a07166f6871658fac74ee6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php-fpm"]
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
	-	`sha256:d21788a5ef1e635e4bfe64d7196d0113334e154d3c1dc65eaca9cf779d04ebd7`  
		Last Modified: Fri, 17 Jan 2025 17:53:52 GMT  
		Size: 13.6 MB (13591305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c888fc374ce0913ea37202cc653237903ff2a18ce9c37fc86e71bc954be1f0b`  
		Last Modified: Fri, 17 Jan 2025 17:53:51 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe755687ef51c8eaf5d5a93169b9964fbb23b0ea77c436b5dd6c258ad9f7884e`  
		Last Modified: Fri, 17 Jan 2025 17:58:12 GMT  
		Size: 14.2 MB (14171458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ae1bdffa8b9af02b7c84f2330604e4baf64a480d643a68b3d7c449ddb9c95e`  
		Last Modified: Fri, 17 Jan 2025 17:58:11 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c7d0cc2b224bec0be7b69eca4d619c32a41c404537231b27abe0e537e3768d`  
		Last Modified: Tue, 04 Feb 2025 17:32:13 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e660660ec6156a56ff6e6dfe2d1df44066a51bb2c94422b760bc794a503393`  
		Last Modified: Fri, 17 Jan 2025 17:58:12 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:77a8fe551afa43cccc8eb6600fc2f49732bca27051a4be6fdaeee5c887f859f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 KB (47575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943206b38917b010bafffc44d41bdc814d1ea35ac7677338e9f8aa38c85c3b37`

```dockerfile
```

-	Layers:
	-	`sha256:b356ad8e78bdd9599cb80ae410535069e10f5b48b88135acc370904b931a2c98`  
		Last Modified: Fri, 17 Jan 2025 17:58:11 GMT  
		Size: 47.6 KB (47575 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-fpm-alpine3.20` - linux; arm variant v7

```console
$ docker pull php@sha256:1a527abd6809d51f14b96c024fc150b13b62d27c8b2b84fd0accdbea64bb371e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 MB (33176128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14e787f0e88d1ab3e53bb884d6213e8102ad8514634c0a38d662186cbada7a9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php-fpm"]
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
	-	`sha256:cc08194873d78ef80e3794ad0bd2bf83d738d08fa8349f0cc33be1747437f55e`  
		Last Modified: Fri, 17 Jan 2025 18:21:19 GMT  
		Size: 13.6 MB (13591301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6811d15a4f336b21f19ea5cb4e0b86f1a4d59a1fd329e2fd25ae87db74e1e94`  
		Last Modified: Tue, 04 Feb 2025 17:32:18 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7344a63e147b334c8b49b54b63f349bd30ad9dc377a36f0d2ab5ba554abce74f`  
		Last Modified: Fri, 17 Jan 2025 18:24:23 GMT  
		Size: 13.4 MB (13358202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87f75975e38d0c9ddd28bfac7f7ffbda3c0ea14f951e5e2bc7a559c2bba3331`  
		Last Modified: Fri, 17 Jan 2025 18:24:22 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9476992aca27ad65440bcd5e5f9098a1cde6aac1f5907f5b3e037a3718ced4a2`  
		Last Modified: Fri, 17 Jan 2025 18:24:22 GMT  
		Size: 19.5 KB (19510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fffd6d68f08ee1e69e170bf67398042b4cbf7de4e461f9c37e625996a9d8d9e`  
		Last Modified: Fri, 17 Jan 2025 18:24:23 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:4c5418029f6aed183042fe8ad1c1fc30813698750db0aac75a1ed7643b982be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.0 KB (307963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1493be07c54e907c6503284f0b245a15bac082fb1aff1e8e874654a2fdb25f`

```dockerfile
```

-	Layers:
	-	`sha256:762974ad5edd087d8f0da1f2bae6d552c5b3fd2d8baab92f8c317896b4cb97c2`  
		Last Modified: Fri, 17 Jan 2025 18:24:22 GMT  
		Size: 260.2 KB (260174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bedf2ea56872521555477778435715d695bf5c7a2034b1464b37e1c121dbd03`  
		Last Modified: Fri, 17 Jan 2025 18:24:22 GMT  
		Size: 47.8 KB (47789 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-fpm-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull php@sha256:9a24cef19459839f018d074fac0e187aa19e2b407b8ee012bbd9c8a9bc4ba7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36304990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74cfe0574d4c9d090b9bf29aec51f86715b0badfb3cc541e5255a8deacd99a8c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbfea75779fb9f51b30df44aa75d799257f21786a16d817ec263eb6cb4d24df`  
		Last Modified: Tue, 14 Jan 2025 20:48:07 GMT  
		Size: 3.4 MB (3360616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47781173f5085c5bf81fea23c55143896e3f61e88db6ca44fe803f5cff0e87b7`  
		Last Modified: Tue, 14 Jan 2025 20:49:42 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c52892499eb092197769cb95ccbc932a1373115445d0425ff828aa7d428bb5`  
		Last Modified: Tue, 14 Jan 2025 20:56:48 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff3428c786ab85214606f1fb2a621101f599a170fd548ae840069bec6fd4a52`  
		Last Modified: Tue, 04 Feb 2025 06:17:46 GMT  
		Size: 13.6 MB (13591303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cde94d14d45913d41dfd86417772929fb4c28b23d32c537eb9211759c21142`  
		Last Modified: Tue, 04 Feb 2025 01:26:37 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9c5923145566d7bea1adfec4a17cdbefa9383a897fd7de023b9771668c007d`  
		Last Modified: Tue, 04 Feb 2025 01:26:38 GMT  
		Size: 15.2 MB (15229490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc56c13aca1f18a9615559194f77eea6ce58757b0b6d6c8e68c83101e10a20a`  
		Last Modified: Tue, 04 Feb 2025 01:53:25 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e595673b29ea58bc34dfcfef9d5fbfa841ee811a7e437aabcb28dc6258079be`  
		Last Modified: Tue, 04 Feb 2025 06:17:45 GMT  
		Size: 19.5 KB (19491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9571e4b320df4e29727037b20cf2590dbafa76bbef79369d3e485555c107a1`  
		Last Modified: Tue, 04 Feb 2025 21:58:47 GMT  
		Size: 9.2 KB (9192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:8de122daf10ff93e707d07b4c202143ac80eeea779fa7109bb106bef23a12a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.0 KB (308024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9811e4f45d584ca6c7f730268eaa315b27696c27de1364ca0d44eef4b8c3aa6a`

```dockerfile
```

-	Layers:
	-	`sha256:27606c3ca27861cff728eb20bba4c75706b8547fac3179fdf61a1c16d1ed1cd6`  
		Last Modified: Fri, 17 Jan 2025 18:12:40 GMT  
		Size: 260.2 KB (260194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfa0405f12c311d6c3fd856ed6eba2d90c9522eb50dd8e22a28529b01d9e1ff3`  
		Last Modified: Fri, 17 Jan 2025 18:12:40 GMT  
		Size: 47.8 KB (47830 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-fpm-alpine3.20` - linux; 386

```console
$ docker pull php@sha256:5e5e859f727caf04a4a26c09157b6eeb60b801b04d164ab153257266e8c2647a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36403786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228ce1772d841647302218d3702e4dd8919a7f4e0473579177df22469f8330e1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Tue, 14 Jan 2025 21:25:38 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cef7ab53f263cde596e49b3671f126029dfbe625c130272cccef5aa20bad773`  
		Last Modified: Fri, 17 Jan 2025 17:34:48 GMT  
		Size: 3.4 MB (3359979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9188a8d97390c09678e311e003f022941425dc52aca1b3740d06c9a83b06b9a`  
		Last Modified: Fri, 17 Jan 2025 17:34:48 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2300a972684768e78c8c37ec22fedc601ef02d0add37d33baf9f6b87d8cab7eb`  
		Last Modified: Fri, 17 Jan 2025 17:34:48 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228e73ca44a6fb546cdccc710fbf129f0a864789ea4c4383f9fd30ce35c13b79`  
		Last Modified: Fri, 17 Jan 2025 17:34:48 GMT  
		Size: 13.6 MB (13591303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5e4d252f8b5d3f73ca635495a98ce1a8a027426d17a286575bb308b1b2b468`  
		Last Modified: Fri, 17 Jan 2025 17:34:49 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053443ae4aac0c3080c133e38ccf8344830c7971ec82b54d1ebd3a40688466a7`  
		Last Modified: Fri, 17 Jan 2025 17:34:49 GMT  
		Size: 15.9 MB (15948507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51573639da4d95cbcb9b94f03a65fd01cf8a899c0e4f896f7228b288e6710ef`  
		Last Modified: Fri, 17 Jan 2025 17:34:49 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cf3f1b4e47a5273882271225d6c0f1dc27cfe5684f6e66c1c577ef315b6826`  
		Last Modified: Fri, 17 Jan 2025 17:34:49 GMT  
		Size: 19.7 KB (19709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1696b04357c848b030e9183028add2b396ad08a4aab2dceedb856fd19058830b`  
		Last Modified: Fri, 17 Jan 2025 17:34:49 GMT  
		Size: 9.2 KB (9191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:7fdb0f1c5b5bb0487b8c633f8449ed8776580db5fd7b42103dcfc8bff0d4a687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 KB (310566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6962516fbded15331dafbd2f4c8bfbf8f6b934bf0f846fdd89a781497b9d14cc`

```dockerfile
```

-	Layers:
	-	`sha256:3853418f26a34d571f299f848e99c1f0db88026f0701ceb80a2be5d8c22d6c4a`  
		Last Modified: Fri, 17 Jan 2025 17:34:48 GMT  
		Size: 263.0 KB (262974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e82200bce9055667d2fb92d08b8cc5d417552aa600e5f78707975aa169b6efc`  
		Last Modified: Fri, 17 Jan 2025 17:34:48 GMT  
		Size: 47.6 KB (47592 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-fpm-alpine3.20` - linux; ppc64le

```console
$ docker pull php@sha256:75c8bb389a5b25d69f7e9af202217c43e9d0de356b8e3232ac4b5bdb3db6aa2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36689226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304eafa4d6042e82333c40a24e26c7929eae7bb52d293eacd241c2d47a5f9bee`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac389e1bad8c901cdd7df01f96be5f8508854f3411c6da9e6e8ef6668f4b16c`  
		Last Modified: Tue, 14 Jan 2025 21:51:58 GMT  
		Size: 3.4 MB (3435551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b7f9d7dcac76616498febca2aa6101a5ff06711026417e0332b7700a8e89f8`  
		Last Modified: Tue, 14 Jan 2025 21:51:57 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bef84277af6646e9da0330c1f81457cb9ace93a33c43f40275eb914946791c`  
		Last Modified: Wed, 15 Jan 2025 01:17:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e3a65824680ef5059132878bff73758762bed2b5fbba4744f3443d8eec286d`  
		Last Modified: Thu, 13 Feb 2025 04:47:44 GMT  
		Size: 13.6 MB (13591321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6487f66d5860eefc80a5d58e0c293a61adf8b6ef07a5200cc3620569574f46ee`  
		Last Modified: Thu, 13 Feb 2025 04:47:43 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13970194aeb3c83028a5b91c64bbd9b62f5148495ceda6d7939380d24777e790`  
		Last Modified: Fri, 17 Jan 2025 17:56:07 GMT  
		Size: 16.1 MB (16055126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9579fc6fa46dfe426805c91e1f80260e68348119535f129f16622a1b05fc04`  
		Last Modified: Fri, 17 Jan 2025 17:56:06 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899ac7dcad32276979078d96d6fd1f1013b8a4d1fb5f23baf9135feab772ea83`  
		Last Modified: Fri, 17 Jan 2025 17:56:07 GMT  
		Size: 19.5 KB (19486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0582b4796b2e4ce48a4a106a6b26082e6b6776a969e868fc4b937cfbd5a187`  
		Last Modified: Fri, 17 Jan 2025 17:56:07 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:1d9fb91ebbb45d8ce1918cab18f663400d6b43261fa9939772b0bc9daa5c4569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 KB (305913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165f6cb2aae74f74adece30518d7ea43061a1706064c00bfaaaccfc6a0c5e37c`

```dockerfile
```

-	Layers:
	-	`sha256:ce0a1e0ce85ed8d7fc81528596327039a5e7b4535e92529723f22407401ffbed`  
		Last Modified: Fri, 17 Jan 2025 17:56:06 GMT  
		Size: 258.2 KB (258221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cae2cba9bd8cbfeaa6453105f23568e5831bcd0fac984ced00747949cfd9227b`  
		Last Modified: Fri, 17 Jan 2025 17:56:06 GMT  
		Size: 47.7 KB (47692 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-fpm-alpine3.20` - linux; riscv64

```console
$ docker pull php@sha256:2ec47e69d88c6a8f8e1e7d24261617fc563f9bfc1dd9e25d42d767729f989b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35429664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994b42d307ba8656b353fd9acec7d0876724e76b9e93b2c0fdc0332f38062e28`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php-fpm"]
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
	-	`sha256:3a8d4cb81373d52ebe332f601c769bf452afbe98b97d1eca24e57909fb4c9998`  
		Last Modified: Fri, 17 Jan 2025 22:21:01 GMT  
		Size: 13.6 MB (13591306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d62d6d849391997642ba062f02b548a15ee9cda97702d7942b5b6399bbcc65`  
		Last Modified: Wed, 12 Feb 2025 19:11:20 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d714140c2b63ec73d8a2f6a47bb608df2feaa5ca8d6aa1605ec8483ebff1777`  
		Last Modified: Fri, 17 Jan 2025 23:15:48 GMT  
		Size: 15.0 MB (15005296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ee7d1d69b0964946926bc40e802bf919582c0c621517c168742ee5250f5101`  
		Last Modified: Wed, 12 Feb 2025 19:11:22 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f1b58d173b7c9ad58a70e769e36b3d2a009067a8dbd524f805d2be2ed934b5`  
		Last Modified: Fri, 17 Jan 2025 23:15:46 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089b8dbd174b2ac563999fa01b02d54e0002b1e57e2393565594be98ba483460`  
		Last Modified: Fri, 17 Jan 2025 23:15:46 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:646b2ac073d20330a4d4ee68fb8da4be6b7c5763d35697ef767c7c3e5e8cc6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 KB (305908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3074840af407c51f1ad09e342beae5f4f8e4b8175772ff20bf9b7fadb91ad962`

```dockerfile
```

-	Layers:
	-	`sha256:dcefa2da6063e9e646c17472914a98ad610c0136eaded9f746b2ac634865d0ec`  
		Last Modified: Fri, 17 Jan 2025 23:15:45 GMT  
		Size: 258.2 KB (258217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f13e1ac268ec6b753737f31f40aae043816f1d73152b7ddd0a834dae406b3705`  
		Last Modified: Fri, 17 Jan 2025 23:15:45 GMT  
		Size: 47.7 KB (47691 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-fpm-alpine3.20` - linux; s390x

```console
$ docker pull php@sha256:3900ae48bff8f144d6471ad24967c1b2e02cc5fe0f6eeb10315d89865e357cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36324513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2532a8b8815622bb14ad9b2a1fd3546ce08790ba356ed437dc3f6161e5a1ac94`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Tue, 14 Jan 2025 21:25:41 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f228edf04a39559d957ef5581b08c9a7d393dc64a098575e63c061140ae78557`  
		Last Modified: Tue, 14 Jan 2025 21:51:57 GMT  
		Size: 3.5 MB (3501854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3a938ef64c5dda4d67df22456ef7b998d8d733e6b109f8565eae8077a42767`  
		Last Modified: Tue, 14 Jan 2025 21:51:57 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8665be221001567b6093cf5d6fd1080ca3c33832bf4656568c06b3f7959c83`  
		Last Modified: Wed, 15 Jan 2025 01:17:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cae6063b04fec9c01d657a94132af13ae5680a4cacd94c87d25c198571800f`  
		Last Modified: Thu, 13 Feb 2025 04:47:45 GMT  
		Size: 13.6 MB (13591300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece051e91e83a0d9e2e9572037a896344c106daa63d502969a69ac96eac6357d`  
		Last Modified: Thu, 13 Feb 2025 04:47:44 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bb997ed721fd862a4b766e0e75878059040838c8eb96236931d6d213416b9e`  
		Last Modified: Fri, 17 Jan 2025 18:00:39 GMT  
		Size: 15.7 MB (15735207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643ea97f15403cba32402f50d9e4268816a26afda405b22a578c6b0fa123fbb4`  
		Last Modified: Fri, 17 Jan 2025 18:00:39 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d1b8f72a52a2a6ebf22e52bad5b3a83aad10e35a44ee5557bb6b745ace8f5f`  
		Last Modified: Fri, 17 Jan 2025 18:00:39 GMT  
		Size: 19.5 KB (19496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c8c2db747da91b3191ccb2d10fea39e972415fb1abf6071a339d88e5737208`  
		Last Modified: Fri, 17 Jan 2025 18:00:39 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:60680bb3bc56d3f455f2502534db2aaacbf11bb1f56869d4622a05a1a266050b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 KB (305823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa2e29005bc86325b33c1dbb677cf6faac016039505f8204a0d6c43a875e1072`

```dockerfile
```

-	Layers:
	-	`sha256:84accd32e8f9503cb0036ecb43781fba06e4f41f3e73a6b5c1cf3ca52c221466`  
		Last Modified: Fri, 17 Jan 2025 18:00:39 GMT  
		Size: 258.2 KB (258187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6c1765d82c241ea606b927039cf0e8bff48f1a075188a4183aac7e8ba58d7b7`  
		Last Modified: Fri, 17 Jan 2025 18:00:39 GMT  
		Size: 47.6 KB (47636 bytes)  
		MIME: application/vnd.in-toto+json
