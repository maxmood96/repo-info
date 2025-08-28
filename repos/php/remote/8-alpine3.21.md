## `php:8-alpine3.21`

```console
$ docker pull php@sha256:6e45a851eecd01f61c60af34003e2c658207add9344087f5053dc2eb0bc70be4
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

### `php:8-alpine3.21` - linux; amd64

```console
$ docker pull php@sha256:61f2fb5dc0b78a4582014286aae0152b1a5b48b87e9d5f5dcaf4f842b6f1167c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41642389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc94db7dee50bb05cfc07bc6c0f0f556923598f52050429d3bb80e00568245b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773412d55816fbb8f2d20d06eacea508867b69c0dce13fa9c26b23980d722888`  
		Last Modified: Thu, 28 Aug 2025 18:24:00 GMT  
		Size: 3.3 MB (3328764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fdddfcf0f797f96cc9c15b393affb93220afcccd9672a1128c7ae0fa8d5766`  
		Last Modified: Thu, 28 Aug 2025 18:24:08 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d398c7e2bb610a63111429489d0ba2d478acfd11245ede4e06306c16f004b3`  
		Last Modified: Thu, 28 Aug 2025 18:24:13 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28b9077a76f0dcabae65b22191544ca0cc65bd84fb7e5708750fa72efa2a971`  
		Last Modified: Thu, 28 Aug 2025 19:22:54 GMT  
		Size: 13.7 MB (13657722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526accd86cfc104eac67074f88967eea797b498b0a20e69fd55fd262a5f28220`  
		Last Modified: Thu, 28 Aug 2025 18:24:16 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e301ce44d31d04feda386b28d2457d2748f2477ba992efc7dafb9032b5e6c44c`  
		Last Modified: Thu, 28 Aug 2025 19:22:59 GMT  
		Size: 21.0 MB (20974655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c8a51412957b48442d9e6aa7bd565b40e16750335521ec048beb7f2989b609`  
		Last Modified: Thu, 28 Aug 2025 18:24:19 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ccb7fed50a019cee95648d096b8c94159847ece436051869683dd708e975fa`  
		Last Modified: Thu, 28 Aug 2025 18:24:23 GMT  
		Size: 19.8 KB (19801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11550691701d57ead6a780ac38a93a8c7203d4ba48c39fb8c2c4ae29f55a32a5`  
		Last Modified: Thu, 28 Aug 2025 18:24:27 GMT  
		Size: 19.8 KB (19791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:ae7f7e59abfdd2a0f152c1a66b011c30ddc1b26a90a746a2eb5b4465c2f2083c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 KB (316544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9231121d40ae2ff7612e9280f2a772ad0766995bbf05336e6922205e2ba4a6d`

```dockerfile
```

-	Layers:
	-	`sha256:c330ec7e27d39fab446993b52e190d0b4b7ccd4b438218d2f8d98341cdae2195`  
		Last Modified: Thu, 28 Aug 2025 19:55:21 GMT  
		Size: 275.9 KB (275851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2db07471ebbf1d5fe7e4b237884f520dea74f368b66461947c0f28180b28fce`  
		Last Modified: Thu, 28 Aug 2025 19:55:21 GMT  
		Size: 40.7 KB (40693 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-alpine3.21` - linux; arm variant v6

```console
$ docker pull php@sha256:c0b2c1cc8be8fd1d224c1e66eac497a2a4200d85a2607ea746a575b67921c249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39445892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc503e6b26fd3b9085a8d45ff0a2a0ed840281b9968ab15fbee43375165e7de`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:ca0c331561564c536ffa9246944bb50ac21d3fb11fe66c38baad97fdd1f05719`  
		Last Modified: Tue, 15 Jul 2025 18:59:41 GMT  
		Size: 3.4 MB (3363814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec35a56991ada71124e00946112bed14ce95845daf607b4301261898bcae3ce`  
		Last Modified: Tue, 15 Jul 2025 20:15:13 GMT  
		Size: 3.3 MB (3297360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0589c789d2c41f5f9ab323c40f888a098fabfe10d0c446429602aeb36c9bea0`  
		Last Modified: Tue, 15 Jul 2025 20:15:12 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab23b9a12cab48afc01d4443f5759dc52e7acb5d1203abc401c161268ed3227b`  
		Last Modified: Tue, 15 Jul 2025 20:15:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165351a1fb6954783076c8f5be0d0171af6b4646a93344af4b8d1019a19ebfb2`  
		Last Modified: Thu, 28 Aug 2025 18:34:03 GMT  
		Size: 13.7 MB (13657736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7487a0302abe72adef685889e982474ef397538aa9441beb7089b1074f4ee0e1`  
		Last Modified: Thu, 28 Aug 2025 18:34:01 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aca061c5bcf143afeb855e6addc709851607a14e9e23a3f17fd42afd498ab9a`  
		Last Modified: Thu, 28 Aug 2025 18:34:03 GMT  
		Size: 19.1 MB (19083665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897cbca0367b864d5ca19a2a8cbb7948eb895e3a05448bb982fcfb5980dd6596`  
		Last Modified: Thu, 28 Aug 2025 18:34:02 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8d863c03d197806cf6d5ca14d9e7d9eb402b5f35a1f757a8e011a2bf083b1b`  
		Last Modified: Thu, 28 Aug 2025 18:34:01 GMT  
		Size: 19.6 KB (19608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c15fcb5d76e46bc49370ef2e4aad9064129a434ffda575ad87ab2b34e4fb9b8`  
		Last Modified: Thu, 28 Aug 2025 18:34:02 GMT  
		Size: 19.6 KB (19610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:fc3fb7e5c607882e663eb3c0e9b5ad9a2dffe101a20e607ef4ee1a6ffd6f17db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 KB (40665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb03c96f661812f4eed2291fea131b47f4a5b397afd4f3a6ceef36debf8eb27f`

```dockerfile
```

-	Layers:
	-	`sha256:29d2471f7735b8f936ffbc3eb1f2f1d2967961b825f35e6b87450aca282889fa`  
		Last Modified: Thu, 28 Aug 2025 19:55:25 GMT  
		Size: 40.7 KB (40665 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-alpine3.21` - linux; arm variant v7

```console
$ docker pull php@sha256:c16cc9ab26732dc03d36c461c1213973360b73e5766a9cf5992164d1a31d66f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (37973974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52372e7b2dc4a32d03ffc601f9e7f3f5cf475cb20af93d80a60ba22211a04f12`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 01 Aug 2025 00:46:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 01 Aug 2025 00:46:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 01 Aug 2025 00:46:35 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_VERSION=8.4.11
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 01 Aug 2025 00:46:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 01 Aug 2025 00:46:35 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:a96f521d793eec1dcb2b825985eb01c309edb500ebd753a2f84cb9430f05802f`  
		Last Modified: Tue, 15 Jul 2025 18:59:46 GMT  
		Size: 3.1 MB (3096871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d20bbf26d2027b5f0292bde8b26a6a24bb47b84b46ab9bbf4ee24a6dcb444d`  
		Last Modified: Tue, 15 Jul 2025 19:54:12 GMT  
		Size: 3.1 MB (3106247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae312659bef4955822c42ab6a0de35b734a568087a4930af34215200d5096f0`  
		Last Modified: Tue, 15 Jul 2025 19:54:10 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69098bb098b25ef97de74c5525dc745e334842258b56814035d483f5302b91a`  
		Last Modified: Tue, 15 Jul 2025 19:54:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ea43d458380d991db6ca4d7156fe420e4ce0aa3ec4399889e295cde8aa6b0c`  
		Last Modified: Mon, 04 Aug 2025 23:23:28 GMT  
		Size: 13.7 MB (13653275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0d6eb33998b80f5624e7362a00ad4fc010867a5be582034c4557ae7b51b77a`  
		Last Modified: Mon, 04 Aug 2025 23:23:25 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa2b1cd9cf0d0be6e2172a42103c42f6de51c675e7e98bdf7c49d333d17d7d7`  
		Last Modified: Mon, 04 Aug 2025 23:23:30 GMT  
		Size: 18.1 MB (18074260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7514722dfeaef6fb93611d647a8f4d35773161d99c8c5c19a5f6bbe64947b6f4`  
		Last Modified: Mon, 04 Aug 2025 23:23:25 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de99f3e7033fb7d3f2ebb46d264c8751ddabba5116c7e7328cd781a58f23222`  
		Last Modified: Mon, 04 Aug 2025 23:23:26 GMT  
		Size: 19.6 KB (19615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a702fc09e48725f01e2ba427b46ee4de6710a020abe6a9078648ee2a8060cce2`  
		Last Modified: Mon, 04 Aug 2025 23:23:25 GMT  
		Size: 19.6 KB (19607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:01f5d8057d8a425d4447359b4a194e1b0c3bbc429ee461a97a392aaa2134f1d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.8 KB (313809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecb39704b3650b7bcc87aec231771283465df5d282631335f70fdd6fbdde3b8`

```dockerfile
```

-	Layers:
	-	`sha256:d42ddd1e27d8c5e31827852f6ab909d326343a7bf6d1c24d3e4c24b85700a97c`  
		Last Modified: Tue, 05 Aug 2025 01:54:46 GMT  
		Size: 272.9 KB (272929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ecd241aa7a9b085455d3d0a990e312a8969d3eaaa550f15d992c824107c7123`  
		Last Modified: Tue, 05 Aug 2025 01:54:47 GMT  
		Size: 40.9 KB (40880 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull php@sha256:1b92dd472c54347e1c13969e4fcaf8524734a0417ac08f5d92f150842a181a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41530046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e02ef9ebf9e9bb602469d34452edc3c51857ae5289880b596004c6d0aba2c7c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ca320762826ec9e7f6d77e262f7bcd16a67a48feca8f7f16463c72715df6c7`  
		Last Modified: Thu, 14 Aug 2025 23:03:32 GMT  
		Size: 3.3 MB (3322217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3d10164fc67ff34c9aed070e424747db24b7c991786233a6e8cc11455b097f`  
		Last Modified: Thu, 14 Aug 2025 23:03:32 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4721a9a5540665e28259446bd86a9cd4402fa0c33dee73fd7f89a8edfe65f`  
		Last Modified: Thu, 14 Aug 2025 23:03:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf22e55153f0cdea08fa3feb7b70fb876b5af155ec0a1e362ea902f06a92f753`  
		Last Modified: Thu, 28 Aug 2025 18:58:34 GMT  
		Size: 13.7 MB (13657728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2789dd177d51641b622467d0172647562d005d09f5e3d0a8b881a0771a97a9fd`  
		Last Modified: Thu, 28 Aug 2025 18:58:33 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25c40f96bada538c37272e00487bdaecfba6804ce388adbe9d2ef40c36227a5`  
		Last Modified: Thu, 28 Aug 2025 18:58:36 GMT  
		Size: 20.5 MB (20519863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592f6a4bf983fb0a404243a0a7fad65e73261d2d8a5eb63a9bafad034f79add3`  
		Last Modified: Thu, 28 Aug 2025 18:58:33 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b98443add80860ded4d603d875cc766991eb5a1d889e5542944656bacbc9cc9`  
		Last Modified: Thu, 28 Aug 2025 18:58:33 GMT  
		Size: 19.6 KB (19610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49f3bf9f5846733c3e2dce6909a9f7731e0daa63765bf65e422e84deed7c058`  
		Last Modified: Thu, 28 Aug 2025 18:58:33 GMT  
		Size: 19.6 KB (19597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:9ffb33364c187138f3ca425fa0d67713efae4eeb5c58cc2d595a0a6fd564016c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.9 KB (313900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd383bbc714bec7cb954387d1740c4d0505ff8d79a85c0d087830da11c22850`

```dockerfile
```

-	Layers:
	-	`sha256:fb3c741b44f8dd594ccab96246ec4ed7f91390f6baa116856e0453c45b1157dc`  
		Last Modified: Thu, 28 Aug 2025 19:55:32 GMT  
		Size: 273.0 KB (272965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da6dafe96371072918215c485a5969120bffacc7c954bc374ceeb3aaa88a216d`  
		Last Modified: Thu, 28 Aug 2025 19:55:33 GMT  
		Size: 40.9 KB (40935 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-alpine3.21` - linux; 386

```console
$ docker pull php@sha256:d9f797a15ff5461778c984606db6c0391d9a237a3490b1b39fe337216b2bc0b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42033390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1f70617cffa8efb93ea9e153dbb9c6561a0f53d28d5347000dc7ca64a38549`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:47ad0adcb4aa253584437783c542bfbd2276c07a7a0b7487bb26f9b2e80cba73`  
		Last Modified: Tue, 15 Jul 2025 19:04:30 GMT  
		Size: 3.5 MB (3460726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4455f46299efaef74d01981cdc126cb8ea71528e2e7bf0f65f7e09e44b3dad`  
		Last Modified: Thu, 28 Aug 2025 18:21:06 GMT  
		Size: 3.4 MB (3370606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a270e8d3f69567a6a490bc393beee5cbb130641198d2684be3e6716f62ca0e`  
		Last Modified: Thu, 28 Aug 2025 18:21:06 GMT  
		Size: 937.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b20c38939e5d817bbc05a37abe0008d7b1a37b53bc8c8f1d993b515a421de45`  
		Last Modified: Thu, 28 Aug 2025 18:21:06 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030113dae48c58443a9546eeafb331b3368df8e5ee06cdef27bd3b1f91c844ca`  
		Last Modified: Thu, 28 Aug 2025 18:21:08 GMT  
		Size: 13.7 MB (13657730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8e64316cea1f1b2cff6c26300235710827e2e93bad94ed73bebb2260689962`  
		Last Modified: Thu, 28 Aug 2025 18:21:06 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c682a10e8fadcd5acb8416f5d4ba01652b007e733fa8302bd17136c914150265`  
		Last Modified: Thu, 28 Aug 2025 18:21:09 GMT  
		Size: 21.5 MB (21500668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b212bfdd14c58c8c2cb0ae86102c76e73698891ba8abc287769d89a61c654e`  
		Last Modified: Thu, 28 Aug 2025 18:21:07 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d0072e9625e6ebfbadf163774770d9f786610deb2356eb9c7a1dfdb3e8b292`  
		Last Modified: Thu, 28 Aug 2025 18:21:07 GMT  
		Size: 19.8 KB (19790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd494af304d7bba64841651ad2806804aa5809afea9154cad9d8c9236afbffcc`  
		Last Modified: Thu, 28 Aug 2025 18:21:07 GMT  
		Size: 19.8 KB (19783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:3aa39a5336885e1e07b806a0ab90aef06496436c8b304a4af26ea1b2c1495d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.4 KB (316436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bacb2aaedfd2831e1cbaef31f2fac20ea8472952fa078a1de8b529e122375cd7`

```dockerfile
```

-	Layers:
	-	`sha256:e94e0aea190f2f7c5d96da15d4908f34f627029abb22aed2c35ecc572c5fe490`  
		Last Modified: Thu, 28 Aug 2025 19:55:36 GMT  
		Size: 275.8 KB (275806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e841b77eceda32bacef79c68bc99f8f1a1c48f48f17a79fef261fb53ee3e43b`  
		Last Modified: Thu, 28 Aug 2025 19:55:37 GMT  
		Size: 40.6 KB (40630 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-alpine3.21` - linux; ppc64le

```console
$ docker pull php@sha256:47feab912237f739a960bf268b5ecfdf260ae26c65a16f965f4cd0360ad1e3bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42610932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f025d4c28d1773eb75753fb17a578ed5bedc0cefcb12ce292a12d7987e435c5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 01 Aug 2025 00:46:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 01 Aug 2025 00:46:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 01 Aug 2025 00:46:35 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_VERSION=8.4.11
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 01 Aug 2025 00:46:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 01 Aug 2025 00:46:35 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de92cb3012c70fdf6ce461e128bebfb28a323ac3e5a165dc24ac1ce93d4b727c`  
		Last Modified: Tue, 05 Aug 2025 00:36:41 GMT  
		Size: 3.5 MB (3472430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252a87919232aed28dbad1c92709dd0a7493804ee5e94ded58dc208829754002`  
		Last Modified: Tue, 05 Aug 2025 00:36:46 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc160638f2a3efd31bf6869b3b8b1bd9e4a6e5fd28ed31ca0a6cea542e55fc5`  
		Last Modified: Tue, 05 Aug 2025 00:18:25 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c306637c8bd38241fb4be3a47cd8b3f5427ff50adf7dd863b4f994f9a67b1290`  
		Last Modified: Tue, 05 Aug 2025 00:57:49 GMT  
		Size: 13.7 MB (13653271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1b2c10d4473564e5001147b598963410cc4b035d4dc4061adc1770796d4eef`  
		Last Modified: Tue, 05 Aug 2025 00:57:47 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587ad9a8ee5c71eac1bde6f0023153ab42ed3079a1ab3ae85936831cf0efae2a`  
		Last Modified: Tue, 05 Aug 2025 00:57:52 GMT  
		Size: 21.9 MB (21872808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260d8649ebe3a4c0b245fc37b3663531288b3974b1a79ff5992016143086ca10`  
		Last Modified: Tue, 05 Aug 2025 00:57:49 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab72ab87514c68ccb9a4b176f5c1a0d634793f899a574da070a2aa38bebf7c59`  
		Last Modified: Tue, 05 Aug 2025 00:57:48 GMT  
		Size: 19.6 KB (19605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c199db57624a04b43591ab79757d574e5cb009dbf3fb1e30cbe61fcda125b32d`  
		Last Modified: Tue, 05 Aug 2025 00:57:49 GMT  
		Size: 19.6 KB (19601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:1a2ca82790b2a69bbb67edca9b76421cde3548b4526510deef94489245898826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.7 KB (311742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7083caed355de0018db274d6e6fd1056463722e0f0f0b415f131cbdd2ee0bcf`

```dockerfile
```

-	Layers:
	-	`sha256:cff3709086335299b53e86fe9befdf0f2e7301c011b2f4b455ee08251ac50a3a`  
		Last Modified: Tue, 05 Aug 2025 01:54:55 GMT  
		Size: 271.0 KB (270968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a4b554a09fc95484cbd9d2291e914a58e6c77711ff0bf837c2fbd72ca035ece`  
		Last Modified: Tue, 05 Aug 2025 01:54:56 GMT  
		Size: 40.8 KB (40774 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-alpine3.21` - linux; riscv64

```console
$ docker pull php@sha256:4049a3d8e24a6a8ecf959c40bf550817a3dd15ecf4bdb42ddd5f2c9619f0355e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40881399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbcb1f958b20489862313dfb738a575ac6cd9345fdb789ce3219a2ad09d5f5a3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 01 Aug 2025 00:46:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 01 Aug 2025 00:46:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 01 Aug 2025 00:46:35 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_VERSION=8.4.11
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 01 Aug 2025 00:46:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 01 Aug 2025 00:46:35 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e5eec9dd173ff9193682a9fef67e972e885c383fb2d4f42544d9772fc751a4`  
		Last Modified: Wed, 16 Jul 2025 06:10:41 GMT  
		Size: 3.5 MB (3452475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cceaa2d271017b75db0cc25a0f8b5f9133ba78f235382feff3a9cc104559bb3`  
		Last Modified: Wed, 16 Jul 2025 06:10:41 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38602048154ac723fa1cd82779b4002e1e756b92f09b7e1eb1373e66b27ce411`  
		Last Modified: Wed, 16 Jul 2025 06:10:40 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39edea33f71b063eec7dc6b0c540dcf901fd464c15446385be196a3b8776c4b4`  
		Last Modified: Tue, 05 Aug 2025 10:02:50 GMT  
		Size: 13.7 MB (13653266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b3d74ee10f68bd0b6a53839e25c500b6d57389b108ea3d54f89abe4d57e8ba`  
		Last Modified: Tue, 05 Aug 2025 10:02:49 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332761ad649f4a710b0ff01dc8b67acbe81d95aa1062b118b33136cb98fc973b`  
		Last Modified: Tue, 05 Aug 2025 10:02:51 GMT  
		Size: 20.4 MB (20383292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3d41c90703adaa4182ec851e613b26be8783f4261ce66c9dc1d70a466c571b`  
		Last Modified: Tue, 05 Aug 2025 10:02:49 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed729cae6dc370cce090aad2f9198dc994789d287d7936a33f310b5678f47d8`  
		Last Modified: Tue, 05 Aug 2025 10:02:49 GMT  
		Size: 19.6 KB (19591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548e8149a75cd9a6d9b0d4fa5eaa046021d37e58c5636ff85a116248489bbabe`  
		Last Modified: Tue, 05 Aug 2025 10:02:48 GMT  
		Size: 19.6 KB (19583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:6a771f97935ba8b1467a01d36894c5746922defb9899f02ffa9350f3a09e9ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.7 KB (311738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f919c1657ad9cd192f28ebc21bccfcd1418c87280171742eaf86a38b8b6f60`

```dockerfile
```

-	Layers:
	-	`sha256:c409c3942a68a5b6c19c493452dae15757745e2ebb52c5be94252324ffb8f829`  
		Last Modified: Tue, 05 Aug 2025 10:54:38 GMT  
		Size: 271.0 KB (270964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f71d970aaa5a8ed3fc0972e3c717d69534bdb39541a12d5fbfd80d7bce3da0b`  
		Last Modified: Tue, 05 Aug 2025 10:54:39 GMT  
		Size: 40.8 KB (40774 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-alpine3.21` - linux; s390x

```console
$ docker pull php@sha256:88225526cd9e0e6be741559292878df326d6319eedf5534db248a7a23d5fe14f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42155955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91c7264ee065432f6d62103b1bfeabc44ba23bdb94a45d60fc5142442c038a0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 01 Aug 2025 00:46:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 01 Aug 2025 00:46:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 01 Aug 2025 00:46:35 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_VERSION=8.4.11
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 01 Aug 2025 00:46:35 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 01 Aug 2025 00:46:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 01 Aug 2025 00:46:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 01 Aug 2025 00:46:35 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c5c36be40cbd9f961103607cfeb4a27fca1247bf32c68ff6c3faa713bf7bb1`  
		Last Modified: Mon, 04 Aug 2025 22:32:33 GMT  
		Size: 3.6 MB (3558701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27269eed04dd727444fd91a3f824269c713ad3dbe7d3d1757b644a946d26a012`  
		Last Modified: Mon, 04 Aug 2025 22:32:33 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff5836572d7f96c46226cf728d11ee75e566f34cd9c4d55f9e4d15f01e0bf23`  
		Last Modified: Mon, 04 Aug 2025 22:32:33 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98927186b53341a7f5bc13bbe414b87a491ec5dff9426a6c48430831233f45d`  
		Last Modified: Mon, 04 Aug 2025 23:11:15 GMT  
		Size: 13.7 MB (13653279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a63c4a8c571a2ab890e2b8b03c7c54663e33c536ac12b8aa2343e59d1d43e88`  
		Last Modified: Mon, 04 Aug 2025 23:11:12 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa83211cca3c0feb6a6f867244e8e39c87f95b6c9dba5b952ad5c38463c77091`  
		Last Modified: Mon, 04 Aug 2025 23:11:14 GMT  
		Size: 21.4 MB (21438574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd845a8d0320acb6ee7e8d58a2035f98009541cb7c9940ce02d53cd8ef2718e`  
		Last Modified: Mon, 04 Aug 2025 23:11:12 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c67903fb056f181cea01371b03c08bee2396244bf3354c17c495fdd32129f94`  
		Last Modified: Mon, 04 Aug 2025 23:11:12 GMT  
		Size: 19.6 KB (19602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f00e02f7f5587bd698733d585bc6e024b853f21c8808f1ca581ff6d5af9297f`  
		Last Modified: Mon, 04 Aug 2025 23:11:12 GMT  
		Size: 19.6 KB (19604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:f1d7e68b41549da8ea07f0d4ef871dc5eb29a62edb9a05933189e3ed2c476214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.6 KB (311604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373dc5df7154512e13fe4bd0c58034878dd5279946f083f5d28370faf1a9d284`

```dockerfile
```

-	Layers:
	-	`sha256:4e235df5a9f27267aa4026d30253fcc92a139318e09fded937a50186ae86303d`  
		Last Modified: Tue, 05 Aug 2025 01:55:01 GMT  
		Size: 270.9 KB (270910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9e6b00bc785806ddc2b368bb6716cf0009248819ef0bbfbe134ac5167898319`  
		Last Modified: Tue, 05 Aug 2025 01:55:02 GMT  
		Size: 40.7 KB (40694 bytes)  
		MIME: application/vnd.in-toto+json
