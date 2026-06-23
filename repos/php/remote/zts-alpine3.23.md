## `php:zts-alpine3.23`

```console
$ docker pull php@sha256:61a264700202abd9f115ed5046689b886c2f667dd3dd2699dd0277d28da7f705
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

### `php:zts-alpine3.23` - linux; amd64

```console
$ docker pull php@sha256:1d8a1f505f543cf225d059fe4ecef928033d624302a5cc9c5ee932b8c89369a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50718728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7329276347a9863b3a99d9d2196ee5b583755b56d7f22df2fc6a65d5462fbed8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jun 2026 19:46:42 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 22 Jun 2026 19:46:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 22 Jun 2026 19:46:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jun 2026 19:46:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 22 Jun 2026 19:46:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:46:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:46:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jun 2026 19:46:43 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 22 Jun 2026 19:46:43 GMT
ENV PHP_VERSION=8.5.7
# Mon, 22 Jun 2026 19:46:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Mon, 22 Jun 2026 19:46:43 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Mon, 22 Jun 2026 19:46:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 22 Jun 2026 19:46:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:50:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 22 Jun 2026 19:50:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:50:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 22 Jun 2026 19:50:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 22 Jun 2026 19:50:01 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1af1cdaa5bae119fb5fe54c90fa172e0778b805ad29bfb48117091440ec75e`  
		Last Modified: Mon, 22 Jun 2026 19:50:09 GMT  
		Size: 3.5 MB (3465280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a67d433cafc1fa74d5c4862f1e964bf3ca19c3a4a9cca70d2a0828fc72dab28`  
		Last Modified: Mon, 22 Jun 2026 19:50:09 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d1f9ba21d5b61e5ab71cef71ef69640b40dce76758e0c7b481ee8dfe2f6b95`  
		Last Modified: Mon, 22 Jun 2026 19:50:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305fecb2f946e469632c3e58f8d85d769907dd855a692ad9e1443aa74c05f0f6`  
		Last Modified: Mon, 22 Jun 2026 19:50:09 GMT  
		Size: 14.4 MB (14421092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f487f4afa04f67c5c3f882f4f27461d0fd53ebcdcf1bb3569f57325080f2410`  
		Last Modified: Mon, 22 Jun 2026 19:50:10 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33642e3a3261a45ed0a37cf66605d906c6f307d6e79529a39e510a2f22a213b9`  
		Last Modified: Mon, 22 Jun 2026 19:50:11 GMT  
		Size: 29.0 MB (28961533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2472b751aa34a81c6fa05c51f1af33f110428e6362c10bb8cdc799c3ac1f852c`  
		Last Modified: Mon, 22 Jun 2026 19:50:11 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cab9264c2143b171776bc7f23c8acc2a5e4e6607dd3f6009759b763d0c560d9`  
		Last Modified: Mon, 22 Jun 2026 19:50:11 GMT  
		Size: 22.3 KB (22315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine3.23` - unknown; unknown

```console
$ docker pull php@sha256:f533d82e75449c318d359e53123d74ca33ec2010a35c24041d895fa041a56b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 KB (296580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15b88057f07ea14920ede7369a0304b14d68b3c89f8b5ffb6159135dbda9bae`

```dockerfile
```

-	Layers:
	-	`sha256:2efb1ba46837e0ed899dd25b929e011fad8cc0b912be2c857584a5f735795624`  
		Last Modified: Mon, 22 Jun 2026 19:50:09 GMT  
		Size: 259.2 KB (259247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2434d6e66686c3d802c714ca8d7e92f484e2a00577e6b38228000ebbe52f2193`  
		Last Modified: Mon, 22 Jun 2026 19:50:09 GMT  
		Size: 37.3 KB (37333 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine3.23` - linux; arm variant v6

```console
$ docker pull php@sha256:bee8d857c9e69771af7f021a065504856285a4fe5f1979874c7359b922eaa276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46547263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50b605aa33582a72e571e329f4f9480303a5c5edbdc91dd20ff76d37b8b5dd2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jun 2026 19:46:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 22 Jun 2026 19:46:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 22 Jun 2026 19:46:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jun 2026 19:46:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 22 Jun 2026 19:46:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:46:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:46:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jun 2026 19:46:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 22 Jun 2026 19:46:16 GMT
ENV PHP_VERSION=8.5.7
# Mon, 22 Jun 2026 19:46:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Mon, 22 Jun 2026 19:46:16 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Mon, 22 Jun 2026 19:46:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 22 Jun 2026 19:46:19 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:49:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 22 Jun 2026 19:49:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:49:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 22 Jun 2026 19:49:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 22 Jun 2026 19:49:34 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0db8c18d35aeb2a1d64f0fc503a66241e07c11ad297de72a034ade7fbb619bb`  
		Last Modified: Mon, 22 Jun 2026 19:49:41 GMT  
		Size: 3.4 MB (3419481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7389a833221b5beee52ae9eda5ac30bf065b78e1ecae51d8dbc9a8c053b0ad`  
		Last Modified: Mon, 22 Jun 2026 19:49:41 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd70a12896827462c7315a21e410ee6a2c47255abc13faf62f8247f35f00587`  
		Last Modified: Mon, 22 Jun 2026 19:49:41 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661ac4953412eca0ab5f7aa2fc22deae7f79de9ca42c43374fe7a159a54573ec`  
		Last Modified: Mon, 22 Jun 2026 19:49:41 GMT  
		Size: 14.4 MB (14421125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13d3a31ce76396021fe70c7223dd14467e68cb5cb5c9259ee940a654aba187e`  
		Last Modified: Mon, 22 Jun 2026 19:49:42 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba36b3c4507df42813cb42ac69ddd7113d37a91028c98a00cdf836dfc108a216`  
		Last Modified: Mon, 22 Jun 2026 19:49:43 GMT  
		Size: 25.1 MB (25127837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b41648b6a1c88ebb328a31337fff9d1387d3bd157149aceda2ade53ba3af122`  
		Last Modified: Mon, 22 Jun 2026 19:49:42 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5329cdb250a00a1a880cb63603f59ef3fc857abab9d06f918372c970e94e1785`  
		Last Modified: Mon, 22 Jun 2026 19:49:43 GMT  
		Size: 22.1 KB (22145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine3.23` - unknown; unknown

```console
$ docker pull php@sha256:cfcabf4d79442ca25ee20fc0f344407dead730fae97e94d5427405094e8e6b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 KB (37263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129a480ae369fabeaefc8da776808626ecc13b46b4a177f4d27f64f51c222628`

```dockerfile
```

-	Layers:
	-	`sha256:8aeeed3cdf949946bd4c20cc6199c6fc4c3373777ac08307fec819eb5f485d44`  
		Last Modified: Mon, 22 Jun 2026 19:49:41 GMT  
		Size: 37.3 KB (37263 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine3.23` - linux; arm variant v7

```console
$ docker pull php@sha256:9249f049e1f854cbe8e7f14dd1a0e7d8e78ef5664a0c860be4984377bf03e4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44611248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa80a059eca1475423a671b7338a1dca2fd0bbb3a146a6324a9e8d07fde94555`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:18 GMT
ADD alpine-minirootfs-3.23.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:18 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jun 2026 19:55:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 22 Jun 2026 19:55:29 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 22 Jun 2026 19:55:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jun 2026 19:55:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 22 Jun 2026 19:55:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:55:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:55:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jun 2026 19:55:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 22 Jun 2026 19:55:29 GMT
ENV PHP_VERSION=8.5.7
# Mon, 22 Jun 2026 19:55:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Mon, 22 Jun 2026 19:55:29 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Mon, 22 Jun 2026 19:55:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 22 Jun 2026 19:55:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:58:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 22 Jun 2026 19:58:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:58:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 22 Jun 2026 19:58:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 22 Jun 2026 19:58:42 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:177f8e1e6f831989320cf2b59b7eabd21cbf36804c79506912f3a81caff426f2`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f18f4f12d927611d762623a3e1c736e11ddc31a842de2067680c495cc8f4cb0`  
		Last Modified: Mon, 22 Jun 2026 19:58:50 GMT  
		Size: 3.2 MB (3229667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09b7014867097e19048e9ae6ed271c63b472d1f5bc065fbad5469c13c3a3dce`  
		Last Modified: Mon, 22 Jun 2026 19:58:50 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7584e22d7a1b8248abd109eeebb14e1321aa651bb9371bdd96793e7a66d368c5`  
		Last Modified: Mon, 22 Jun 2026 19:58:50 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69b97d7147999b57de1172d08669ab12a8428aa98abfe1ab6ff8f9549d38c3d`  
		Last Modified: Mon, 22 Jun 2026 19:58:50 GMT  
		Size: 14.4 MB (14421134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed39470e6c5051ae90c2f95548c886a91354aacf3fa152ea20be18db105110f8`  
		Last Modified: Mon, 22 Jun 2026 19:58:51 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b6126a435f00d3a0e66026e23da7afbd418361048e3973390683551edabe58`  
		Last Modified: Mon, 22 Jun 2026 19:58:52 GMT  
		Size: 23.7 MB (23672389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dc5e73f0965541f836a9c121ab7810c54b587f67709bda252609271a13f43a`  
		Last Modified: Mon, 22 Jun 2026 19:58:52 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7e671626f8428536339eb370f05b0b65e5c08b7ea7fa20c74bc9a684b945d7`  
		Last Modified: Mon, 22 Jun 2026 19:58:52 GMT  
		Size: 22.1 KB (22124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine3.23` - unknown; unknown

```console
$ docker pull php@sha256:f455c27d48d156823824e3d4c4658b8d55617f8c2776ffcb01b41ae8c104df1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.1 KB (293120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7dc045febd835af39f68c4a33bafe98772aa3a03bc8d105a7caeb008ff8891f`

```dockerfile
```

-	Layers:
	-	`sha256:f402336aec93a812d9c41f6a1b9df8cabbbb4dd41521d7173da721b6d130205a`  
		Last Modified: Mon, 22 Jun 2026 19:58:50 GMT  
		Size: 255.6 KB (255643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c9cb4c969f872635b0c24f29731f45e4a8e9c9efe5139cd93b8e1141171dac4`  
		Last Modified: Mon, 22 Jun 2026 19:58:50 GMT  
		Size: 37.5 KB (37477 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull php@sha256:cb84756f1e760ac92f6fd0b9378ccbac3b54e79668b9eb3d02b3496e5b5df468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50004577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07634cc424309037014b175416ac419cb1e3e4646e872e2c3377331ec9665e8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:47:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jun 2026 19:47:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 22 Jun 2026 19:47:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 22 Jun 2026 19:47:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jun 2026 19:47:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 22 Jun 2026 19:47:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:47:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:47:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jun 2026 19:47:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 22 Jun 2026 19:47:25 GMT
ENV PHP_VERSION=8.5.7
# Mon, 22 Jun 2026 19:47:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Mon, 22 Jun 2026 19:47:25 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Mon, 22 Jun 2026 19:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 22 Jun 2026 19:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:50:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 22 Jun 2026 19:50:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:50:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 22 Jun 2026 19:50:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 22 Jun 2026 19:50:54 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d5fd78b319a9087fec367c204bd7f7c9296481a02a3723e1f1b75871cd49c5`  
		Last Modified: Mon, 22 Jun 2026 19:51:03 GMT  
		Size: 3.5 MB (3476751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3b6a02680a5a3f4643295647860fccebb2ba0e865966f7b407fe833b773b9d`  
		Last Modified: Mon, 22 Jun 2026 19:51:02 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3a3abc9d118fda44063064fd298a5289e2096565bd61db93dfb2f0b6675d2a`  
		Last Modified: Mon, 22 Jun 2026 19:51:02 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843d64670d8e0886545b046841abf876d70fcf2aded8a2e3274624826b90f0b9`  
		Last Modified: Mon, 22 Jun 2026 19:51:03 GMT  
		Size: 14.4 MB (14421108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95745831280563ba42e2576b0e6e0c311bb0cb21febb17fc01d8401665510801`  
		Last Modified: Mon, 22 Jun 2026 19:51:03 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19ecaca60a03daf1879155f27e43374d403311f6f660426918692cb90158509`  
		Last Modified: Mon, 22 Jun 2026 19:51:05 GMT  
		Size: 27.9 MB (27898647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3c083b054b50a59168e4befe806c49a2f73f5c4ff4700e37f0f42c8fc8ec03`  
		Last Modified: Mon, 22 Jun 2026 19:51:04 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7379e10473d4e46a8d8d5d17d1c98d85999b050a1b48cbe809dda137ef67c4cb`  
		Last Modified: Mon, 22 Jun 2026 19:51:05 GMT  
		Size: 22.1 KB (22129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine3.23` - unknown; unknown

```console
$ docker pull php@sha256:40b9cd0c1e09130809169c942c587b673803e183fa6cac66100f9ac168561fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.2 KB (293175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25491a6ac7b2532411a8edad6b7f9936af0ac51ebbe5110a3bb52bbb164fa150`

```dockerfile
```

-	Layers:
	-	`sha256:6949ad51bc6bbd6a81c05210e586c0a70d84031b44d5001d4bbac4477fbc1a26`  
		Last Modified: Mon, 22 Jun 2026 19:51:02 GMT  
		Size: 255.7 KB (255663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72bb81528bcf33ebfa5797cc91236cb2ee9e4b13007cac38d333be261e7334e1`  
		Last Modified: Mon, 22 Jun 2026 19:51:02 GMT  
		Size: 37.5 KB (37512 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine3.23` - linux; 386

```console
$ docker pull php@sha256:4520a703bffe3dcdf5cf4844af6bb3772c3187f5d869e1ddd976ae220769c9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51037323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ffcacbb2d16a1cfdb66ff1790179553ff0f57750b76e4d1403e1991965a244`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jun 2026 19:46:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 22 Jun 2026 19:46:26 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 22 Jun 2026 19:46:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jun 2026 19:46:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 22 Jun 2026 19:46:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:46:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:46:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jun 2026 19:46:26 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 22 Jun 2026 19:46:26 GMT
ENV PHP_VERSION=8.5.7
# Mon, 22 Jun 2026 19:46:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Mon, 22 Jun 2026 19:46:26 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Mon, 22 Jun 2026 19:46:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 22 Jun 2026 19:46:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:50:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 22 Jun 2026 19:50:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:50:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 22 Jun 2026 19:50:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 22 Jun 2026 19:50:14 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edc33c64e6ce4436a6483ed772b5d48038a24101ebb051af7c17a671f5c0d0b`  
		Last Modified: Mon, 22 Jun 2026 19:49:57 GMT  
		Size: 3.5 MB (3495880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f784e8ff2ddbc6bcb9f94b339eb1d05d6d39279dd13a15720122a172f7c908`  
		Last Modified: Mon, 22 Jun 2026 19:49:56 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664083ecc53183f5e9289de341f761b117e3a2fc9da0c6025ffed0864ffd2ded`  
		Last Modified: Mon, 22 Jun 2026 19:49:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c364abf98af30a67fce66ee45dbfeb8b6278d728f57df692d4858d81681e9b`  
		Last Modified: Mon, 22 Jun 2026 19:50:23 GMT  
		Size: 14.4 MB (14421079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29730daa92a9c14379004538cf1eb1ad5a884e2f26852854134963e13b7c5caf`  
		Last Modified: Mon, 22 Jun 2026 19:49:58 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6b0ac4cff5ccc8e0179f74c27f2a0cf9d1fb6de19992ca550610397ca4a6a2`  
		Last Modified: Mon, 22 Jun 2026 19:50:24 GMT  
		Size: 29.4 MB (29425991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb8e4e14f04edd8938045888f0dcf5b5544328fd4edfc6dbfa43dbca231990b`  
		Last Modified: Mon, 22 Jun 2026 19:50:23 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5166e13ef6df18a6bd1034c377f41a2dd4ae80127c6bd4573cf8800754da3fc`  
		Last Modified: Mon, 22 Jun 2026 19:50:23 GMT  
		Size: 22.3 KB (22303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine3.23` - unknown; unknown

```console
$ docker pull php@sha256:57bd7cbaf53599e2f0c84517b404a4cb7a0480801abcf1fbcb5039ec00522411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 KB (296512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74897fc2a2540109f83c6f4a2df8cee621e25475a09f40def8cf5765f5d1aaf0`

```dockerfile
```

-	Layers:
	-	`sha256:46a5284789c963c14f17b75ad1f25ebcd67fc1d88100faf7358ca6ba3f329f56`  
		Last Modified: Mon, 22 Jun 2026 19:50:23 GMT  
		Size: 259.2 KB (259222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b76d621f069a827585b32444cf00fb99804fc16ca66fe464e84c2f029d467455`  
		Last Modified: Mon, 22 Jun 2026 19:50:23 GMT  
		Size: 37.3 KB (37290 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine3.23` - linux; ppc64le

```console
$ docker pull php@sha256:4484e41be7ba606e249adbabc456421d4dc824d2e6e13611c46e1c0d29d27901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50952320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62609bb5393c95b3c70a8e7346e973343657b9596d9247efe83f2ffe80a42c2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jun 2026 19:55:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 22 Jun 2026 19:55:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 22 Jun 2026 19:55:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jun 2026 19:55:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 22 Jun 2026 19:55:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:55:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:55:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jun 2026 19:55:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 22 Jun 2026 19:55:46 GMT
ENV PHP_VERSION=8.5.7
# Mon, 22 Jun 2026 19:55:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Mon, 22 Jun 2026 19:55:46 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Mon, 22 Jun 2026 19:55:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 22 Jun 2026 19:55:52 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:07:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 22 Jun 2026 20:07:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:07:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 22 Jun 2026 20:07:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 22 Jun 2026 20:07:55 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1c2b8ee17956f259bd90745e13528ff9e462e59d64a1ed6ee0c1189527c623`  
		Last Modified: Mon, 22 Jun 2026 20:01:58 GMT  
		Size: 3.6 MB (3640684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1b6c964853f49997526f30758b273165c99348dfc22cc1c2fafb34d7e98af0`  
		Last Modified: Mon, 22 Jun 2026 20:01:57 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a102c8fc5cb12dd9d7014a9062d35ec9f60b78b90449669541c0b50dd561db`  
		Last Modified: Mon, 22 Jun 2026 20:01:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d8248567f757005fe52972b2afaa430abbf1fef54ad1b4e3c2cb4d9f4533ed`  
		Last Modified: Mon, 22 Jun 2026 20:01:58 GMT  
		Size: 14.4 MB (14421102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad75f483b7c0359e4655c0a7f12c56399735f6c7e0123c4bd81efc7d9f9e0a1e`  
		Last Modified: Mon, 22 Jun 2026 20:01:59 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614b30619228beff52948f8a5e93ea129bb560dae3bceab66cf12b7f9d5a6c85`  
		Last Modified: Mon, 22 Jun 2026 20:08:17 GMT  
		Size: 29.1 MB (29051992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321420dd91260f52b717d05bfff244f044aa79461419a8c4d48e6a679f9a3e3b`  
		Last Modified: Mon, 22 Jun 2026 20:08:16 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0021164fb2b60fe178c124a636a7c32b4dbb5c6b5522c1f3efa91e0e7306ccf`  
		Last Modified: Mon, 22 Jun 2026 20:08:16 GMT  
		Size: 22.2 KB (22155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine3.23` - unknown; unknown

```console
$ docker pull php@sha256:644276f49158174565c172cd01b57c66c1907361d7e7d1544498e3fb84f8f977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.0 KB (293027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5113c24a5850eea1a5e57f0b8ea2adb7115b8c08c420a56c1c2c0e8b601c4b79`

```dockerfile
```

-	Layers:
	-	`sha256:5a20e3c25a5b4847571ac79546c74a491f4c99b03137e47d54f9c81a9551d649`  
		Last Modified: Mon, 22 Jun 2026 20:08:16 GMT  
		Size: 255.6 KB (255640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a34353a80d2b8f06d9831eb603ff09efc821ada2447d6378a46ba6a8f3853c7`  
		Last Modified: Mon, 22 Jun 2026 20:08:16 GMT  
		Size: 37.4 KB (37387 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine3.23` - linux; riscv64

```console
$ docker pull php@sha256:070be3d478938d000f31db07ecb922905818ced795db7681f9730c5ad566e43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48297658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b96ebdf45ad49b80192eb62c0ba0fb040778cc086f9ee5e998adeded03df73`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 22 Jun 2026 19:30:17 GMT
ADD alpine-minirootfs-3.23.5-riscv64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:30:17 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 21:37:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jun 2026 21:37:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 22 Jun 2026 21:37:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 22 Jun 2026 21:37:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jun 2026 21:37:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 22 Jun 2026 21:37:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 21:37:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 21:37:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jun 2026 21:37:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 22 Jun 2026 21:37:25 GMT
ENV PHP_VERSION=8.5.7
# Mon, 22 Jun 2026 21:37:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Mon, 22 Jun 2026 21:37:25 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Mon, 22 Jun 2026 21:37:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 22 Jun 2026 21:37:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 23 Jun 2026 00:47:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 23 Jun 2026 00:47:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 23 Jun 2026 00:47:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 23 Jun 2026 00:47:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 23 Jun 2026 00:47:06 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:8a1e5860a6401101356d3688f519ef896539fceeb0e505b24a7224fe7e76fdb1`  
		Last Modified: Mon, 22 Jun 2026 19:30:41 GMT  
		Size: 3.6 MB (3573240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb42bea68a2af79d3ab5c7d97b0d79df81a465d93a9d7af266e102c3724bb82`  
		Last Modified: Mon, 22 Jun 2026 22:40:47 GMT  
		Size: 3.6 MB (3605582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88f0e7707ae583d6042075063a4c05b2191916232960e9aa4f37a61bde64b0a`  
		Last Modified: Mon, 22 Jun 2026 22:40:46 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a793f7413b68510356f0ff3df3c37f19645827c4d4847cff60fbdcf56de075be`  
		Last Modified: Mon, 22 Jun 2026 22:40:46 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf71615d818600295929d25343ae0e967e94e4a94700932e8227926ad6c07e1`  
		Last Modified: Mon, 22 Jun 2026 22:40:50 GMT  
		Size: 14.4 MB (14421117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba93106dabfd05a46c05e0abe10fe20c7d47040ed6962da905127e7fad6a3ff8`  
		Last Modified: Mon, 22 Jun 2026 22:40:48 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a81a8718cab1c4d8373d6548fddd64c1fb70c5a66099de21c9543d1674d65a`  
		Last Modified: Tue, 23 Jun 2026 00:48:23 GMT  
		Size: 26.7 MB (26671481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b90919e7707674f443f6072478e8262b7bc08fec2b18d4354a76ad7fcedbaa`  
		Last Modified: Tue, 23 Jun 2026 00:48:19 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f962145e14a6c83a5a7d99e0883e655d573109d67ca82d0abd7380f716303682`  
		Last Modified: Tue, 23 Jun 2026 00:48:19 GMT  
		Size: 22.1 KB (22149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine3.23` - unknown; unknown

```console
$ docker pull php@sha256:9d59e95f6c96a7d2a0e4d99d8a7dfc09f6755f4855d8a73c3e14f15f442a57fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.0 KB (293023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5439fe96c8ca7cb538c0456742b0b80633b99f0b97d342472835f2c50cd48fdc`

```dockerfile
```

-	Layers:
	-	`sha256:0b2caacbcb327ce3636117a02571eefc674de57a81edd2b686fae14f30b56896`  
		Last Modified: Tue, 23 Jun 2026 00:48:19 GMT  
		Size: 255.6 KB (255636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:069564bc7b76fb3caca962c694bef3d20b6cc2a12206d5191f4c7a6157d60807`  
		Last Modified: Tue, 23 Jun 2026 00:48:19 GMT  
		Size: 37.4 KB (37387 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine3.23` - linux; s390x

```console
$ docker pull php@sha256:d8481f544e33e83cc0f567740409aae578a628b28ee4a6e768214765f89f3fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49465507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32012a38fc18ebd5aef3332d62b017a34ec5a745e32f2b6f06b15ddf1014062d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:47:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jun 2026 19:47:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 22 Jun 2026 19:47:23 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 22 Jun 2026 19:47:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jun 2026 19:47:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 22 Jun 2026 19:47:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:47:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jun 2026 19:47:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jun 2026 19:47:23 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 22 Jun 2026 19:47:23 GMT
ENV PHP_VERSION=8.5.7
# Mon, 22 Jun 2026 19:47:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Mon, 22 Jun 2026 19:47:23 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Mon, 22 Jun 2026 19:58:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 22 Jun 2026 19:58:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:03:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 22 Jun 2026 20:03:11 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:03:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 22 Jun 2026 20:03:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 22 Jun 2026 20:03:12 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720364b97424794225edcbe5cc981444a6cded22d12d35f9d0472a9da0f26d40`  
		Last Modified: Mon, 22 Jun 2026 19:52:25 GMT  
		Size: 3.7 MB (3654456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e10377bf9f4e2b226a5bf70c6c8138d3d5ca33cb5aae50ef1c1b0df9e22c636`  
		Last Modified: Mon, 22 Jun 2026 19:52:25 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ad03e12eed7fbcede3ede1390f457cde57bdfe7a6f83e2eaf41500123e841c`  
		Last Modified: Mon, 22 Jun 2026 19:52:25 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3d67fb7a50bb1c0fa3ab40532a6d7286ce50273e3bfb1eba890500d5e84428`  
		Last Modified: Mon, 22 Jun 2026 20:03:26 GMT  
		Size: 14.4 MB (14421107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db916887f3ecb0f36b10fe54e782ce02110864be78cd348ae31bbec2cc5bb69a`  
		Last Modified: Mon, 22 Jun 2026 20:03:26 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d53864f61df705c64c22209fffe31ec4a0634508f79a8cce15235b65126ecb7`  
		Last Modified: Mon, 22 Jun 2026 20:03:27 GMT  
		Size: 27.7 MB (27656443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7db4872c2eac12c09fd381f6911d80f1de8ba861ffe47e764779b5ddbdc561d`  
		Last Modified: Mon, 22 Jun 2026 20:03:26 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45838994651462555ebd7cf7a082a7fb07e6a6235cdf419dd1e6a950f02427f`  
		Last Modified: Mon, 22 Jun 2026 20:03:27 GMT  
		Size: 22.2 KB (22157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine3.23` - unknown; unknown

```console
$ docker pull php@sha256:c8e9b43af7e984a9e6fae96584d43fcf97571758aac1a96496658271667ee719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 KB (292939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d1f1faeb55db3c466e8d2c6de38cc39259c416a7bdbd08e9f9905c40e14512`

```dockerfile
```

-	Layers:
	-	`sha256:7175ab4c56c2857368f71f2cec2785508acb2217d2aaa88f5406696b829c0287`  
		Last Modified: Mon, 22 Jun 2026 20:03:26 GMT  
		Size: 255.6 KB (255606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52b788b66096b9ebf9e5f0c9d5d7a5861686baf9909b7fe7e90078e42cdca1a5`  
		Last Modified: Mon, 22 Jun 2026 20:03:26 GMT  
		Size: 37.3 KB (37333 bytes)  
		MIME: application/vnd.in-toto+json
