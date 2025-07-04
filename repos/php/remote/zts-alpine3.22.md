## `php:zts-alpine3.22`

```console
$ docker pull php@sha256:8c2f6c87a94450cc9d38601bf70ec94cbebe5d1731cff5da0ba5e11ca2d18115
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

### `php:zts-alpine3.22` - linux; amd64

```console
$ docker pull php@sha256:5c92eba30399fa67b06d447278ccfee9a2fe01d2ef1470b37b2c3e6c15984b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49881495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b066a32e7148f24a43f8662975f2bbb63306d87ae76d4eaa7fec5cd0f480aa56`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Jul 2025 14:40:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Jul 2025 14:40:24 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_VERSION=8.4.10
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Jul 2025 14:40:24 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0358e78c9ce59e2c9fe3930240a62e27da7a705f21a6e1d21a9f530d133dade`  
		Last Modified: Thu, 03 Jul 2025 23:04:39 GMT  
		Size: 5.9 MB (5944409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03425d2a9ad60e561033df0dcd351588441ec744e657d7fe3074c8f467e4c032`  
		Last Modified: Thu, 03 Jul 2025 23:04:38 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cd889674d7d0421533643dc5d4254e3ae6138d84a34f32d32332e78ae853f9`  
		Last Modified: Thu, 03 Jul 2025 23:04:38 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ab5e966ec2f9e1959ecb2a659b81a18a46b980b0b5f35fea37d0295f886e13`  
		Last Modified: Thu, 03 Jul 2025 23:04:39 GMT  
		Size: 13.6 MB (13647268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257c3c13917903279dd55d701e8556f61e377420b3e03a53fcf301834b83185c`  
		Last Modified: Thu, 03 Jul 2025 23:04:38 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c909e8afd90fe6868c5c136022c0e9c1b8ce247a7a974910139fe8968d06a930`  
		Last Modified: Thu, 03 Jul 2025 23:04:41 GMT  
		Size: 26.4 MB (26448472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a3d2cfbadd794adabcbc55e75df2ae68e335ed37077e48cda3835868933e10`  
		Last Modified: Thu, 03 Jul 2025 23:04:38 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a75cbd9e94028a50fb63ebf0941d649a48448872d0f62d61bda251c988b769`  
		Last Modified: Thu, 03 Jul 2025 23:04:38 GMT  
		Size: 20.2 KB (20209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a974e888bc0669dcdee220b9afe901ef4a2b47ecb718bd2882bf7a5168f97a`  
		Last Modified: Thu, 03 Jul 2025 23:04:38 GMT  
		Size: 20.2 KB (20205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:9008dbb8b99a0c490ebd905054480a637da922ba179678ef92260f2286aec92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 KB (323993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebdf596306beaf8934dd1ec4d66c52d723facecd1c9a88c04603a4c108fa32c1`

```dockerfile
```

-	Layers:
	-	`sha256:03d9f4071a83fe43c1641af57ac7bce8d8fceb3e03bc15128d415506505d896f`  
		Last Modified: Fri, 04 Jul 2025 01:59:38 GMT  
		Size: 282.5 KB (282489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea07f438a7ed45f3d9624c22af6a9c81b91ec7a392439b6643ff87acf398c457`  
		Last Modified: Fri, 04 Jul 2025 01:59:39 GMT  
		Size: 41.5 KB (41504 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine3.22` - linux; arm variant v6

```console
$ docker pull php@sha256:e94341ac17c43a2170d9c152c93d30fda3adbb25502b7871d4315466e6d2132b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48076524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a873bc494c5328537786b061c0b34ba86fc9bb23641b39f49b991f7b5454abc8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Jul 2025 14:40:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Jul 2025 14:40:24 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_VERSION=8.4.10
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Jul 2025 14:40:24 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4a1a48d371204daac6d50cf0ade3fcbe953b7326556c347d0834eeb808b22f`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 13.6 MB (13647232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7209fb73f851518e0fbc85b54004a573116286207c48ee96ab37833cb8ea1353`  
		Last Modified: Thu, 03 Jul 2025 23:00:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a5bd7160dfe22501a35022ef829d10e6f8b6ce50ec212f861637c21f92db2e`  
		Last Modified: Thu, 03 Jul 2025 23:12:05 GMT  
		Size: 27.5 MB (27451812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378523e4aa42f942603fbb85c28db20bed2d1dbaf200c35445e5bc1243997f0b`  
		Last Modified: Thu, 03 Jul 2025 23:12:04 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61b04f31b51aae6590120956be591418ac8eb0226dc36184f6e03ebc03fc7bb`  
		Last Modified: Thu, 03 Jul 2025 23:12:04 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e402901f996141e6587ce05e0736e761e0f883398fa7a90f145eda394e1c7d`  
		Last Modified: Thu, 03 Jul 2025 23:12:04 GMT  
		Size: 20.0 KB (19993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:47f0c5b451a764adf0594777c45f144b59f15df5bd55dc07ebcff9e80a0268cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 KB (41475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e02d51492af3fdcd43b0f66b84635d2a1d698865aee0048182ecebde87cca3`

```dockerfile
```

-	Layers:
	-	`sha256:b4e1bb83be368981da15d34279f9f7fe7586d08529898412b2cb988460ba84b2`  
		Last Modified: Fri, 04 Jul 2025 01:59:42 GMT  
		Size: 41.5 KB (41475 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine3.22` - linux; arm variant v7

```console
$ docker pull php@sha256:416272c15e4ceb7e92b5bb3a26b3a7ec783a436b904f8ec344ab42c09b9981cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46057196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4b4ab8bfd4523b44a5be67dde15dd793af0e5d409a039310fc58aadf38139d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Jul 2025 14:40:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Jul 2025 14:40:24 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_VERSION=8.4.10
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Jul 2025 14:40:24 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f4b8d7b2257f1a6ac3d6d3cc6bf9a4b64ab9fc5d2607c301f7de2c7d6c4f46`  
		Last Modified: Thu, 03 Jul 2025 23:46:20 GMT  
		Size: 13.6 MB (13647249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a41d3b4f0ee7936d37a29b00d6599e6c083cdd6c3c1e87cf67e60c78bed722f`  
		Last Modified: Thu, 03 Jul 2025 23:46:17 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f524d76f0354b6ecc378e1c665757264918c0c040f2a2bd64cba788277962ef5`  
		Last Modified: Thu, 03 Jul 2025 23:58:15 GMT  
		Size: 25.9 MB (25899209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b67d88191e3b93b0f89624b65ae059ddb9c9fcd006fed35442912ab0d7d2aa0`  
		Last Modified: Thu, 03 Jul 2025 23:58:12 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c774e0dfa624b0cea963362b48770f5024e53be14d0ea36d5c3b7c0588faf289`  
		Last Modified: Thu, 03 Jul 2025 23:58:12 GMT  
		Size: 20.0 KB (19995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388812f729656e82ba33e3c02a8954c18f8f04526ec86f97db930f763dda564e`  
		Last Modified: Thu, 03 Jul 2025 23:58:12 GMT  
		Size: 20.0 KB (19992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:957b714db399e7d03c09032dd0e24f0b4468c91ee7f01c67a4d7f31f4668c168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.3 KB (321257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deae1b4e215233e0e0e06e2b17cabf98cc165bf6f7597d995d82478f67468868`

```dockerfile
```

-	Layers:
	-	`sha256:4c1b2d6f71066ac867e7a713345ca974a76d9e5a5ab50b78a2e18f2ec7088c76`  
		Last Modified: Fri, 04 Jul 2025 01:59:45 GMT  
		Size: 279.6 KB (279567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ced30afda84cdd470c103701af5b4c3d33396f66576f417497dfcfe53eed4f9c`  
		Last Modified: Fri, 04 Jul 2025 01:59:46 GMT  
		Size: 41.7 KB (41690 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull php@sha256:5fe77fb73e787089b0bf9a9961d70a6b4d082a633b0ae4b0edc7a1d2c97ed4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50065946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabcac2d1514876052c6267d272854ead4e3c2776109ec0dd64e1d316087cb48`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Jul 2025 14:40:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Jul 2025 14:40:24 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_VERSION=8.4.10
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Jul 2025 14:40:24 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73985aec8f2b878dbb559825b96bc42ecedc3f93d14e5f1b9a6ca2e1816299c`  
		Last Modified: Thu, 03 Jul 2025 23:26:01 GMT  
		Size: 6.2 MB (6231904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2edf112b2c5bea025053bf307e764ef87252d3b53a912374edb00c6b9cda47`  
		Last Modified: Thu, 03 Jul 2025 23:26:00 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106cb39859ac9004e783043bb75563ecfc6db5970ab2b1965a10cfec3c797d10`  
		Last Modified: Thu, 03 Jul 2025 23:26:00 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b220f2eaec9520ea981fe044dbd753069e82acc397dfa855f2a332e39b93468`  
		Last Modified: Thu, 03 Jul 2025 23:26:01 GMT  
		Size: 13.6 MB (13647248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d569bf8384ea7859bc5bdebb7b303dc9b3a01a31162528b5298988b410fd2ace`  
		Last Modified: Thu, 03 Jul 2025 23:26:00 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45863f66c30bb4d03ccdda4d8033ac10f701a2a40ebbf057c4785e510e08621e`  
		Last Modified: Thu, 03 Jul 2025 23:34:09 GMT  
		Size: 26.0 MB (26006771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92c8a05ea92c1781b1b7bcaa42e2e8596293ba54c6b811a3e0bd1f39942ccc0`  
		Last Modified: Thu, 03 Jul 2025 23:34:06 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b94b5888e7b858522661203fa9ab8755eb5b86ba79a616c9def781b277d013`  
		Last Modified: Thu, 03 Jul 2025 23:34:05 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0576a89959422c21db006152715dff127526866ec770f15f789426099ac8a6`  
		Last Modified: Thu, 03 Jul 2025 23:34:05 GMT  
		Size: 20.0 KB (19999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:b1c0637e3fcb56740aa89a0f80e8079ce2294ac61e793f752856f786e8a0caf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.3 KB (321349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affac67f96ac0cc16a3bc6b87aa0a771ecc5323f333fc4093c7013bc4daf9520`

```dockerfile
```

-	Layers:
	-	`sha256:fb708dd84b75b130e7f50b103fc616e7b9ceff5d9daa1b9d4958e6c900aacf2b`  
		Last Modified: Fri, 04 Jul 2025 01:59:49 GMT  
		Size: 279.6 KB (279603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00174a39d65726503ee0cb98fc83d8cadb1f4adcb2d98aa690202e14c429ad88`  
		Last Modified: Fri, 04 Jul 2025 01:59:50 GMT  
		Size: 41.7 KB (41746 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine3.22` - linux; 386

```console
$ docker pull php@sha256:52001109f79156a7379f540740b68392e82b91421d261b57d8cdc0025017bcc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50156376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e7ebdd3fa97602fb530e4ed3a4fe917ed65312836b9a340fe2ff2d4e925ec7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Jul 2025 14:40:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Jul 2025 14:40:24 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_VERSION=8.4.10
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Jul 2025 14:40:24 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a092f1bda6ef198e62395f0b206601e5922c1a6271f16dc1846266eb3bffdc2`  
		Last Modified: Thu, 03 Jul 2025 23:05:31 GMT  
		Size: 5.8 MB (5806969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbdb73dc089983876e055e036d93788fa1587337d07465e845e14bfd6bba0d5`  
		Last Modified: Thu, 03 Jul 2025 23:05:30 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a14602c696f40b5eedce16d23c67090b4667f6d988970859cd3593263308ce`  
		Last Modified: Thu, 03 Jul 2025 23:05:30 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f84a66bd8abae7a77fa4b999cbed45916bf88f42f98bc21751c92f7e55b45ee`  
		Last Modified: Thu, 03 Jul 2025 23:05:31 GMT  
		Size: 13.6 MB (13647234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520b61b5a5e515909b7824732f6dd5b704dcbe2f57d6df28c39606e161607899`  
		Last Modified: Thu, 03 Jul 2025 23:05:30 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7765ef7a4cf337576a9ed9c9698c0b6c45f914b41be222ef500353134a275b`  
		Last Modified: Thu, 03 Jul 2025 23:05:33 GMT  
		Size: 27.0 MB (27041675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2886fe5a82db0dadb7a73b6fd6c06b720041e135012b5e0555d2ade580f090`  
		Last Modified: Thu, 03 Jul 2025 23:05:30 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14d11c4f444a84c2e17b16b1d3c271f45a52ff8b6b05d96fa5a3460dba75d6b`  
		Last Modified: Thu, 03 Jul 2025 23:05:30 GMT  
		Size: 20.2 KB (20195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ec83c439739dd6d76ac7cf6c94e52b7e4bca36718f0e41f353a23e96d027a9`  
		Last Modified: Thu, 03 Jul 2025 23:05:31 GMT  
		Size: 20.2 KB (20191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:91f9cd3a706d839ae18b3aa603ca3c35e082e848797bf1625d7de51c031ad4e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.9 KB (323884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f847c764cd29d000e92e9f7a574a3506e4812c156091e54b7987a23434fbcc1`

```dockerfile
```

-	Layers:
	-	`sha256:be297d93c3380409fdacb33f3643e1c99b384a8db78d9395963c4ef85d8a0444`  
		Last Modified: Fri, 04 Jul 2025 01:59:53 GMT  
		Size: 282.4 KB (282444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ecf65186a02595aca2465112f09e6074d5e9a9479258c8c04547bbbbfe0c62`  
		Last Modified: Fri, 04 Jul 2025 01:59:54 GMT  
		Size: 41.4 KB (41440 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine3.22` - linux; ppc64le

```console
$ docker pull php@sha256:26b65ab98fb0ff58841f9b110df652d36e11b16c298526cede036c6267243b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51147179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506de853f9afe1ecae3210bb7ff36f4891d65ad1eb430e841ad8083b314f44d0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Jul 2025 14:40:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Jul 2025 14:40:24 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_VERSION=8.4.10
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Jul 2025 14:40:24 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7db3af28cc31124a8bce98c13cd1b2512963d13f437d0d67f9918df0d57d2b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 5.9 MB (5946924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ec39d79edfa484fac002ed8c640f17ae8077df4dce88811d8d186865593a6b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 939.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2995d4272705fc452f2b3ea9e2d118681efbad9f858c7743f6f69364d73a50`  
		Last Modified: Thu, 03 Jul 2025 23:15:35 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da4669ab0266f9dd895304e7c92d52e7df1b0acfdc30e6abf0d73fd20c6d09a`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 13.6 MB (13647243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdb584c1e59e66bf7047b954cfc1e41ae7df62560b963934f349b9bd0a11fed`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064eb10aa0838c95212bbf26d0c21cdf184297e154d2e27884eeee455a286f44`  
		Last Modified: Thu, 03 Jul 2025 23:23:18 GMT  
		Size: 27.8 MB (27778711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f418b450c228a0d1ef55aa70940fe5004fe06311169578611777e90a6e98ed39`  
		Last Modified: Thu, 03 Jul 2025 23:23:15 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce95daecb425ec57b6d6cacbb9a0a407e712ef52aa0a8d76e7d3e8854640c439`  
		Last Modified: Thu, 03 Jul 2025 23:23:15 GMT  
		Size: 20.0 KB (20009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba002f2f2ab39589f7cd7d445addc17f83545169dfa3db8fef1289c40bb28384`  
		Last Modified: Thu, 03 Jul 2025 23:23:15 GMT  
		Size: 20.0 KB (20007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:968514c40936b5d2664cfdd2aa495e3f2e7445f4e13464b94bf08543a36340f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.2 KB (319190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38d2a8e2e1b7ca0cb2db1954c7286c2512d7cb1872dcaff18e23e8dff26efb2`

```dockerfile
```

-	Layers:
	-	`sha256:13cdb052cbb347b22f09eed1e8650826de8029669302df47ef2d3bc6cb8fcedb`  
		Last Modified: Fri, 04 Jul 2025 01:59:58 GMT  
		Size: 277.6 KB (277606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b61f8e962619e848bfcb61ff4806451590d746b4177d1f6c88a1ac7e8856040`  
		Last Modified: Fri, 04 Jul 2025 01:59:59 GMT  
		Size: 41.6 KB (41584 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine3.22` - linux; riscv64

```console
$ docker pull php@sha256:a7a1c57c0c6f61dfcef66d92b5f7c694f784ff5c48ab775565c842351a902677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49916660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e6c6bf7eefcc385a720b02684589aea4cab57b24b32b5ce738177001aec86c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Jul 2025 14:40:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Jul 2025 14:40:24 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_VERSION=8.4.10
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Jul 2025 14:40:24 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fef9af04f77cee78d12af5c916be05fdbafab520d953b27a0e22aabf6917d85`  
		Last Modified: Fri, 04 Jul 2025 00:22:03 GMT  
		Size: 13.6 MB (13647251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae4f98ceb1c3250752dcd6d2b2322a49e9241e8b32b996d4fc611be6bbb87a6`  
		Last Modified: Fri, 04 Jul 2025 00:22:01 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006b2a575e53236bfccff44de61015f9d312da5114822ad45559f71f7171165d`  
		Last Modified: Fri, 04 Jul 2025 01:22:03 GMT  
		Size: 29.1 MB (29108157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943bc7057dc49e8beffedca76c47d537d461c1a7cb73ed631d062331a6a86b01`  
		Last Modified: Fri, 04 Jul 2025 01:22:00 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb007279c9314f70948cd5adc59e6e4e522654fd5fda47630b3a84f39c7cbc3`  
		Last Modified: Fri, 04 Jul 2025 01:22:00 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b635916968f03cc69a8cf1fcdc0212d454dffeee2bfffa907c4d90cce2d80d92`  
		Last Modified: Fri, 04 Jul 2025 01:22:00 GMT  
		Size: 20.0 KB (19991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:84f8e6c14c5e9abeaa43b06c066105acced5dac46b49d943487db4cef06750f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.2 KB (319186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b60642fd50ba58b79a9f82dca968bca1a2d186713129bfda9e80750a2ce3c84`

```dockerfile
```

-	Layers:
	-	`sha256:2942601dbe4507c864c9003530a1e7e4206543ad0f369da3b4e12c13449afede`  
		Last Modified: Fri, 04 Jul 2025 02:20:48 GMT  
		Size: 277.6 KB (277602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad517527c980ef4d43ec7e9186e8f61681a5a85a44eb5d4e9059963d0c6c9a1a`  
		Last Modified: Fri, 04 Jul 2025 02:20:49 GMT  
		Size: 41.6 KB (41584 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine3.22` - linux; s390x

```console
$ docker pull php@sha256:8b5d6dcdb068ae9b1c1c05620b21b313041e2f5b866d7677b8e6608b8bd8d593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50731373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2a46ec0a46427f5f743d9789f96027ea0d3b019faee6725f80753e6c32ddd7b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Jul 2025 14:40:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Jul 2025 14:40:24 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_VERSION=8.4.10
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 03 Jul 2025 14:40:24 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Jul 2025 14:40:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Jul 2025 14:40:24 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abd3e67b018bcd8c0aa4d0434d7ec04dcdb3a3cfbf444a313e2be49d0524ec2`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 5.9 MB (5932552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f41e4866617495859c5133b898f769b3867a6a3ae061aa9561da765981c5ad`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9335ac6e22dd0c0b2e07f4a5406c437168067a987662ebd8bcd3b269496018`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da3506587d8ded424a7c5730d972ae6f1735f6afc1a325c7e9f83474f399fde`  
		Last Modified: Thu, 03 Jul 2025 23:16:27 GMT  
		Size: 13.6 MB (13647264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671a375a1790dbb9b0d83c7dd0560e7f6e75fb5b06afbc76019557052c897e5a`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9925d85071d1dd1b2ea41923bf2c620494e341f9c7d646c8e7a9e4f9ab9845`  
		Last Modified: Fri, 04 Jul 2025 06:37:14 GMT  
		Size: 27.5 MB (27459948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fca4b34ee2c9b2228b59a5ca061af1d76ad63e26057c4e86c7779dd9416ec9e`  
		Last Modified: Thu, 03 Jul 2025 23:27:52 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bc84e9037fe006ce953d2e95435be9d54ae4280ba90ed64e2fa9c008931359`  
		Last Modified: Thu, 03 Jul 2025 23:35:07 GMT  
		Size: 20.0 KB (19998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ffcaee82ec62c9e9b5068fbc59a3a3a89e3c5f49d5e65cc322a3b37de4ab131`  
		Last Modified: Thu, 03 Jul 2025 23:25:50 GMT  
		Size: 20.0 KB (19994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:5ae0d3c5dc142c2ecc06e793fcddff587ff8b7378ddb4af331baa557db5f4a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 KB (319052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fd7e302e583a17ce5f0334841adc2dfb5a4ed44d66059582459fd0ec3e6661`

```dockerfile
```

-	Layers:
	-	`sha256:f791e167ad73261d59474a7ec202b0eb8e994a1c23b4d6a4d6ddcaf28a2c98e4`  
		Last Modified: Fri, 04 Jul 2025 02:00:18 GMT  
		Size: 277.5 KB (277548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11ee0f9e41d17e29764e0fbd645648fa423d09110de09a4c8f78e75fda6f6d1b`  
		Last Modified: Fri, 04 Jul 2025 02:00:19 GMT  
		Size: 41.5 KB (41504 bytes)  
		MIME: application/vnd.in-toto+json
