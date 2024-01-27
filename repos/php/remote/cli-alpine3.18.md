## `php:cli-alpine3.18`

```console
$ docker pull php@sha256:a5534ecf3d62b29076f478e880beec0a080db23999ca3ea105f915fc71c293f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `php:cli-alpine3.18` - linux; amd64

```console
$ docker pull php@sha256:008042056cca585df8dce8fd3210d9432576e90a2e0e1c709d5af464f9c8370d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35589541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec34653cf72aec558fbfa363c3ab99317099b94992865c2789a21ce170c7ef1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:35:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 04:35:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 04:35:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 04:35:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 04:35:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 04:35:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 04:35:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 04:35:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 04:35:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 27 Jan 2024 04:35:39 GMT
ENV PHP_VERSION=8.3.2
# Sat, 27 Jan 2024 04:35:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Sat, 27 Jan 2024 04:35:39 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Sat, 27 Jan 2024 04:35:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 04:35:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 04:39:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 04:39:18 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Sat, 27 Jan 2024 04:39:19 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 04:39:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 04:39:20 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdd08544f3979add7a1135032c708137f3a42762bb48446a036a80d16a9c796`  
		Last Modified: Sat, 27 Jan 2024 05:37:35 GMT  
		Size: 2.7 MB (2682495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f2d92bc3b905b7db953512ceb84266e42e19d498f9d6c4c91170b5360cf3b2`  
		Last Modified: Sat, 27 Jan 2024 05:37:35 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7427b71a5dd639a1a4b6123f46f2d5c6e6f8bd6d7bb8f8ca879516220b330d9`  
		Last Modified: Sat, 27 Jan 2024 05:37:35 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46ed5ffd1b5ac1adb35a42dc7f1bc2015035a355e5fa55c10a3c95e5dcedcec`  
		Last Modified: Sat, 27 Jan 2024 05:37:34 GMT  
		Size: 12.5 MB (12460693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415e0429f1b13b8528353dfa55187e56f2cdb716b43764645f30d6b79b07b7d0`  
		Last Modified: Sat, 27 Jan 2024 05:37:33 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560bb6d2b0101e951b7a28575231d06e326adde64dc99327d78cbe6c477c43ca`  
		Last Modified: Sat, 27 Jan 2024 05:37:36 GMT  
		Size: 17.0 MB (17020394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76160fb9d63ec00f194268709d052f5a75a204d66da3caa633eee4ae38c3ff4d`  
		Last Modified: Sat, 27 Jan 2024 05:37:33 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7290690d035cf8b921d1a5f5131eb1f3e6e455fed2e55373311c4f8a54b41e`  
		Last Modified: Sat, 27 Jan 2024 05:37:33 GMT  
		Size: 18.9 KB (18950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:cli-alpine3.18` - linux; arm variant v6

```console
$ docker pull php@sha256:3bb012173e11404dc9583eedb40762d149d93be77746f81fd45e4e0bd908a904
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33882801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51821896ba9e279ae63b5ea133046314b2aade94584b1373bdaf53c869fddef`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 05:34:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 05:34:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 05:34:26 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 05:34:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 05:34:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 05:34:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 05:34:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 05:34:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 05:34:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 27 Jan 2024 05:34:27 GMT
ENV PHP_VERSION=8.3.2
# Sat, 27 Jan 2024 05:34:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Sat, 27 Jan 2024 05:34:27 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Sat, 27 Jan 2024 05:34:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 05:34:35 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 05:39:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 05:39:58 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Sat, 27 Jan 2024 05:40:00 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 05:40:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 05:40:00 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62daf641b680894f28bde55f9b558dcd71afae65a613d7289839b0ccc1c59935`  
		Last Modified: Sat, 27 Jan 2024 06:45:53 GMT  
		Size: 2.7 MB (2688488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bbdb0364f95226b0ddc30b86f27a68af4cb1b836ca10db53e713f447ff13bc`  
		Last Modified: Sat, 27 Jan 2024 06:45:52 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72425da7bbe49396c65f29cc1da85be4ba13d8917fa75ad08fd7a48974409d13`  
		Last Modified: Sat, 27 Jan 2024 06:45:52 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01e8350bc9a68ae4c2c6d4e6653c77d662ba56daa9f0bbf52901a37cfef7426`  
		Last Modified: Sat, 27 Jan 2024 06:45:51 GMT  
		Size: 12.5 MB (12460682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e97475420bc37e47fdd21e24b34a3d7407cd618b80e88e7fedaa9f04e7474d0`  
		Last Modified: Sat, 27 Jan 2024 06:45:50 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce21f5fe010c4346514f59b88ce16402b12a90853ebc73936f40fc4cf2f23f8`  
		Last Modified: Sat, 27 Jan 2024 06:45:54 GMT  
		Size: 15.6 MB (15563336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d417448761b3652ec326c34fd89ea3869f598de259d325c37289ac3e7cc8ec3c`  
		Last Modified: Sat, 27 Jan 2024 06:45:50 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db37661a2be1dee1faaace14afb8e02bac41ad9077c107db6a247c57ca4f6dc5`  
		Last Modified: Sat, 27 Jan 2024 06:45:50 GMT  
		Size: 18.8 KB (18770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:cli-alpine3.18` - linux; arm variant v7

```console
$ docker pull php@sha256:ab5e2b6f5ed59104e494e1f145b5c60e8409e6f38bc443ef000f931bd7ec5d12
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34563629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e1364ae33d58a521ce1191c231cda71081828c342e4f2f897394b2eb1072be`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Thu, 30 Nov 2023 22:58:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 12 Dec 2023 20:30:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 12 Dec 2023 20:30:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 12 Dec 2023 20:30:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Dec 2023 20:31:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Dec 2023 20:31:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Dec 2023 20:31:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Dec 2023 20:31:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Dec 2023 20:31:01 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 20 Jan 2024 00:11:12 GMT
ENV PHP_VERSION=8.3.2
# Sat, 20 Jan 2024 00:11:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Sat, 20 Jan 2024 00:11:12 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Sat, 20 Jan 2024 00:11:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 20 Jan 2024 00:11:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 20 Jan 2024 00:14:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 20 Jan 2024 00:14:52 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Sat, 20 Jan 2024 00:14:53 GMT
RUN docker-php-ext-enable sodium
# Sat, 20 Jan 2024 00:14:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 20 Jan 2024 00:14:53 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2952d7a17ff3c6e07d09737b9b4aa1666b8a80ce6376de09203883260011487b`  
		Last Modified: Tue, 12 Dec 2023 22:37:12 GMT  
		Size: 2.5 MB (2528496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860b046a1e57ad92d9b8a7b74d56a87953677b5cc11c995d1c7a2f8cf59b70ee`  
		Last Modified: Tue, 12 Dec 2023 22:37:11 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88aeb612e7437063efb5da34b46a1f5b3e345e92aab4681d6a3590d9d35f547`  
		Last Modified: Tue, 12 Dec 2023 22:37:11 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a410f007b0a8ef8d9123efb9f238a2806e43932b9e8a6fd8ec5bed3f7a62c06`  
		Last Modified: Sat, 20 Jan 2024 01:09:11 GMT  
		Size: 12.5 MB (12460697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8ffa2bf52c3ecd4b2bba8a55ce4acc5493d647c6995de50bd2c76692621b71`  
		Last Modified: Sat, 20 Jan 2024 01:09:10 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b17db958f6b1b1b18d288495858272cefe1361acd8164aaff2233a90ca7b82`  
		Last Modified: Sat, 20 Jan 2024 01:09:15 GMT  
		Size: 16.7 MB (16650171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74796f5a6ecbaa361f0ae5602f584f29cc3000f17854d37f7941cc6e4b6daaa1`  
		Last Modified: Sat, 20 Jan 2024 01:09:10 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc895d6df54d33bb05ede1f8a14c9421c2f7143e4ba84d75ab0169bd50836778`  
		Last Modified: Sat, 20 Jan 2024 01:09:10 GMT  
		Size: 18.8 KB (18780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:cli-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull php@sha256:7525f9d892ea6a22a9b2e465344784def5f20148dde50248fac1ee0ba1165125
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37930275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ba4d2c5dbb69f198e9400fb210a0060f2944862010ad1946907451ce1d6b63`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Thu, 30 Nov 2023 23:28:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 12 Dec 2023 20:23:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 12 Dec 2023 20:23:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 12 Dec 2023 20:23:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Dec 2023 20:23:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Dec 2023 20:23:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Dec 2023 20:23:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Dec 2023 20:23:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Dec 2023 20:23:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 19 Jan 2024 23:34:53 GMT
ENV PHP_VERSION=8.3.2
# Fri, 19 Jan 2024 23:34:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Fri, 19 Jan 2024 23:34:53 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Fri, 19 Jan 2024 23:34:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 19 Jan 2024 23:34:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 19 Jan 2024 23:38:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 19 Jan 2024 23:38:39 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 19 Jan 2024 23:38:40 GMT
RUN docker-php-ext-enable sodium
# Fri, 19 Jan 2024 23:38:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Jan 2024 23:38:40 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9493d390846313743a61bb9fd10069c0615ed8474da609a9a62ef2ae3a07d6`  
		Last Modified: Tue, 12 Dec 2023 23:01:30 GMT  
		Size: 2.7 MB (2721137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a094d8333de010a9ce81148984a52cc40090c05dbbf5caf82c5be8a98d8d7f`  
		Last Modified: Tue, 12 Dec 2023 23:01:28 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef6120775a4798753155fc2c5b38706e5d6351f725e1a504527d9ff5db74921`  
		Last Modified: Tue, 12 Dec 2023 23:01:28 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d29ab57bb3fa882e2f1cd25113c3427bb0227c109c7ed8629b8cd5f2b8f021e0`  
		Last Modified: Sat, 20 Jan 2024 00:41:20 GMT  
		Size: 12.5 MB (12460675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cddd5103350dee59ad62a89f3fbc7aa79404531bdba806b69567983b30f446`  
		Last Modified: Sat, 20 Jan 2024 00:41:21 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e513e4b8ce478bb03b8dead6612990c27bd5a9b5a952b17e8f312a3c450f357`  
		Last Modified: Sat, 20 Jan 2024 00:41:22 GMT  
		Size: 19.4 MB (19392213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a152d01cd8c204a909c842f4959cca4fc36278d568bef151b961d8572c53a5`  
		Last Modified: Sat, 20 Jan 2024 00:41:20 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f055ca6b0afc497b3783bd984b086fdbdd9e152fd60fe0b506fd5527062ca464`  
		Last Modified: Sat, 20 Jan 2024 00:41:20 GMT  
		Size: 18.7 KB (18742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:cli-alpine3.18` - linux; 386

```console
$ docker pull php@sha256:5f3b952eb050d45e5d3888c9b98c04f7f7e3817c4ce720c06849f1a31af01775
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35733873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbc6d10628ed9cbb87a6cbf79edc62fce5f2bc2e0029abb451609476c75656d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 05:03:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 05:03:36 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 05:03:37 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 05:03:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 05:03:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 05:03:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 05:03:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 05:03:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 05:03:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 27 Jan 2024 05:03:38 GMT
ENV PHP_VERSION=8.3.2
# Sat, 27 Jan 2024 05:03:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Sat, 27 Jan 2024 05:03:38 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Sat, 27 Jan 2024 05:03:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 05:03:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 05:10:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 05:10:15 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Sat, 27 Jan 2024 05:10:16 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 05:10:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 05:10:16 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d6d2f12df1b19df541851aca59cb3e004d030eea096ff568038497561d6df4`  
		Last Modified: Sat, 27 Jan 2024 06:47:46 GMT  
		Size: 2.7 MB (2727226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7c7b40044db0622103ed0e4a3fa021b8c4579d1677fd27d6e9116d5d8e48c5`  
		Last Modified: Sat, 27 Jan 2024 06:47:45 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0514c3edcfd0f1b5d370eb4eeea4e395ebadba50de6e4f2065e48323f90afaa`  
		Last Modified: Sat, 27 Jan 2024 06:47:45 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b06cd3235d544db24c501d715eb564df11955afeaa6ed4211c89a08047561f`  
		Last Modified: Sat, 27 Jan 2024 06:47:45 GMT  
		Size: 12.5 MB (12460679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e902cc2c78f3afd534c25c6cac539816f582ff87e927caeeff19f42c258560`  
		Last Modified: Sat, 27 Jan 2024 06:47:43 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d6b0fa382a8e441d67664ebe3c944bb0be6d826d1938cb1551c9511c06ba05`  
		Last Modified: Sat, 27 Jan 2024 06:47:48 GMT  
		Size: 17.3 MB (17283502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16e4a7dfcb1a08977d7163b81f44f9907b8a6df45a61fa731db98a34cc35ff0`  
		Last Modified: Sat, 27 Jan 2024 06:47:43 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020416cd7b40f534e9ced54395c9e3b7b1b44bbcc2f91ac7df2b10b7d45f4d97`  
		Last Modified: Sat, 27 Jan 2024 06:47:43 GMT  
		Size: 18.9 KB (18931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:cli-alpine3.18` - linux; ppc64le

```console
$ docker pull php@sha256:98087358b089ffbc58a486aa328dccecd9765eff86f0a0267168af30b9990eb8
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36410752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ee65afd988b0a51b0d8e7f4c271fd5da9e2bf2aa48dbbb774a1f90f5ae845b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:35:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 03:35:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 03:35:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 03:35:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 03:35:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 03:35:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 03:35:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 03:35:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 03:35:21 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 27 Jan 2024 03:35:22 GMT
ENV PHP_VERSION=8.3.2
# Sat, 27 Jan 2024 03:35:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Sat, 27 Jan 2024 03:35:23 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Sat, 27 Jan 2024 03:35:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 03:35:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 03:38:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 03:38:05 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Sat, 27 Jan 2024 03:38:10 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 03:38:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 03:38:11 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a7a89d73e4ee9a28b90eadd129944afbcac67d80107089f98662fe261ca2da`  
		Last Modified: Sat, 27 Jan 2024 04:23:07 GMT  
		Size: 2.8 MB (2768094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73447972e8407c67ac46260eccde3029f8c096a6bcd6ecfa99d54c3b4f02551`  
		Last Modified: Sat, 27 Jan 2024 04:23:05 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af6a1382346f24ae6f048ea13c81e62a254330bb7b5b1baa18f25dc2245ec31`  
		Last Modified: Sat, 27 Jan 2024 04:23:05 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccbe1687bc6f17fbe6fa456ba35ae935e4646fca41a74bfb8c740d2052232944`  
		Last Modified: Sat, 27 Jan 2024 04:23:04 GMT  
		Size: 12.5 MB (12460675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf7cfed65ced7b3eef0e2037e8397bdbd7fa7137400b36cfd1ea0b984460870`  
		Last Modified: Sat, 27 Jan 2024 04:23:03 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c07ac8e353d54d5df691990700090019ec61e82da5cd8344d2b0a9e5a4990fd`  
		Last Modified: Sat, 27 Jan 2024 04:23:07 GMT  
		Size: 17.8 MB (17810304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5650bc8ad987339a817f061ac6890075de45568ff678ebea3b808c48227a2b9c`  
		Last Modified: Sat, 27 Jan 2024 04:23:03 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aec8401e183609e34f58471bc857754019f0d73ca3e067d22aa0025ba12618f`  
		Last Modified: Sat, 27 Jan 2024 04:23:03 GMT  
		Size: 18.7 KB (18727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:cli-alpine3.18` - linux; s390x

```console
$ docker pull php@sha256:ac0d15fe767de3d8a0b42ed2feace4768050bf670a62a5f0dd388b51851a6bad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36711006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ba628af5e7332e0053608bf56072c562284ae0d74caf652e93e59b9eb5bf8b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Thu, 30 Nov 2023 22:45:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 12 Dec 2023 20:07:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 12 Dec 2023 20:07:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 12 Dec 2023 20:07:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Dec 2023 20:07:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Dec 2023 20:07:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Dec 2023 20:07:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Dec 2023 20:07:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Dec 2023 20:07:44 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 20 Jan 2024 00:21:36 GMT
ENV PHP_VERSION=8.3.2
# Sat, 20 Jan 2024 00:21:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Sat, 20 Jan 2024 00:21:36 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Sat, 20 Jan 2024 00:21:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 20 Jan 2024 00:21:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 20 Jan 2024 00:24:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 20 Jan 2024 00:24:34 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Sat, 20 Jan 2024 00:24:35 GMT
RUN docker-php-ext-enable sodium
# Sat, 20 Jan 2024 00:24:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 20 Jan 2024 00:24:35 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9d8a04e5ffd20d63f8efed3950a23dcb2ee8c86112d44078098827cc0a057c`  
		Last Modified: Tue, 12 Dec 2023 22:07:56 GMT  
		Size: 2.8 MB (2792794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc1eecd649c3114a4174ae109f3249b22dd301b21fff70ecf137592a983070c`  
		Last Modified: Tue, 12 Dec 2023 22:07:55 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4c869f81ed8d85aa688c56443814d8b1a0a9691bf3d2e9ce43691b73186c28`  
		Last Modified: Tue, 12 Dec 2023 22:07:55 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a610d2db872c7a260c8ab4702631784b22f3a2fc29cdbb4a68a366b987a41d1`  
		Last Modified: Sat, 20 Jan 2024 01:59:08 GMT  
		Size: 12.5 MB (12460679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726c8595ebb1bd962cf6792cb001aeb227a8a3d9cdf7f600203d95e6d626968b`  
		Last Modified: Sat, 20 Jan 2024 01:59:07 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5934099bd484ffdc39b4f91b799900505cb1b1659f29151768cc8394e08e69`  
		Last Modified: Sat, 20 Jan 2024 01:59:10 GMT  
		Size: 18.2 MB (18216829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf833783dc7a70e4c1afdaa6d0a7fddf9f0c29f8e69b6debf11bf705e5818b03`  
		Last Modified: Sat, 20 Jan 2024 01:59:07 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea80a4e293259c9669e4cfa8d75c5285cb8853e87df98d1d77be1b3c8442bd4d`  
		Last Modified: Sat, 20 Jan 2024 01:59:07 GMT  
		Size: 18.8 KB (18778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
