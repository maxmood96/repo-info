## `php:zts-alpine`

```console
$ docker pull php@sha256:2eb19f82dba4f2cb6002e3a7b7797d1d95565c6dcbdc2b7427af5d5b677f68bc
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

### `php:zts-alpine` - linux; amd64

```console
$ docker pull php@sha256:2912f689997e04a0476485fe30a9d8e371b918e58e8d068971d28909b654b373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49015609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0217c1976d21af3084a9f2991c16f3875b002085a0a38bcf607805c38538d4df`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 21 Nov 2024 14:39:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 14:39:47 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_VERSION=8.4.1
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 14:39:47 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85925b28662551b12a9eb124d8448c0d8e073a6751a0a2471018eed172aee69a`  
		Last Modified: Thu, 21 Nov 2024 18:00:43 GMT  
		Size: 5.6 MB (5583590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35040ad6d8b1d6b6c74eef3db3caf2831c3a469e6204132806ea50a4fe4d2873`  
		Last Modified: Thu, 21 Nov 2024 18:00:42 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b79aebd2e2f021efa3567b336821458f74ba83bfa3eb253ddace199b7c12b8`  
		Last Modified: Thu, 21 Nov 2024 18:00:42 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b292627c2ca818075cb1cb528721cfd0e8a7e2276725a7b6747aa14e6348bc`  
		Last Modified: Thu, 21 Nov 2024 18:00:43 GMT  
		Size: 13.6 MB (13572759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63379815975575eb817ea2b2279b6bfa7c7ba77efe8453089081afd27f88a9e`  
		Last Modified: Thu, 21 Nov 2024 18:00:43 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300dc6ddf0bdb13614ab24b312c437fae39d547a376ed71f49aa237bba6cd15b`  
		Last Modified: Thu, 21 Nov 2024 18:00:44 GMT  
		Size: 26.2 MB (26211603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d060acedef12ad44d98e74f75018487aaf6dbbc18d22bcc2eca396f6151db684`  
		Last Modified: Thu, 21 Nov 2024 18:00:44 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d369887f1a2f410ef5e08eda9bc1b6ea6b1b01d3110101e5caeb9071307cd3`  
		Last Modified: Thu, 21 Nov 2024 18:00:44 GMT  
		Size: 19.7 KB (19661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine` - unknown; unknown

```console
$ docker pull php@sha256:22845e61bce49843f031c23a1f7296854d41857c3c7c90dc8652e1e684f86952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 KB (301845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c38ce335c27c6da118150870b11918040b57063a9a977933cbb82f6b417a53`

```dockerfile
```

-	Layers:
	-	`sha256:90e61ee14a7e01aa28c5c252db5facb3b5b704d5b1bc2a143967c4d9fc1e7a27`  
		Last Modified: Thu, 21 Nov 2024 18:00:43 GMT  
		Size: 263.3 KB (263333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeddcf0925634a862ba55da94d08caf8ad3e3b44dc5b9610c2f351174a8eb91a`  
		Last Modified: Thu, 21 Nov 2024 18:00:42 GMT  
		Size: 38.5 KB (38512 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine` - linux; arm variant v6

```console
$ docker pull php@sha256:d611b5d10c4612066d626775bb73dc5769168c596e253900c98bdbf794f66b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46473999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f671ebfc0486445159103e3fcfc5ca10698872840d8afdba276f96dc169d2891`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 21 Nov 2024 14:39:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 14:39:47 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_VERSION=8.4.1
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 14:39:47 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdae56950198dea1248e6f62d7e9ef311c976d55790449240dfa46ad43351f7`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 5.2 MB (5236002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773d98c98ade13dc692eaf9700be32a03220033d99905be410eda923ce054fb9`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ae964d3deb57dca49dadfc5c487d64a372e3df3db6ef51b58087c318beb33d`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851605dfb3d928a53fef3860db97edb0f94316d382df472a9f36d31603ae85dc`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 13.6 MB (13572750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb476219577608ba4633ce4f2bf10a95d8fd1bd1bb56c2fb972587e5207cb3f`  
		Last Modified: Thu, 21 Nov 2024 17:58:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c90893b1eba200acce37b6756966367156a26b8cb8cacb555a38d057a9c66a2`  
		Last Modified: Thu, 21 Nov 2024 18:05:49 GMT  
		Size: 24.3 MB (24275105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d1e9c50dd0a4e03b9152bc86072ae430c8213fb1a6e0d0dbaa0fc0a33bea9e`  
		Last Modified: Thu, 21 Nov 2024 18:05:48 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afc26363854be94c47749677c086839e5b57071849249e319738ceb75d60e2e`  
		Last Modified: Thu, 21 Nov 2024 18:05:48 GMT  
		Size: 19.4 KB (19438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine` - unknown; unknown

```console
$ docker pull php@sha256:681d53370d1064745fee47ca4efeb741cd1d2290447215b64f88b10e7065f8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 KB (38470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3900f7c4b531e5d2e6cca38b695053663a43bac4e458566ec7d66699e37a233`

```dockerfile
```

-	Layers:
	-	`sha256:dcc6fca9a91e1823c6d73bf328b4e0cc55066b8a3cc793988e2a201596d2d3ac`  
		Last Modified: Thu, 21 Nov 2024 18:05:47 GMT  
		Size: 38.5 KB (38470 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine` - linux; arm variant v7

```console
$ docker pull php@sha256:9509854db42050407d0e0d878fa333ff5941c4cf099b88d6f643b9fad4260b6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 MB (44427649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4eb1b584e9a6f14996946e667d2598e9c5618bb559a3bb7f51b421c390b20f9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 21 Nov 2024 14:39:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 14:39:47 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_VERSION=8.4.1
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 14:39:47 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2878563f55378e5cb0d2e6fc051acec0bad59706b4c55d991502e489d45f15b9`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 4.9 MB (4894482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1da599409a1b1b855c6d69889b78470128711398dd127ceb61f803c590c9c39`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fec221aedc472ddb77d24345957296ec946aab0b124953af99b1b103ca464d6`  
		Last Modified: Tue, 12 Nov 2024 03:55:37 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46d0dd0a80f3bfa93fe376e12f14d3cf1bf7c86c9c039106b233b8584ec9aac`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 13.6 MB (13572743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d138265234b8809a223e845ff20a559fa757eebafc98f9e9bf724fe8e7dc8b6c`  
		Last Modified: Thu, 21 Nov 2024 18:28:27 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5602229b9d6255ceb7b85b99698a17720c76f214722d68749b3f689864696f`  
		Last Modified: Thu, 21 Nov 2024 18:35:44 GMT  
		Size: 22.8 MB (22841385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e1c059534584e71189da6addcd7871a66b05ed2dada184623d831e916fb75e`  
		Last Modified: Thu, 21 Nov 2024 18:35:43 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07bc1d513b3d1dd4aafeaa415693129fe2fc44b0ff113a05cbc90e8b0b54cc5`  
		Last Modified: Thu, 21 Nov 2024 18:35:43 GMT  
		Size: 19.5 KB (19452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine` - unknown; unknown

```console
$ docker pull php@sha256:64d2972cc6d29fefbe0c73253078eab8c193211d2f41fba4deea8150d30873a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.2 KB (299222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca8a86bb9146a5da69705abb467e235174a6796a3a92e23d1dbcd3470f9a785`

```dockerfile
```

-	Layers:
	-	`sha256:2573599d6a5e769e825f29b976473817ead2adae1cd1ba65068466c6e9cced77`  
		Last Modified: Thu, 21 Nov 2024 18:35:43 GMT  
		Size: 260.5 KB (260537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0780137740291cd6b6219c6053835791ff76b6e8ebcafdff2359356bd478cab6`  
		Last Modified: Thu, 21 Nov 2024 18:35:43 GMT  
		Size: 38.7 KB (38685 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine` - linux; arm64 variant v8

```console
$ docker pull php@sha256:52fb4c8607c4692cf0f69aebb46bd6bd775295cd9ebce0aeaec18260edf5d4b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49561869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8f23212d7c8ad23c4f832721b6a4df9a49196978f3f0f0226ac3a84ae2a60b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 21 Nov 2024 14:39:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 14:39:47 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_VERSION=8.4.1
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 14:39:47 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8484336630ebb870b45fd46b300831768da17cae91aa6a615fe97d849bf7d9`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 6.0 MB (6047382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f0bf50f7dfd6864235893d3a770f2748c511f29a319b959cd61ab88719f191`  
		Last Modified: Thu, 21 Nov 2024 18:25:40 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4094551f517548ba326fd9610784089231cb5fe7b32fb0fd484b4ef62a06ec4e`  
		Last Modified: Thu, 21 Nov 2024 18:25:40 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f3a19954028229594dc87f84401ff6bb04343f60f6850d3ffd56376584e127`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 13.6 MB (13572746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cec773ac8fce78f9e43c85101520fcc9a1dfd15d5ae6b0086a53ed446c44e83`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae671fe188a888830181d920997217a414d1c9da575740767682658701ce891`  
		Last Modified: Thu, 21 Nov 2024 18:33:07 GMT  
		Size: 25.8 MB (25830501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f88d7bc2a6d717866629025e78388291db78f597a97a4eafd36999dd1d865f`  
		Last Modified: Thu, 21 Nov 2024 18:33:06 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb8a9ea467c32eef1e121d3d2eaca36fb574baa9f29d0bd9ecf11cc907b0847`  
		Last Modified: Thu, 21 Nov 2024 18:33:06 GMT  
		Size: 19.4 KB (19423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine` - unknown; unknown

```console
$ docker pull php@sha256:1108fc11dfc32c58174bac9b7cd06255fd3eb577376b76db1e6c03e8110b0bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.3 KB (299312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c2cb614256773887557fa2274a2aedaf68cf1afb5e72c554644ebf5d8981c2`

```dockerfile
```

-	Layers:
	-	`sha256:328db2d79703e60eb38a95cdc3854ad9ab8891801c1052c11ff3581cfaba6378`  
		Last Modified: Thu, 21 Nov 2024 18:33:06 GMT  
		Size: 260.6 KB (260573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a123817493302e32278309ff2cde60f22b7982e05ac8b8c39de1e0f420dbb798`  
		Last Modified: Thu, 21 Nov 2024 18:33:05 GMT  
		Size: 38.7 KB (38739 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine` - linux; 386

```console
$ docker pull php@sha256:92bb3ca7f2a0bf455ad841d8c6b7535399102f45ae6e9349e1bfb4e7899548f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49358279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d6cde6173ef84158232b0ff9a91a540251b5d4be3517aa0882e8c88fdb0887`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 21 Nov 2024 14:39:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 14:39:47 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_VERSION=8.4.1
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 14:39:47 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092f282f13631d640f01821016c6ac37b0daa000185d7c67faa04d90462fa091`  
		Last Modified: Thu, 21 Nov 2024 18:00:47 GMT  
		Size: 5.5 MB (5468309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c212757052485b18f4c28a594ed6ef201474099774b854599014b223821bfeba`  
		Last Modified: Thu, 21 Nov 2024 18:00:46 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d72d855f24d23433acd99b1c0394c2e24d39b2d7d2863c1a3414a89512017f`  
		Last Modified: Thu, 21 Nov 2024 18:00:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8990dbe5885528646f1404f05d3a42e1324ebcfc9127710d1d19f253061a744c`  
		Last Modified: Thu, 21 Nov 2024 18:00:47 GMT  
		Size: 13.6 MB (13572749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725c3c7c3688e7b689c624b27bce8234e6d9043992400f02aa6f9dfb6c7db102`  
		Last Modified: Thu, 21 Nov 2024 18:00:47 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3988d0637aaa7f9bdfbbfa12ce47e7eae9dc1d3fc2da1d85ffc4e872f740023`  
		Last Modified: Thu, 21 Nov 2024 18:00:48 GMT  
		Size: 26.8 MB (26824268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2a012cf8af0d32f645358a017fa4e6e98540cc04c13f20f55a3e54d8e2eba7`  
		Last Modified: Thu, 21 Nov 2024 18:00:48 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6657d3e33e4bf0bd29968b72a918b4a22c2302649ff05b8d67e28bd0c56628`  
		Last Modified: Thu, 21 Nov 2024 18:00:48 GMT  
		Size: 19.6 KB (19639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine` - unknown; unknown

```console
$ docker pull php@sha256:527bf186ca26174c17ead4d6426c725d28c6d3090e96ca8e6b80fa13ab9a1a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.7 KB (301738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf93d89c5ee56aea5027e9e2d38d960eb1bfccb49f26b07f6856efaa374b9bce`

```dockerfile
```

-	Layers:
	-	`sha256:12d845ad2b5ea41e0addc5a66f755964880da2294adc8dcc416eb1f2e0cc51b6`  
		Last Modified: Thu, 21 Nov 2024 18:00:46 GMT  
		Size: 263.3 KB (263288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615a2faa346134777010306564a9355b44295ed3f6c5548ed06591fe2d489f0d`  
		Last Modified: Thu, 21 Nov 2024 18:00:46 GMT  
		Size: 38.5 KB (38450 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine` - linux; ppc64le

```console
$ docker pull php@sha256:d8ffad84752f08c3fb62921062efece6dbb0bb3fd809e4e148f9fc01f7f6a5db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50327439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e954205715236a59c4f6863df371efff6f3a9e4f495edeb38db112c73f2c1dcd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 21 Nov 2024 14:39:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 14:39:47 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_VERSION=8.4.1
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 14:39:47 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2473147d3bc2923a26c8ba560c425ef2674fbae2edbc29833bb5790c2c94db2`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 5.6 MB (5572572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53975073457162c05af82756884811d86cf52d05953b0589749a216a80864431`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58037573bd03f9687676a3398cb715ac628a3bc280f63aa990e8171ef59ce1c9`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f80183c138cedf9dc24420caf7f9769369bf61c8db0eb09729c4303c31ba1b`  
		Last Modified: Thu, 21 Nov 2024 18:14:28 GMT  
		Size: 13.6 MB (13572757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1746563bd5a8883ee2e1758e12423a999df46412bbeb663f9f774dc595e96ed`  
		Last Modified: Thu, 21 Nov 2024 18:14:27 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8728a2784d60613852a31b019eb16a2a64e074d075658e0a96a0f68a70839680`  
		Last Modified: Thu, 21 Nov 2024 18:21:37 GMT  
		Size: 27.6 MB (27586119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4468fa50bbef18becff1bb5225b9b3f18b2eeae9f4c54ffc1f9d88ca24c077fa`  
		Last Modified: Thu, 21 Nov 2024 18:21:35 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f534b9024bbb52c06e84a3d7618beefb869e3601d6672150f471748f75e29ad7`  
		Last Modified: Thu, 21 Nov 2024 18:21:35 GMT  
		Size: 19.4 KB (19425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine` - unknown; unknown

```console
$ docker pull php@sha256:3cb0c9644edebc0d93a095720e0d274c33705baeb6c97ae6dd679d0c48ac243d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 KB (297163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7fdc9ee53fa69b463deaf68e26fdca362f6ffb2914140d5dafc525f55bc480`

```dockerfile
```

-	Layers:
	-	`sha256:6749cd4fe5298248cd624a59ff10ec5169fe41e3ea50cba2bb397a19bcabc5ab`  
		Last Modified: Thu, 21 Nov 2024 18:21:35 GMT  
		Size: 258.6 KB (258573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fde65d4faf2024d002266f286516aea87701549ef25fc3f6ba015b257582520`  
		Last Modified: Thu, 21 Nov 2024 18:21:35 GMT  
		Size: 38.6 KB (38590 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine` - linux; riscv64

```console
$ docker pull php@sha256:7c6fc6197ba351b1fb9c9e40f4e02aff0ca51a4837bf6f0dc1a871e2edd0734a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42497621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190b8c4ffcefc89b5ead703736bef98078057ee14829c8dcf084c0191fff08c1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8ca85c9d20c6f76d0a8087ac3a4ddd6a1e40652d189dc8dad7ca6b0737c4b0`  
		Last Modified: Tue, 12 Nov 2024 06:14:49 GMT  
		Size: 5.4 MB (5382174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d2dfe107b4bddcc389bedcee9ca3fc81f02dc0799e313c21f307ddb454b4dc`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df7310166e795cb48e721a885b92af688db981613ad6597943011293aca738c`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626cc5aa152e22cd453ede74c922b963a3bc8a4bcf66d8a4763c977a36db9bbf`  
		Last Modified: Tue, 12 Nov 2024 11:38:11 GMT  
		Size: 12.5 MB (12504597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e68d6f9ff3ad2f5f92d5d2e1da7c8e8e8c7acf26714c65fb1634379b0ceabea`  
		Last Modified: Tue, 12 Nov 2024 11:38:08 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34144cc4a19545e1d893890fe190b569ed00cf288a728e650425e1d56b9b773`  
		Last Modified: Tue, 12 Nov 2024 13:21:16 GMT  
		Size: 21.2 MB (21215810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1008e3400de665ffc72859da0e398ab0f60a6edf5e2cf810af439263bae0fe16`  
		Last Modified: Tue, 12 Nov 2024 13:21:12 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb36189828194e237280e87d3982d83bf1581c4c6db29848d9a5a519a6e67d3a`  
		Last Modified: Tue, 12 Nov 2024 13:21:13 GMT  
		Size: 19.4 KB (19449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine` - unknown; unknown

```console
$ docker pull php@sha256:f4d13927aa5b798ffe67879616ba1eddc3df72a20ddf537093008c7c8620053d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 KB (297184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e7aafd78f88e6efb0dc5e05111ea0d4cfd68c1825ad00c7c101190df6b5e44`

```dockerfile
```

-	Layers:
	-	`sha256:c4707f6f7388695306105522f5089c57c18f467cd88e78897f68d3cff47f60bd`  
		Last Modified: Tue, 12 Nov 2024 13:21:13 GMT  
		Size: 258.6 KB (258577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22cd949da414aa68129f11f81c30ca00d4be79e7ae080f93da4f32cb96b7d46e`  
		Last Modified: Tue, 12 Nov 2024 13:21:12 GMT  
		Size: 38.6 KB (38607 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine` - linux; s390x

```console
$ docker pull php@sha256:e6ff0500e341c6537615b0d9c0208638d7bb055fa6da79fe8892ba9f3d04d8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49816675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccbdcf8b1085e4b8afde1c42283ba2cb6e7c725c492becc28d1450a7772d18ef`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 21 Nov 2024 14:39:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 14:39:47 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_VERSION=8.4.1
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 14:39:47 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26915a92034b18e2de9232a415d1ad92dc1c7a9f9e2b5bb9c590ce4c503ab73e`  
		Last Modified: Tue, 12 Nov 2024 03:39:27 GMT  
		Size: 5.5 MB (5532119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4041b6d620078267a8ee6dd6b9c31735d82dee5f22aa96467865a8134d616c`  
		Last Modified: Tue, 12 Nov 2024 03:39:26 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5555efb309fc5275c2fd44eabaaf4ca859f01b510ef24cbad6009d7ed6dc4696`  
		Last Modified: Tue, 12 Nov 2024 03:39:26 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ebcb70bd65f646a0a9f4f475ec50ab3b189c26c5453f7261bc927c566c16f4`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 13.6 MB (13572754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1fe669f736130225879d8f3a94b1a2dc84c8a542232c1010d5c0efdfb490ab`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fff3dcfbca713ea0de7c369ca07c39952857c8b02e205019cdfa62d9c81cf5`  
		Last Modified: Thu, 21 Nov 2024 18:32:30 GMT  
		Size: 27.2 MB (27226654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1180a1f89b48408bdb6f76b92078df6ea68a6dabad81fada2ed8473968ac96f5`  
		Last Modified: Thu, 21 Nov 2024 18:32:29 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e13d796071f2a676e39188d75ab1339d9001eb4193c89fddc70dd75ff1ed794`  
		Last Modified: Thu, 21 Nov 2024 18:32:29 GMT  
		Size: 19.4 KB (19440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine` - unknown; unknown

```console
$ docker pull php@sha256:d41631543d1cdbd555d75f1649e503c42929b4a12cf0fce95aa8ea1c290929e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 KB (297027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90082ff10a18e8f3c1d8412281ce77d013977eeb97269e58d4a48eeecbbc1a6`

```dockerfile
```

-	Layers:
	-	`sha256:96344eea6a942c81d69b7d087b7e5791aaf1ffb8021f9f688809c7968adf259a`  
		Last Modified: Thu, 21 Nov 2024 18:32:28 GMT  
		Size: 258.5 KB (258515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1178c3d7f3cb2892a25ecbe4bca98c922f99c9e39bb10fad5aa91b0147883e`  
		Last Modified: Thu, 21 Nov 2024 18:32:28 GMT  
		Size: 38.5 KB (38512 bytes)  
		MIME: application/vnd.in-toto+json
