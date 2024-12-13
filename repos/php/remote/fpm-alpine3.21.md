## `php:fpm-alpine3.21`

```console
$ docker pull php@sha256:dcbcd25f19919d0d80eff895322d8f8d75f0aa75ff21f906e3da11a63bd74fb3
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

### `php:fpm-alpine3.21` - linux; amd64

```console
$ docker pull php@sha256:661709ebd2995433800a6f617072d40a0c52a4f3abfae1db4d4a3e280b3ddaea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36209701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd16d2a0aaedb88dae22334b937d796ab2720b8146305ea765a79d7713df4cf4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Dec 2024 09:57:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Dec 2024 09:57:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_VERSION=8.4.1
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 07 Dec 2024 09:57:27 GMT
WORKDIR /var/www/html
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
STOPSIGNAL SIGQUIT
# Sat, 07 Dec 2024 09:57:27 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 07 Dec 2024 09:57:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93eeb75053d8a1a70ab07195971427472fdce022d4c893e17f073c05a361ee4e`  
		Last Modified: Wed, 11 Dec 2024 23:35:41 GMT  
		Size: 3.3 MB (3335087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d561dc5f913bf5ac5c30d9c4d42bdf7aa341b8fba0e0ded0354c6e1aca173438`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a465f443f2fadb2b0191af2eb2aae7a8ff4e66fef38973f7b9f36688fc1ff5cc`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13f9742f73a6fa9912965eebfb2b8d038e3d515f16744be4f7fdac1e322361f`  
		Last Modified: Wed, 11 Dec 2024 23:35:41 GMT  
		Size: 13.6 MB (13573065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20aacfe2a7e63ac6a466fdd1e475e04893747676adf77fd7c97952a74c93e137`  
		Last Modified: Wed, 11 Dec 2024 23:35:42 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8459d08a3711cd4e6a91411598c182de60fcfb38528aae2eb5356ac02f1652`  
		Last Modified: Wed, 11 Dec 2024 23:35:42 GMT  
		Size: 15.6 MB (15623716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4973e1d2f291823ce103f0f6504fb450696167804965e80eb980ac367d7a5a0f`  
		Last Modified: Wed, 11 Dec 2024 23:35:42 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936612d1745f88175c1f20aa5e1148a96d01261c14560a00b5c860d1f8c70922`  
		Last Modified: Wed, 11 Dec 2024 23:35:42 GMT  
		Size: 20.1 KB (20066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31da68ed88d50ad5128037e9a04e67af9181507bd2a3a020a4d724719ffd8bd`  
		Last Modified: Wed, 11 Dec 2024 23:35:43 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:90d57c1925e2c056df8e8c0dbf09e86866731801cb6b64f088edb323ed4dff4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.7 KB (319678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e960ea736ed9495f599189ffd49effec2ce483895841ed6e76b881871a671d`

```dockerfile
```

-	Layers:
	-	`sha256:b4a54b8555fba308028480c3fd8bd39ee1164f2a60a0c9fcbd2e65bc7da77457`  
		Last Modified: Wed, 11 Dec 2024 23:35:41 GMT  
		Size: 270.8 KB (270818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d6ff6180b7b12403ab4a532e879fc356de90530ea3756dda0755f240feb0220`  
		Last Modified: Wed, 11 Dec 2024 23:35:41 GMT  
		Size: 48.9 KB (48860 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.21` - linux; arm variant v6

```console
$ docker pull php@sha256:ba28d71cf0f6856240f986c2959bb565237cba63e1cc0242b1760b5900a309f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34432655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2a6ba670af98cc5d82d04288985f25b40863ef287bcabf2ce68f982e13ebb8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Dec 2024 09:57:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Dec 2024 09:57:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_VERSION=8.4.1
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 07 Dec 2024 09:57:27 GMT
WORKDIR /var/www/html
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
STOPSIGNAL SIGQUIT
# Sat, 07 Dec 2024 09:57:27 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 07 Dec 2024 09:57:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b736a50b989ce147c8a50cd4eff3990052fbae41313316dd15bdd3ae41bb055`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 3.3 MB (3302897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520076a7063b8a800f7aeb276beb6363fa2c2192a17d803ee3f5fa20b0b0b211`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065854d8dae5a225e01a05809bd10528e215d02290cc6d9f51d4bc29dc1ac134`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c626ecd80716f5c5a684662046769c61c669d292084ebe6f9300b07542470fe7`  
		Last Modified: Wed, 11 Dec 2024 23:46:06 GMT  
		Size: 13.6 MB (13573094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0558011eb01fafcdfc6d1a5db0174996f259d322e58c6bbe550960e2b86d1844`  
		Last Modified: Wed, 11 Dec 2024 23:46:05 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fa01c8a9b281a50472dfaedf6245e12b5523e7f9c35377823e1e7c3ff4b07b`  
		Last Modified: Wed, 11 Dec 2024 23:50:11 GMT  
		Size: 14.2 MB (14156277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9889b29a3ef38cb4dbfd00956bfd8f6dcd5b2dc27f8a3be402d23ea33c400d1a`  
		Last Modified: Wed, 11 Dec 2024 23:50:10 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5876d4dbfe50f9e4f62e30ca6d69a390d26d4b4f5c70b27639f068f9f55fc5a1`  
		Last Modified: Wed, 11 Dec 2024 23:50:10 GMT  
		Size: 19.9 KB (19884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab79a720b2c09901364f2a3e329222dba918685a769e9b43e071b92703bf5a7`  
		Last Modified: Wed, 11 Dec 2024 23:50:10 GMT  
		Size: 9.2 KB (9192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:b30d9c4832c93351932f7c64be2008f48b6b0551cd9a21594b3bafdbd9192ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 KB (48831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cf9a94eb19e5a8947f24eb3cbd9da34154fcc97bdcc3c5a672d82882c68e59`

```dockerfile
```

-	Layers:
	-	`sha256:63c2ee5db785c26405ddb7de1cd6d8976f83a2181149f8eb7ec5f24455e1ecdd`  
		Last Modified: Wed, 11 Dec 2024 23:50:10 GMT  
		Size: 48.8 KB (48831 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.21` - linux; arm variant v7

```console
$ docker pull php@sha256:15543dca9a94229ad97dae5c8b9a2df161d0c06ec9a92e55922da3f30fd9d283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 MB (33248270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e7572e17ee19ce154f3f3ab6478264edc803aa0eb445cc3cdec3579ddf169c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Dec 2024 09:57:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Dec 2024 09:57:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_VERSION=8.4.1
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 07 Dec 2024 09:57:27 GMT
WORKDIR /var/www/html
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
STOPSIGNAL SIGQUIT
# Sat, 07 Dec 2024 09:57:27 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 07 Dec 2024 09:57:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e58a80555964d79b4c54d0bc69d1ac3c99d92bfa41dc077ad9039581c976fe1`  
		Last Modified: Wed, 11 Dec 2024 23:35:20 GMT  
		Size: 3.1 MB (3128235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30daf13605f2d1179f6005fb32926b33b8626b9ceb92de019df902d09cedf935`  
		Last Modified: Wed, 11 Dec 2024 23:35:19 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7365fc515397f6962469f3d1c8654b5801822a766158bca2e8a9fa961d78db8`  
		Last Modified: Wed, 11 Dec 2024 23:35:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46234f84a591182641b5590fe4e04a71ddd05a47082e61983e6d868dcc79cdfe`  
		Last Modified: Wed, 11 Dec 2024 23:48:08 GMT  
		Size: 13.6 MB (13573104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f3109f721f75e7b84cc380538d75d2799a5dd2df9204d6c2fb3347e2e4cb1c`  
		Last Modified: Wed, 11 Dec 2024 23:48:07 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170c2131476bc45d559098067aa59d6fece57ab08c18efca7098094d27a9bc1f`  
		Last Modified: Wed, 11 Dec 2024 23:52:14 GMT  
		Size: 13.4 MB (13413675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dac3d99808e9acd557235975bb64cd4c557e7ff6b5ac56cac8a5b02e170744b`  
		Last Modified: Wed, 11 Dec 2024 23:52:13 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e918f99a6a9025e6ae1a6dacbb37cd7694c3b32fdedd4a14afff4cf433f276f`  
		Last Modified: Wed, 11 Dec 2024 23:52:14 GMT  
		Size: 19.9 KB (19896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78489678b64137a44cd26d59541f622ed698c86bb0b563107e90d727d2b1cf68`  
		Last Modified: Wed, 11 Dec 2024 23:52:14 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:e791a6d7871ee7248092429e259b83445004d02afa7a17096b64b4d7c70afae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 KB (317115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72bfae63d58d66ff9af39ceeb258a2e418a65d391d03ba641c676408bc9ed9d0`

```dockerfile
```

-	Layers:
	-	`sha256:d6bd57db5f78c51f88e22c8566fd2a2f8e50c59d000510b9176702819f8b4bda`  
		Last Modified: Wed, 11 Dec 2024 23:52:13 GMT  
		Size: 268.1 KB (268070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b054b6d75a5a810b71aac40c862c312585facf68b08490457d9bb499cb5d19d`  
		Last Modified: Wed, 11 Dec 2024 23:52:13 GMT  
		Size: 49.0 KB (49045 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull php@sha256:eaae7977a71c799306eb69ad7ee114cf856c4de37bf4c3f782e7fd9e89f95760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36190526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b07c5ea5e4625ee5394028fa69f5729046b3f9a22ef81af44a746e01ee0728`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Dec 2024 09:57:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Dec 2024 09:57:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_VERSION=8.4.1
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 07 Dec 2024 09:57:27 GMT
WORKDIR /var/www/html
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
STOPSIGNAL SIGQUIT
# Sat, 07 Dec 2024 09:57:27 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 07 Dec 2024 09:57:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02eb691f526c59a4feade4837dd3c26533d9fe4c9306da60dc23a30620af346`  
		Last Modified: Wed, 11 Dec 2024 23:34:10 GMT  
		Size: 3.3 MB (3331581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f32f7c87db3a6447e39cf371cb0c2bb2c95f7a814793eff967d2a9a3b95122`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7c12be75768edb813fc94e2e1d2c48d7cb1f4cea2c832026ca6ae796dff9ac`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcf41220f696f1ec3f3f3b53534f127b841636f0ca74e73210df73c7afefd94`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 13.6 MB (13573084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809689fb0b0450d700790c2f857ee46f0365fcb59cd3a227a736a8490de3c543`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f976215c3cf5b49d86169d42e9fa09e8069f17acb69caae622053351c8729e`  
		Last Modified: Wed, 11 Dec 2024 23:49:37 GMT  
		Size: 15.3 MB (15259459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb3b0856735ddfa340e3e5078e311847887eafd8d97c273929f7e53527b19b6`  
		Last Modified: Wed, 11 Dec 2024 23:49:36 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428877b6140c787278a952ed3b34f6f6411b6acfc00ea3f64c5dc4250a06a50c`  
		Last Modified: Wed, 11 Dec 2024 23:49:36 GMT  
		Size: 19.9 KB (19887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c639250e56006fd189cb393dc37722259eb038bfaa4ac13fc0cf07c2c96d7362`  
		Last Modified: Wed, 11 Dec 2024 23:49:36 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:6d2eb6faf90d72a26cf187f13a43377e5b358a1c50255ca6abfcfae4fce48a98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.2 KB (317208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e31e32569720d287136c693ed92b433558b979c7a404650c2222f2f2bc7d6c`

```dockerfile
```

-	Layers:
	-	`sha256:c818e7dc7694098ef5dc86e9054246f5e7310b8464e9dfe888d37dd97abd5649`  
		Last Modified: Wed, 11 Dec 2024 23:49:36 GMT  
		Size: 268.1 KB (268106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a36ee0fa32e1fb7dd504c60ab54c1cc9370bc3af2d6abca7e692e16cbe34ffd3`  
		Last Modified: Wed, 11 Dec 2024 23:49:36 GMT  
		Size: 49.1 KB (49102 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.21` - linux; 386

```console
$ docker pull php@sha256:499a9921f29cec65283cc349595e4214e53211d94f0f826d33e7ad983c4f5cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 MB (36457261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a75b7f04920ed7e2423ef23facd70fdab8af244b616184c30f92b7a7d718ee2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Dec 2024 09:57:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Dec 2024 09:57:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_VERSION=8.4.1
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 07 Dec 2024 09:57:27 GMT
WORKDIR /var/www/html
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
STOPSIGNAL SIGQUIT
# Sat, 07 Dec 2024 09:57:27 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 07 Dec 2024 09:57:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec63d753a66019d0506eedbd2698718dda3e92df8f2852e56b62cd59c8d0a36`  
		Last Modified: Wed, 11 Dec 2024 23:36:31 GMT  
		Size: 3.4 MB (3376207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d530c0e6934798b4dedf2bf65c3370d88f2cdeb0557d47303a7cece6539428`  
		Last Modified: Wed, 11 Dec 2024 23:35:43 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb82371a0c17328001566c01f034162e8c082082318b31c52940a8a5906dcae`  
		Last Modified: Wed, 11 Dec 2024 23:35:43 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81129bfbb70cfbf194277db80399982a3df2083ec48fbbbc31c76afd5bfcbcc`  
		Last Modified: Wed, 11 Dec 2024 23:36:31 GMT  
		Size: 13.6 MB (13573041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411c627caa3ded5267657eaaff09786f8dcf7fc9d5997b468551bebe5d4c9993`  
		Last Modified: Wed, 11 Dec 2024 23:36:31 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e59a6701cc5e8a836595b4ad8186866a4242fee062715422c2306dae6f13f6`  
		Last Modified: Wed, 11 Dec 2024 23:36:31 GMT  
		Size: 16.0 MB (16008546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7993174a9f32d8878fa9926ef7523e7571df90d14d4c32f92d611c461dff37a7`  
		Last Modified: Wed, 11 Dec 2024 23:36:31 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1275641edf69da778572bc13968350da1cbec2a0c62ea0261a632f44410aa28f`  
		Last Modified: Wed, 11 Dec 2024 23:36:31 GMT  
		Size: 20.1 KB (20064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46846bb5f3bc5f579cb4859636ea216b8373850e4376a00376745b5fb956855`  
		Last Modified: Wed, 11 Dec 2024 23:36:32 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:b8b6c14d0795f64fb5ed5640964104e0a61007b5c5bdcdd101748dff642278a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.6 KB (319569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1502b5e48ae1af98a1744013e09b86ca9a0b959379023f3c83dc9c8fa26e823f`

```dockerfile
```

-	Layers:
	-	`sha256:7882d8abd95ab08afdca8da3712659c9a38773f0b15865c6c8c5d2beb7268d80`  
		Last Modified: Wed, 11 Dec 2024 23:36:30 GMT  
		Size: 270.8 KB (270773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7f5b029deb20a09fee38fbe0a2ecea6e72621e7a6c1871c7280399579d8726b`  
		Last Modified: Wed, 11 Dec 2024 23:36:30 GMT  
		Size: 48.8 KB (48796 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.21` - linux; ppc64le

```console
$ docker pull php@sha256:cf0a7939f55311bf29fbb0bd564a68ad15b2ebfab26bf24b31ecdb3a94a8795a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36767694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c5a57d4f6dc190be545c1ac5c98b5ec2d541b69e3c93b28033497b625dca14`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Dec 2024 09:57:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Dec 2024 09:57:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_VERSION=8.4.1
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 07 Dec 2024 09:57:27 GMT
WORKDIR /var/www/html
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
STOPSIGNAL SIGQUIT
# Sat, 07 Dec 2024 09:57:27 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 07 Dec 2024 09:57:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dab8c9093e7207bf34d7e27bcaf8a12d512bc9a6228a188ccd032ab556c048`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 3.5 MB (3474267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887eff0819f1e81cf0537030ec0eefbed710884b4bdcb74a53300dafe99af22`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40d10c33dd4ddf3d7039e24ae3ea2657811b8add42853a37557baa89339c584`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3708563094bdeb69b89124b79d07a1f082713efec0e595c079930180fb6d4955`  
		Last Modified: Wed, 11 Dec 2024 23:42:30 GMT  
		Size: 13.6 MB (13573079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a7589b163bca027b4edba09f13de85c98ca7f239d8d9502595b0aff0e783cb`  
		Last Modified: Wed, 11 Dec 2024 23:42:30 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fd32089ac597dce704738cef23299bdefe9395b62b64c642d841ea3ce47ff2`  
		Last Modified: Wed, 11 Dec 2024 23:45:46 GMT  
		Size: 16.1 MB (16110025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65850f3c16b63936ae1c8f12ec1b15b7edce4ebe66942a3700d72c8e17780c17`  
		Last Modified: Wed, 11 Dec 2024 23:45:45 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704bc0aecb3fc1ca97faf9a26c1a1966b6ee5b59438a18a36e0be6a89a92b733`  
		Last Modified: Wed, 11 Dec 2024 23:45:45 GMT  
		Size: 19.9 KB (19891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c961ecf9c8e12dbe349946df6b24cacdd7b665c0b382351ad2d56a5ae125e66b`  
		Last Modified: Wed, 11 Dec 2024 23:45:45 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:015796ccafd596c13f17ec1524f0074afe8a069aaf7aba5da78195535219d60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.0 KB (315046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05985a0205308712d7b66794c7316c389ba4f0988a8f37a017ac6ab0f9316ba0`

```dockerfile
```

-	Layers:
	-	`sha256:b656254bb99542b8edfc1b727c3f6abc1efd90fb60fc503d5ee3ef49f6362c6d`  
		Last Modified: Wed, 11 Dec 2024 23:45:45 GMT  
		Size: 266.1 KB (266106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b5f823952924f0e1ea2757a2cb08ea24c582e1428d3eac9decb42c3712d0ad0`  
		Last Modified: Wed, 11 Dec 2024 23:45:45 GMT  
		Size: 48.9 KB (48940 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.21` - linux; riscv64

```console
$ docker pull php@sha256:c7e8d93ba463fa94bdcf0e1652c00705c704f830c8a13bcb4ca7ed82216c4388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35449225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:793ec4262a045b1557db6e7f430db93face98cc4d7daec30e862f3966c0c4809`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Dec 2024 09:57:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Dec 2024 09:57:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_VERSION=8.4.1
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 07 Dec 2024 09:57:27 GMT
WORKDIR /var/www/html
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
STOPSIGNAL SIGQUIT
# Sat, 07 Dec 2024 09:57:27 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 07 Dec 2024 09:57:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
		Size: 3.4 MB (3445761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9c93fa8ac38e6017fe5251627d738084239fbab425319ead8bdece897e493`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b65b4aeb40f99d5493f73d9206995a90aa94768378fa8ed5e3d1bfa1a5650e5`  
		Last Modified: Thu, 12 Dec 2024 05:33:08 GMT  
		Size: 13.6 MB (13573066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d3a97d778691306fc952ddd90fe8250103f76d9aeb4d0203ae146e8e521bae`  
		Last Modified: Thu, 12 Dec 2024 05:33:06 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2234f600356f28830a0637ad86c6eb271a88c33c6971dd9b9a8b52fccc474b21`  
		Last Modified: Thu, 12 Dec 2024 06:32:02 GMT  
		Size: 15.0 MB (15043169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5cddbdb141090ea56ffa215c9c2a671975308173dc3032aa18a535df6617e6`  
		Last Modified: Thu, 12 Dec 2024 06:32:00 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450b0e81191534a9d49f91fba641cc39f05429945137aa566fb80196599a9477`  
		Last Modified: Thu, 12 Dec 2024 06:32:00 GMT  
		Size: 19.9 KB (19870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff3f7a148422816cecdbabbc20455b35e5224b12c579be8b6360c40384b5e38`  
		Last Modified: Thu, 12 Dec 2024 06:32:00 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:fadc37b4a5e9e50861bb4388e7420531c1e13a605c3c3dd28cbc85e1dede0763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.0 KB (315042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618174908dfa91abfb3f7603fe84fd8baaae2c8702fefe770662885a31872862`

```dockerfile
```

-	Layers:
	-	`sha256:1d667dcce6c516e5f72533b0782619ee1aed16a3628a46d3e5126473aca557ef`  
		Last Modified: Thu, 12 Dec 2024 06:32:00 GMT  
		Size: 266.1 KB (266102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a003b4a59e0fd8d655b5bc16d0dd784a4521636a284033f77e08a6426c89d2a7`  
		Last Modified: Thu, 12 Dec 2024 06:32:00 GMT  
		Size: 48.9 KB (48940 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.21` - linux; s390x

```console
$ docker pull php@sha256:2882047c760ed080571df71efc19315491b9f9198e79be064033eb3513fa86e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 MB (36451108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be89313bb89ddfcc19fa031dc57b0a989e53e82e7c850479eb2bf48aeb741c9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Dec 2024 09:57:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Dec 2024 09:57:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_VERSION=8.4.1
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 07 Dec 2024 09:57:27 GMT
WORKDIR /var/www/html
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
STOPSIGNAL SIGQUIT
# Sat, 07 Dec 2024 09:57:27 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 07 Dec 2024 09:57:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4b02d148e9caeb82d2cf6c286e6c9c576dbce389f6c2cb18910b789ebd4813`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 3.6 MB (3561751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d561dc5f913bf5ac5c30d9c4d42bdf7aa341b8fba0e0ded0354c6e1aca173438`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a465f443f2fadb2b0191af2eb2aae7a8ff4e66fef38973f7b9f36688fc1ff5cc`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fedb1f25ba3b80074435858fc7794f83dc60e8736ca21254eab5159475f8ce4`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 13.6 MB (13573088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2c1315e733813b79535cafe40777595657596cda0a210db51f85480bfef1d4`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41803c5c8c9a11033c90b952d7e6480f0da5e1b5959b3d713e0b31c3b8962540`  
		Last Modified: Wed, 11 Dec 2024 23:48:51 GMT  
		Size: 15.8 MB (15813538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd9d11c484f341ac10c114edef26e193d71e4ea6e25f3a4a15d6426af984af3`  
		Last Modified: Wed, 11 Dec 2024 23:48:50 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a067402dd09485b3a00781df32e6e5dbfeaf40559879f9d751b14852e57de31e`  
		Last Modified: Wed, 11 Dec 2024 23:48:50 GMT  
		Size: 19.9 KB (19888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff1143fac8892812d28aefecc08eae3044a823224f0f9995bbfb77eee896b77`  
		Last Modified: Wed, 11 Dec 2024 23:48:51 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:482960cc39239cdf37a000b34c84a201b80a31a2785c5215b0870644396d6c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.9 KB (314908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9f31874cdbd9c097f18bc0521ab0b86d3fca88880a1408f9923639bb0375e9`

```dockerfile
```

-	Layers:
	-	`sha256:e14cf7ac48f4a1d9592f5a0c01dc4f26e68044cb3ea90a7df9c50de5c1f8d386`  
		Last Modified: Wed, 11 Dec 2024 23:48:50 GMT  
		Size: 266.0 KB (266048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd1e2eeb31aae0923f946312cc5bdd864d956f038ff2bc01d5ad0dd466c93d48`  
		Last Modified: Wed, 11 Dec 2024 23:48:50 GMT  
		Size: 48.9 KB (48860 bytes)  
		MIME: application/vnd.in-toto+json
