## `php:7-alpine3.13`

```console
$ docker pull php@sha256:abe37f05b3e40a5bfddd4f41eee6b44ac6b046ff5c19939a52c20a8ed7ae2c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `php:7-alpine3.13` - linux; amd64

```console
$ docker pull php@sha256:c3e6ddddfc8830b94942425c7dbe0a0ad7d53afbfeb741bed807b5b8bb27d871
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29143857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd02f5b6c65d6579890749f0cb9deee1669210a06fc71b5ca3d724938edfcd9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:59:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 14 Apr 2021 23:59:20 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 14 Apr 2021 23:59:22 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 14 Apr 2021 23:59:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 14 Apr 2021 23:59:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 14 Apr 2021 23:59:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Apr 2021 23:59:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Apr 2021 23:59:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Apr 2021 00:39:20 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 15 Apr 2021 00:39:20 GMT
ENV PHP_VERSION=7.4.16
# Thu, 15 Apr 2021 00:39:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Thu, 15 Apr 2021 00:39:20 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Thu, 15 Apr 2021 00:39:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 15 Apr 2021 00:39:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 15 Apr 2021 00:49:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 15 Apr 2021 00:49:53 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 15 Apr 2021 00:49:55 GMT
RUN docker-php-ext-enable sodium
# Thu, 15 Apr 2021 00:49:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Apr 2021 00:49:56 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933cf2f4a68ffb603d67468c6e390ce893a1410ea927dc00e8faabfd01032afa`  
		Last Modified: Thu, 15 Apr 2021 02:15:25 GMT  
		Size: 1.7 MB (1702188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c5cc202a60c205410f5462131556b8ecfba3092bceab1bf75723d1a356c7fb`  
		Last Modified: Thu, 15 Apr 2021 02:15:23 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74403c16157d84037726eebe566275f9e5fdb3f301ce6c101eeb3fb37b8914ef`  
		Last Modified: Thu, 15 Apr 2021 02:15:22 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f951463155805bab7debea596b3d387eb0cd223f5566fb64d1a01c168e834e`  
		Last Modified: Thu, 15 Apr 2021 02:18:21 GMT  
		Size: 10.4 MB (10354090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13703f5b0141c0b9ba3f88976b1bdb8e6c3bcbbeca63e655512556101616b833`  
		Last Modified: Thu, 15 Apr 2021 02:18:20 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef0daa84b76791c04e1f33b306ef8ba9e476dd266a3615ec880114c86c23300`  
		Last Modified: Thu, 15 Apr 2021 02:18:26 GMT  
		Size: 14.3 MB (14253787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63a785ab53e22d1da677c0ad202836e9f4403738bfbd6bd5f76e8a58ad6fdae`  
		Last Modified: Thu, 15 Apr 2021 02:18:20 GMT  
		Size: 2.3 KB (2262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a4dd2c14c09cdad48509137100b894b8218de5ff4f2eb5192bc0501cad0b62`  
		Last Modified: Thu, 15 Apr 2021 02:18:20 GMT  
		Size: 17.5 KB (17538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:7-alpine3.13` - linux; arm variant v6

```console
$ docker pull php@sha256:511578ae371cb331287cd3f479163b54134bd88be5d97f7ef192ea3fe81a9d5b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27933287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:491d0a3b3018c520c77f7da22b2d80f0616b3bedd23a435cc8eac9c3b4161504`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 01:06:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Apr 2021 01:07:05 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Apr 2021 01:07:14 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Apr 2021 01:07:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Apr 2021 01:07:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 15 Apr 2021 01:07:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Apr 2021 01:07:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Apr 2021 01:07:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Apr 2021 01:29:48 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 15 Apr 2021 01:29:48 GMT
ENV PHP_VERSION=7.4.16
# Thu, 15 Apr 2021 01:29:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Thu, 15 Apr 2021 01:29:51 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Thu, 15 Apr 2021 01:29:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 15 Apr 2021 01:29:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 15 Apr 2021 01:33:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 15 Apr 2021 01:33:26 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 15 Apr 2021 01:33:30 GMT
RUN docker-php-ext-enable sodium
# Thu, 15 Apr 2021 01:33:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Apr 2021 01:33:32 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4726cd3e9e578579e631e21133870b656f3938f6a87797a842254b274d8b76e8`  
		Last Modified: Thu, 15 Apr 2021 02:33:02 GMT  
		Size: 1.7 MB (1690998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db188e87a6ea4fd0959949208b039a0d9facc96183df8dc346c6d0d3368b77e`  
		Last Modified: Thu, 15 Apr 2021 02:33:01 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a73dce0ed56811623cd40b786e95b951ce9d6341d9bfefded4f8aa12574283`  
		Last Modified: Thu, 15 Apr 2021 02:33:01 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a754cb0e9edfe6cfa0f12bcc1573c249b7922070719aff9b118aba58769da282`  
		Last Modified: Thu, 15 Apr 2021 02:35:44 GMT  
		Size: 10.4 MB (10354072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e487ebe3f4ada28d0871716afc356557e4cda7d63e7ad84b80cac76c81d605`  
		Last Modified: Thu, 15 Apr 2021 02:35:38 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69815ff11219da10c9e13898b08ea7056899011d613cd832d0c380507c5352f4`  
		Last Modified: Thu, 15 Apr 2021 02:35:49 GMT  
		Size: 13.2 MB (13244268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09007d2e2d613974ff670bcf28ad791de58ecab6f3c8a8a34eadde2d31433013`  
		Last Modified: Thu, 15 Apr 2021 02:35:38 GMT  
		Size: 2.3 KB (2264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cfdadb0dc07df7978292859b78e90f43b27dd2ea570e818b4729955c3a1285`  
		Last Modified: Thu, 15 Apr 2021 02:35:38 GMT  
		Size: 17.5 KB (17537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:7-alpine3.13` - linux; arm variant v7

```console
$ docker pull php@sha256:ecd3efea44ee554d96bc9466c623160f24ccf5986d80f449ae5c8190715a5138
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26765646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9854b992053b6830e5450c9f391c57e27bbcb67777b1bdcf3849776cdc3d937`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 02:08:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Apr 2021 02:08:23 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Apr 2021 02:08:26 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Apr 2021 02:08:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Apr 2021 02:08:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 15 Apr 2021 02:08:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Apr 2021 02:08:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Apr 2021 02:08:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Apr 2021 02:35:41 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 15 Apr 2021 02:35:43 GMT
ENV PHP_VERSION=7.4.16
# Thu, 15 Apr 2021 02:35:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Thu, 15 Apr 2021 02:35:47 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Thu, 15 Apr 2021 02:36:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 15 Apr 2021 02:36:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 15 Apr 2021 02:39:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 15 Apr 2021 02:39:28 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 15 Apr 2021 02:39:35 GMT
RUN docker-php-ext-enable sodium
# Thu, 15 Apr 2021 02:39:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Apr 2021 02:39:38 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bc6d3f07b2e440bf9a8e52a0a5bba0f27637990ee4976424cef6aae97e169f`  
		Last Modified: Thu, 15 Apr 2021 03:38:53 GMT  
		Size: 1.6 MB (1559061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9000ca9dcd92a2066a3a2c4031e677c3998cd82a3ecbc68468d11255ecbdb62`  
		Last Modified: Thu, 15 Apr 2021 03:38:49 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d102949f174ecad1044574e45dded8368eb7451bf66b3bdac6e367c7f415d3`  
		Last Modified: Thu, 15 Apr 2021 03:38:49 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e862f54bc36ab24d87ba865e9006f09f490e2afc055a9dc3da4a872e16c19906`  
		Last Modified: Thu, 15 Apr 2021 03:41:20 GMT  
		Size: 10.4 MB (10354086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a2f653b142a11e16b67bc5eed8e26f7306b6c4c26bf2213006eb4e20846e09`  
		Last Modified: Thu, 15 Apr 2021 03:41:18 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86755320fae7ba0972779779190499f96955d175d2c826d57b0faf4101936c14`  
		Last Modified: Thu, 15 Apr 2021 03:41:22 GMT  
		Size: 12.4 MB (12406522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41cbb4006c0aa0c8db8ced953a8097c2155cc3fd6bb1e256cbb1fb98c60b1ce7`  
		Last Modified: Thu, 15 Apr 2021 03:41:18 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68db0e9d9291bcfd57d52607880016eda34c61b5f56ebb526b2681000fd963d5`  
		Last Modified: Thu, 15 Apr 2021 03:41:20 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:7-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull php@sha256:1e0c457497986cdbf3db8475d4972580d67991badc30d977d1550760c652fcce
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28815475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2df919c680948bd1f0f0c80342d8c50367c506fa3218d4c2c546b51aeed4de`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 00:27:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Apr 2021 00:28:02 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Apr 2021 00:28:11 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Apr 2021 00:28:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Apr 2021 00:28:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 15 Apr 2021 00:28:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Apr 2021 00:28:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Apr 2021 00:28:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Apr 2021 00:53:41 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 15 Apr 2021 00:53:42 GMT
ENV PHP_VERSION=7.4.16
# Thu, 15 Apr 2021 00:53:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Thu, 15 Apr 2021 00:53:45 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Thu, 15 Apr 2021 00:53:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 15 Apr 2021 00:53:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 15 Apr 2021 00:58:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 15 Apr 2021 00:58:38 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 15 Apr 2021 00:58:42 GMT
RUN docker-php-ext-enable sodium
# Thu, 15 Apr 2021 00:58:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Apr 2021 00:58:43 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bea792edc0a65854bc13c90079b9e33a399c351b73e194d9df4f2cf5a0efeb2`  
		Last Modified: Thu, 15 Apr 2021 01:59:52 GMT  
		Size: 1.7 MB (1700262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31bbfcb500579a0c450809a6b082c564c3ce4873732c1b62d8dab52ed0a11ac`  
		Last Modified: Thu, 15 Apr 2021 01:59:50 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22841fe152c1fe4ec2048ebca3b9c0db9d29773b0d0670167a848d87fcfe83f3`  
		Last Modified: Thu, 15 Apr 2021 01:59:51 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b98b38ba2c329c6bfcc177bc90e1236b8fe6031077c00e7d4049ac38c84ca36`  
		Last Modified: Thu, 15 Apr 2021 02:01:30 GMT  
		Size: 10.4 MB (10354094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f905511edb8221d5ae2fbd7dc03bff7e8fa8cb38c4cc9b77d47872ab14ebd00`  
		Last Modified: Thu, 15 Apr 2021 02:01:30 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e65183ed3484daae927f3b4612d6a68886decd1d22725fb7065b056949cfb4`  
		Last Modified: Thu, 15 Apr 2021 02:01:34 GMT  
		Size: 14.0 MB (14027253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584d47f046c33d147576cbff7198e0d202a59156d30c9e908edf486aa6f083d9`  
		Last Modified: Thu, 15 Apr 2021 02:01:31 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0315077c39648df7bf58f090c0f4fbaa8afcfc89a71608e3e753ac10f7931e3f`  
		Last Modified: Thu, 15 Apr 2021 02:01:31 GMT  
		Size: 17.6 KB (17551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:7-alpine3.13` - linux; 386

```console
$ docker pull php@sha256:9cdf3256598c3f1cf65ea5e5f9e18e5fe62c4eb53efef9ceac8941eb2f515895
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.6 MB (29618633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead53363070cf824dcb6fe6eba24ba9c43cc8ce76da8c01365d627b73106d1f4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 31 Mar 2021 17:43:00 GMT
ADD file:245767f958e2b5e6fad41d45d3361849e7c6b2255303e3c785f0f2c86019553a in / 
# Wed, 31 Mar 2021 17:43:00 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 02:49:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 01 Apr 2021 02:49:02 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 01 Apr 2021 02:49:03 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 01 Apr 2021 02:49:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 01 Apr 2021 02:49:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 01 Apr 2021 02:49:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Apr 2021 02:49:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Apr 2021 02:49:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 01 Apr 2021 03:15:31 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 01 Apr 2021 03:15:31 GMT
ENV PHP_VERSION=7.4.16
# Thu, 01 Apr 2021 03:15:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Thu, 01 Apr 2021 03:15:32 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Thu, 01 Apr 2021 03:15:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 01 Apr 2021 03:15:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Apr 2021 03:22:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Apr 2021 03:22:02 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 01 Apr 2021 03:22:04 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Apr 2021 03:22:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Apr 2021 03:22:05 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:b22e590ebf70a9a5901c380b07232ef3c07cb13440402934dfdffb8f8721a949`  
		Last Modified: Wed, 31 Mar 2021 17:44:05 GMT  
		Size: 2.8 MB (2818802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4303b3cd022ad91251e7495aeed4896d9bb7f6fa0dcb18e18234a628ef5cfeec`  
		Last Modified: Thu, 01 Apr 2021 04:41:12 GMT  
		Size: 1.8 MB (1793710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526e185ad2b26faab26d003f328b965c1bbcb1058eae28cb5cb132c7ea7f0c09`  
		Last Modified: Thu, 01 Apr 2021 04:41:11 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e9b82cb292af1dd42fbdda274111233ed643f3515fe3b67e1c212c10f26daa`  
		Last Modified: Thu, 01 Apr 2021 04:41:11 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b36eb2a5730c967902742634417f87e6565eb6623b0f9d4ad6920f9a331be4`  
		Last Modified: Thu, 01 Apr 2021 04:44:34 GMT  
		Size: 10.4 MB (10354070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1866215f4e22f1c527eaa78b5048398800a7f6ae83761d678d2ac9d28594a73f`  
		Last Modified: Thu, 01 Apr 2021 04:44:32 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de52964447f5dee09ae162f698b8aec7cc24c128cc7192579f219d77b5b05e7b`  
		Last Modified: Thu, 01 Apr 2021 04:44:37 GMT  
		Size: 14.6 MB (14630258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82dd6c8e9b5fa5096dbed5adb0ac5e72d7be8418d445d894fb93623216f6ee4`  
		Last Modified: Thu, 01 Apr 2021 04:44:33 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2631eea095f9a398e8e593976afffb3bd5b2d9531c4d77880a205cb7891e75`  
		Last Modified: Thu, 01 Apr 2021 04:44:33 GMT  
		Size: 17.5 KB (17508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:7-alpine3.13` - linux; ppc64le

```console
$ docker pull php@sha256:3301d60ec94f266591624137b67981db5896fbd0a8fa8979e53d4da679fa3f3a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30219149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319ce899aa995a9732865e08a4e0c13f1645a779dc3e5e846f4bf40b662da280`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 14 Apr 2021 19:30:57 GMT
ADD file:52162c4413e3597dad4ccb790c379b67ef40d50c0d0659e8b6c65d833886b3af in / 
# Wed, 14 Apr 2021 19:31:02 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:15:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 14 Apr 2021 20:15:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 14 Apr 2021 20:16:09 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 14 Apr 2021 20:16:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 14 Apr 2021 20:16:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 14 Apr 2021 20:16:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Apr 2021 20:16:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Apr 2021 20:16:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 14 Apr 2021 20:46:01 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Wed, 14 Apr 2021 20:46:08 GMT
ENV PHP_VERSION=7.4.16
# Wed, 14 Apr 2021 20:46:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Wed, 14 Apr 2021 20:46:24 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Wed, 14 Apr 2021 20:46:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 14 Apr 2021 20:46:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 14 Apr 2021 20:51:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 14 Apr 2021 20:51:48 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Wed, 14 Apr 2021 20:52:02 GMT
RUN docker-php-ext-enable sodium
# Wed, 14 Apr 2021 20:52:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 14 Apr 2021 20:52:16 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:771d2590aa602a0d4a922e322f02b22cc9d193f8cd159d9d1a140cadf1f8b4d4`  
		Last Modified: Wed, 14 Apr 2021 19:32:33 GMT  
		Size: 2.8 MB (2813141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18b4999d98214ab55ea75ff5caca694bebb5bb07f5c23e9a6f4ce900ce4c2c6`  
		Last Modified: Wed, 14 Apr 2021 22:01:00 GMT  
		Size: 1.7 MB (1748637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8118faf424e03fa2a7d0df76aa1813928f5598c3bdd1b390629452fd95766a66`  
		Last Modified: Wed, 14 Apr 2021 22:00:59 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc86fc5a1b429a1fd2c88a0a1f7506b2543ae32ff0ba83f0ba697a84dafa2ded`  
		Last Modified: Wed, 14 Apr 2021 22:00:59 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f21aacaa107d3d98050c77019e280e560d4e0dfe2a51858005777f9efec025`  
		Last Modified: Wed, 14 Apr 2021 22:03:22 GMT  
		Size: 10.4 MB (10354081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e95142baa591b8e88ccd558867dd5bef0bc391dbe0649c7dceafa84b5b3d110`  
		Last Modified: Wed, 14 Apr 2021 22:03:21 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4385af26fd4dee701f7198dbdd8fd4dd3f392b7c1be79ce10fddf3fe874c1f1a`  
		Last Modified: Wed, 14 Apr 2021 22:03:26 GMT  
		Size: 15.3 MB (15281444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f7e4a02b3e44c7cdcc57f117762d89dcc91b125a4bb3af1faf064e2c640e42`  
		Last Modified: Wed, 14 Apr 2021 22:03:21 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd3a493c4a32951756304eea6ef4b7261132f3f184e441bbb274c600f8112c9`  
		Last Modified: Wed, 14 Apr 2021 22:03:21 GMT  
		Size: 17.6 KB (17557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:7-alpine3.13` - linux; s390x

```console
$ docker pull php@sha256:55aab42f9cbee6f5309cd32bd690eb4dd9822e096d24a6a434083e4793b59393
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28352540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ebf00873b1e6f457991e640068a6b61211d1b3e8b6ea96f1baff9d2b87177c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:00:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 14 Apr 2021 19:00:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 14 Apr 2021 19:00:56 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 14 Apr 2021 19:00:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 14 Apr 2021 19:00:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 14 Apr 2021 19:00:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Apr 2021 19:00:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Apr 2021 19:00:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 14 Apr 2021 19:18:59 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Wed, 14 Apr 2021 19:18:59 GMT
ENV PHP_VERSION=7.4.16
# Wed, 14 Apr 2021 19:18:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Wed, 14 Apr 2021 19:18:59 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Wed, 14 Apr 2021 19:19:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 14 Apr 2021 19:19:05 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 14 Apr 2021 19:22:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 14 Apr 2021 19:22:49 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Wed, 14 Apr 2021 19:22:50 GMT
RUN docker-php-ext-enable sodium
# Wed, 14 Apr 2021 19:22:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 14 Apr 2021 19:22:51 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d300c94e92b07eb0727117362a4c02c33a3af45a2c84e27e191b18fd64537ff2`  
		Last Modified: Wed, 14 Apr 2021 20:01:05 GMT  
		Size: 1.8 MB (1760701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c222b785aeace308f4ae843bd963ab89b5e43b40c39e44819a79a97ab65ffd`  
		Last Modified: Wed, 14 Apr 2021 20:01:04 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdca579f326f21cb64727b7a043ef139e61e18d78e009c7aaa0d00c8787d500`  
		Last Modified: Wed, 14 Apr 2021 20:01:04 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e023ade7aa7ae24c1ec05780b87d8bcbdbae8af6981f8c45a965aead4c3ddeb`  
		Last Modified: Wed, 14 Apr 2021 20:02:48 GMT  
		Size: 10.4 MB (10354073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e078ca74127104e79e4fcb8a4214f5c9489346f68bfbcab9fe57b4b5e9f102fe`  
		Last Modified: Wed, 14 Apr 2021 20:02:47 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528db2db38d3e75f7c279f3656746050864a7ecc657fe418cf25a476410b95c6`  
		Last Modified: Wed, 14 Apr 2021 20:02:50 GMT  
		Size: 13.6 MB (13613281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d55068cc4639d221add2bcad14e1d7107444349b31ed5aa1a6d63edcdb6de6f`  
		Last Modified: Wed, 14 Apr 2021 20:02:48 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a02562b9902cd402500ba105146fdfb050144ec4a531871c87607dca13ce102`  
		Last Modified: Wed, 14 Apr 2021 20:02:47 GMT  
		Size: 17.5 KB (17544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
