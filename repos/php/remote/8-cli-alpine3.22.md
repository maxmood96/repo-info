## `php:8-cli-alpine3.22`

```console
$ docker pull php@sha256:f4482392d7f844ec3350dafc1f494ce0b1a7b30a278368de06f7035a3938e20a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `php:8-cli-alpine3.22` - linux; amd64

```console
$ docker pull php@sha256:8ae901385b46443dc59b7dea20c700dbc68e8d1e42d025c335029b09c35c33c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41899797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f04fd2db7589879359879abd6f98951125d9f7a7d452a855ea78c927072caa6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 09 Jun 2025 21:43:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 09 Jun 2025 21:43:33 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_VERSION=8.4.8
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 09 Jun 2025 21:43:33 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa41ed00f4f69f9b33b5e886fedfa6143b6e95cd34c48de5a67dfca449d27075`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 3.5 MB (3468342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3dd3a928e1a1d32cf4174792bbec9d7d27add5d439d1765653b7fc22f66b92`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0721ec88e7a2844011b208a2272d18e4e309abd51c06c8e85a7fd685455524c`  
		Last Modified: Wed, 11 Jun 2025 00:03:26 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f084ac2a53f05708a861a663438bea25fa87e41a10129b5c0a01e67aed1432c`  
		Last Modified: Wed, 11 Jun 2025 01:13:20 GMT  
		Size: 13.6 MB (13640521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87939f6f4e61218155cd7a88d809fc899e6d6a2b413033839baacad75def377a`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07468323dd1f0b8efa9f6be2eaf69811d60fee46c187e62fc1b05bd2bd100fa`  
		Last Modified: Wed, 11 Jun 2025 01:13:18 GMT  
		Size: 21.0 MB (20969804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d64e952347861cf8f1c360fcf1984249571751d095594a156d453d4cb4ec8b`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f854fc0d234074345274bcbda7bb11f7295b4bae6d7d400dcbe3bd892683a59`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:96ce5b0a6d5bbc2c83f110e2d01cacc8356ce0db65f33a09a2070f2402e637a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.2 KB (325226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099218972d8b1e89dcd07eecc98b1fa262ff8b2fd822d1572837ceab0b1f17dd`

```dockerfile
```

-	Layers:
	-	`sha256:bb7c49e4e6864ae6a0bf7def3ce51d45dca011c190d13d934440552004369273`  
		Last Modified: Wed, 11 Jun 2025 01:54:49 GMT  
		Size: 284.9 KB (284903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:413dac8493b5f7221639c58ef8fab12d6656ec77ad6dbf98b8c467dbe847b608`  
		Last Modified: Wed, 11 Jun 2025 01:54:50 GMT  
		Size: 40.3 KB (40323 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-alpine3.22` - linux; arm variant v6

```console
$ docker pull php@sha256:dd4e1d02357421b7638c1b26798165d3be961e9bea7c800c895672afc0ce8b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39689457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a988d8d228129dcfce4b2ffbb01eba26fbffa27f3f6d29a4993053c239822755`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 09 Jun 2025 21:43:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 09 Jun 2025 21:43:33 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_VERSION=8.4.8
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 09 Jun 2025 21:43:33 GMT
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
	-	`sha256:d738e6a7e1662efb7b90b7f0a4b2cce2f9247f395ab8c1924148a0d2dde272c3`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 13.6 MB (13640499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeec31f51dc18a99c6251ab6abd48a6b17b9bd04c498ca1ce606fbe0119a506`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a9bea01d63368fc6a169811ad55c9f7baf8d06c4a3c909bea5606bf5d161c`  
		Last Modified: Tue, 10 Jun 2025 23:54:15 GMT  
		Size: 19.1 MB (19091501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ab1a6cbed4c7bce681ea2c1ba6335b04364d328abb8504ac38b7cb01546c1e`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f7ac6548196a7241e2ff5aeb2ebaa92bd912151a57decbc09707501826e55d`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 20.0 KB (19986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:25a99a6dd488d027fa1c79c04d72c1e627103af2e4fbcd9cfba90adfe1eefc04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 KB (40345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547b23f0fdca30b0b8c471e72d955cad881580ec2737e19cef409fc907c607c7`

```dockerfile
```

-	Layers:
	-	`sha256:a6d92ebd96ca32f6c17f581946b116a3d8d4a41aac1ee3e1d1e36c40ece10b90`  
		Last Modified: Wed, 11 Jun 2025 01:54:59 GMT  
		Size: 40.3 KB (40345 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull php@sha256:6a8ef19f6ee53824c26f7be09fa15493fdf61a8bcafda4d6a1b85ea49549b07f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41790092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f0984d0e80433f6d4e1410677f8905b2b37e68343bd5603f4da279939e2446`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 09 Jun 2025 21:43:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 09 Jun 2025 21:43:33 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_VERSION=8.4.8
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 09 Jun 2025 21:43:33 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476e263556d24cfaaa81ec9153b95e1b25d54abdb35b46c3c74fa988a9f252f3`  
		Last Modified: Wed, 11 Jun 2025 09:16:54 GMT  
		Size: 3.5 MB (3470681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1e5bea448bb73ac691df99daf5772e7cb7307f122b4e0544c289a55be9ee24`  
		Last Modified: Wed, 11 Jun 2025 09:17:12 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49a64acbbc8d220ea4c16baed763b26899f58299a8b85d3b8513f03b3023893`  
		Last Modified: Wed, 11 Jun 2025 09:17:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123dcf4adf55a39c8cf4f202302f0a9dfd6d576c94bf8db94686e5a5ee1f4cf4`  
		Last Modified: Wed, 11 Jun 2025 09:33:08 GMT  
		Size: 13.6 MB (13640507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff08fc5740a571af506cddc0c38e20506f6151e574d4a10d77b748c7c3bd4b`  
		Last Modified: Wed, 11 Jun 2025 09:08:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc080435edc41cfa70a84f9586ffca3f880a9b4cedccc53c481889b18e1e1c2`  
		Last Modified: Wed, 11 Jun 2025 09:33:10 GMT  
		Size: 20.5 MB (20518887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3995038baa7f047e93509966aa2798fbc7bddf48517c43343b9add69edd5df`  
		Last Modified: Wed, 11 Jun 2025 09:08:59 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ae69002966a0d0881786cca5d1dfa7b1fb54c0e7b1e4b6bf9c41f92f6208ec`  
		Last Modified: Wed, 11 Jun 2025 09:17:23 GMT  
		Size: 20.0 KB (19991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:a137d4e513a6cb6474a3572f542836ea0196a051855e4d2f996744c59eeaea45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.8 KB (322759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67a823d54f059bf3665a8c4ed636950635418e8627804ebb91ab789317f1860`

```dockerfile
```

-	Layers:
	-	`sha256:72a0b514f531ad98bd2fe5cad63d34ec79491558829e97c5e993722a12d4d813`  
		Last Modified: Wed, 11 Jun 2025 10:54:33 GMT  
		Size: 282.1 KB (282113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0646caf466159870f975e3291f000255681e88de41147d963e39dc4a54cd499`  
		Last Modified: Wed, 11 Jun 2025 10:54:34 GMT  
		Size: 40.6 KB (40646 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-alpine3.22` - linux; 386

```console
$ docker pull php@sha256:b2b8e9b2546d41019dd69527f175cdc8e02402c0cf9334eb6c48601c7ee54da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42301600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58081147217e9595089a06ce685b4ddefe0e2a2895fa8596ebaa05104172907f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 09 Jun 2025 21:43:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 09 Jun 2025 21:43:33 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_VERSION=8.4.8
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 09 Jun 2025 21:43:33 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298f020aec5b2eb58f3f5d72ed081bd6c76a95799b7e438e4f3384447e42693d`  
		Last Modified: Wed, 11 Jun 2025 01:13:13 GMT  
		Size: 3.5 MB (3527774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3ebeb8397f1f59382fb3bd2f49e7ae5aa3c63f7a6f5adde3d5af0fe196ad48`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65c3fa431069cd36b1283a6dd73ec3c559701f45df22999775e61dd0dd4d578`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7db0fb8a413bd77d83d365246beba56a6d3ab745a296bb3119dd1c4844e7e2`  
		Last Modified: Wed, 11 Jun 2025 01:13:12 GMT  
		Size: 13.6 MB (13640494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c81720a5bbf56ccfa06979187dbca8afa1859fb3d323625fe188373b9a06ed`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8fb25f24bc12988d302f27fbc0c27090c75c814e4f8dcb4396e125eafae7cb`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 21.5 MB (21493036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b67d63641d3800bf94c0e5eb453a80e9e00ec38acbc41e8b2dbe883e470dd6d`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821e028fb8ab3dacea139b63763d5d53b2d0981367d47fcd3f94182a0a2ac456`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 20.2 KB (20182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:7c09e3b104ad8bb150e5873470caf0ec275b083016a06739611eaa46a07b5c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.0 KB (325039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932be414954700a7b30406a8fda6c62ec1289bbc22e0b6e9a2235fa348cf0af7`

```dockerfile
```

-	Layers:
	-	`sha256:ab3507c5ed42724dd29ea5dc556a1a422186ad47fecb3cf150389595444d7cc7`  
		Last Modified: Wed, 11 Jun 2025 01:55:07 GMT  
		Size: 284.8 KB (284818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca2117bcef907c9683c607660177ce929c88d9352a8cd0ae35dff899e8d22c1`  
		Last Modified: Wed, 11 Jun 2025 01:55:08 GMT  
		Size: 40.2 KB (40221 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-alpine3.22` - linux; ppc64le

```console
$ docker pull php@sha256:6daf9cf4929be97795f0cbf09ceab5793bbf693ae17e2801214cdcee9eef7934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42887975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b712f196e2db80a623d7a5738b8f0f81c17af97c90ee8cf704ae41595c382b57`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 09 Jun 2025 21:43:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 09 Jun 2025 21:43:33 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_VERSION=8.4.8
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 09 Jun 2025 21:43:33 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a27d95a001e42dd9b82fe6b7e63b48f844b2bd3aa5239c663167b36d4f1fa42`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 3.6 MB (3619144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0377d467323561e29ac5bd8915837530c91c4ef72b3a2f4ad73bbcd6d467c36d`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b63ba550992ed4fdaf12dd9e376ec5efd146f93f3e9f970030c609f95b4c30`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeaaf729ae44f9ac3f9b3f4551595556a417993152b53954f6f6a89f90a4954`  
		Last Modified: Wed, 11 Jun 2025 09:12:57 GMT  
		Size: 13.6 MB (13640505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5928f2bed6e9375b5161e1fcbc32d598a194fc67da4a537c5d6a3aaab21aa3d0`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951f75742ee54512415191653f6d3e2b7b2a4ff66bc4dcc60a24c12d00a0db76`  
		Last Modified: Wed, 11 Jun 2025 09:12:58 GMT  
		Size: 21.9 MB (21874047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189ddb23dd34f7e52d4b584e89ed11029f27d1dee76f138e62d772e61c75c0b6`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2c88f7798e99a903cbf372177b9f7b8f2c70690f8dac0d589ec956038b045f`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:db4eed88c15154071507ef63ac0cb40294e16215c628aff466a764fb25adad35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.5 KB (320517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6abaa22b4fda533db42fd12ac1e633d5d6751533d728ae007b5eb62f03d6e4`

```dockerfile
```

-	Layers:
	-	`sha256:d8c61eb34e6f7a9fc97910da9216c7740e96df4cdc67153906751f6cd531e122`  
		Last Modified: Wed, 11 Jun 2025 10:54:45 GMT  
		Size: 280.1 KB (280068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71d49bfd8f302e082eb3d3d0a5e6e4a9befdf9c7f0a46228fcccfce97cb7cf65`  
		Last Modified: Wed, 11 Jun 2025 10:54:46 GMT  
		Size: 40.4 KB (40449 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-alpine3.22` - linux; riscv64

```console
$ docker pull php@sha256:2ad620d07eb4811d923299c66ba307a5953ad9ed400cdafb44f2dc965c467b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41170354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b591ae22ed40594680b356636bbe64ef463e0271a9057aa626a5664813deefcc`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 09 Jun 2025 21:43:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 09 Jun 2025 21:43:33 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_VERSION=8.4.8
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 09 Jun 2025 21:43:33 GMT
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
	-	`sha256:44d0224769088850e26eb3ba2638a8a3febc4b65991ac8cc63dc3f29cf199070`  
		Last Modified: Wed, 11 Jun 2025 05:05:11 GMT  
		Size: 13.6 MB (13640513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a45f979f3844cfaf9ad9f1a00668b3bb56bc478c711f2d939a7dba0c2ed6e1`  
		Last Modified: Wed, 11 Jun 2025 02:39:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b864e2d5fb63463e7b594794f1b0077ef70793371e80280a29b09008bb9771a`  
		Last Modified: Wed, 11 Jun 2025 05:05:14 GMT  
		Size: 20.4 MB (20388593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba389b9b1d6d27f7a263c92d52685675ded66f85f52a097bec1b658400eebc5`  
		Last Modified: Wed, 11 Jun 2025 02:39:58 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb4f8cea261544e7d849e5aa9581396ef8d4bd1b7c14ceb536acc047c9ff257`  
		Last Modified: Wed, 11 Jun 2025 02:40:00 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:ab36a8ca084fa5b709931473b3acfdea16b9323de27e70f15e323c1a4a9638c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.5 KB (320513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f5c389e260478a26500f54643801be610fee8a456ca6c95eab1ec499af8e38`

```dockerfile
```

-	Layers:
	-	`sha256:10efe67d34c19751db4e408bf2c2a69eecc270936b0aef6eae12c6193dff6f50`  
		Last Modified: Wed, 11 Jun 2025 04:54:37 GMT  
		Size: 280.1 KB (280064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9abb8d469ea64447564c72c7fb5be294e32e5948d43994e5b9bcd74844763818`  
		Last Modified: Wed, 11 Jun 2025 04:54:37 GMT  
		Size: 40.4 KB (40449 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-alpine3.22` - linux; s390x

```console
$ docker pull php@sha256:bb21d6833e3f1b36eaea78b51773b0cfa1bf2972a21fc26579048ce6f8600686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42457920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29996b3c49f363e7682490c9f9c77fec1b0003d3d54637c8c31f7dbb5c18f59`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 09 Jun 2025 21:43:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 09 Jun 2025 21:43:33 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_VERSION=8.4.8
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 09 Jun 2025 21:43:33 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78969cb3507a7e09a6a1541cd0fe9a6e6ba70522f240c985e34a594a5c5c2db`  
		Last Modified: Wed, 11 Jun 2025 06:32:49 GMT  
		Size: 3.7 MB (3698999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86831d5f3921b134159344ea1287339c8645e651a6ee0db4a544874087b848c3`  
		Last Modified: Wed, 11 Jun 2025 06:33:00 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb672e9b170264102c0793a333d3f87a8a40a5f4ac69848957f71e5c752d123`  
		Last Modified: Wed, 11 Jun 2025 06:33:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1035d42a37d5be6b1617300170ead6ce8970a5e2e4154fe287efc8af1e2f7441`  
		Last Modified: Wed, 11 Jun 2025 08:13:18 GMT  
		Size: 13.6 MB (13640519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca62563344c489947dce07a51fbce42cb5c2f338f525f3dc64a869bb23eea05`  
		Last Modified: Wed, 11 Jun 2025 06:17:32 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b12b2d32a5b3932415a1a3b75f1dce848914c79f4be0b381c79061048ef8945`  
		Last Modified: Wed, 11 Jun 2025 10:56:19 GMT  
		Size: 21.4 MB (21446797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d13957f45dfaafb933ab00f3283ea48d057cd2179a84687ebe45ad163f535de`  
		Last Modified: Wed, 11 Jun 2025 06:17:35 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db48dd1edbbaf646c03ef3f286cc921fbc422e665578b988b9d03d890364f0d5`  
		Last Modified: Wed, 11 Jun 2025 07:14:21 GMT  
		Size: 20.0 KB (19993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:c74c7b66258914c8d414e701b9290ee006da6522dae2862b2245fcb618301937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.3 KB (320285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e83ea17bfe67513f2a9113f0534d5024438f4078bfc9dccb525a12b4f1f89f6`

```dockerfile
```

-	Layers:
	-	`sha256:636ded5c3e95f59b9a65709f549642908861f3f1800864b0e6177b47313f1751`  
		Last Modified: Wed, 11 Jun 2025 07:54:35 GMT  
		Size: 280.0 KB (279962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ce28da3880d8c41a59a1a07ad64a0c6ae5321cf9fcc26e2e5b5e1f36c4ba809`  
		Last Modified: Wed, 11 Jun 2025 07:54:36 GMT  
		Size: 40.3 KB (40323 bytes)  
		MIME: application/vnd.in-toto+json
