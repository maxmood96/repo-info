## `php:8-zts-alpine`

```console
$ docker pull php@sha256:eb91c2072ed1c751c344805ecdeb3f6ac4255d6c5e6c60ad4187651b1a2baf60
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

### `php:8-zts-alpine` - linux; amd64

```console
$ docker pull php@sha256:ba31624492bac7ae5ee4bd26d50a4192efa4033aab8aec3738bb8b964615035f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47374044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf3ff2b76d0fb4046cecf23566a5cc7e8bb82270817eb052f9e6529603f81ef`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 10 Jun 2025 17:24:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 10 Jun 2025 17:24:03 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_VERSION=8.4.8
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/4c7220322bc74b0fc8416e1958cadd7bc51fe1b7.diff?full_index=1' -o 18743.patch; 	echo 'a19e795b24c52d4d1aa3d45b67339e1b62a5365b37cf4418b83e2709fc98bcb5 *18743.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 18743.patch | patch -p1; 	rm 18743.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 10 Jun 2025 17:24:03 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4798648b57845cf7d300c18c1e6d8f616348861d965a44fccf0047e03f5460f`  
		Last Modified: Wed, 11 Jun 2025 01:35:53 GMT  
		Size: 3.5 MB (3468416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc705559c23601ee17e1bd3843c7a0fd71ec30a5522fd3cd4b74d9c4e8a0117`  
		Last Modified: Wed, 11 Jun 2025 01:36:02 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fed6c44a57edcbca39a326a75fabfcf376d3e82901cb525cc952d19892499f`  
		Last Modified: Wed, 11 Jun 2025 01:36:05 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8878eb48ee79edc19442653b5f76c4c3e3a61dbc831952f878d84aa33acd4a00`  
		Last Modified: Wed, 11 Jun 2025 02:15:13 GMT  
		Size: 13.6 MB (13640523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ae7f3c6786d48103e5a184e20c1fc0b9230e0e801b4ce13264552dccf4bd9d`  
		Last Modified: Wed, 11 Jun 2025 01:36:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b5476811ad04802a112f6bb8fb8c998a85802e450430fa7d1ef960a5d93775`  
		Last Modified: Wed, 11 Jun 2025 02:15:15 GMT  
		Size: 26.4 MB (26443970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d01eee3b9aa684cb7f08008808850641f46e3cd2608be9f0cb2a65ff8f731e5`  
		Last Modified: Wed, 11 Jun 2025 01:36:12 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228e1dec2082fc5ade75b276269ba0cf21cda9f670cb0f4a266454f8f926b207`  
		Last Modified: Wed, 11 Jun 2025 01:36:14 GMT  
		Size: 20.2 KB (20204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine` - unknown; unknown

```console
$ docker pull php@sha256:8eb88492e686611602fac21265a9b99a01bc6c3e58cad01f5e9488a6d22a78aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 KB (322319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d677e54fec00c9b6c9b2c5102e559d73337cc5aa4868950f434a9425b72e67c0`

```dockerfile
```

-	Layers:
	-	`sha256:dd997cf42035ca11cceb21f50289e402f89ff1fe31567be7e6a7a03642ba2683`  
		Last Modified: Wed, 11 Jun 2025 01:57:39 GMT  
		Size: 282.5 KB (282479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f0674d87ec7d13be7310781b6c54c50bd45545658eacd00522287e841f9d94`  
		Last Modified: Wed, 11 Jun 2025 01:57:39 GMT  
		Size: 39.8 KB (39840 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine` - linux; arm variant v6

```console
$ docker pull php@sha256:e269042b91580c27522475d30704dbd232314d43dcb2a342aba76453cff9e9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44922792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b305ce4a5573151cb4a6fc5819711a170fbd880d41e059490c523e855e7823`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 10 Jun 2025 17:24:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 10 Jun 2025 17:24:03 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_VERSION=8.4.8
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/4c7220322bc74b0fc8416e1958cadd7bc51fe1b7.diff?full_index=1' -o 18743.patch; 	echo 'a19e795b24c52d4d1aa3d45b67339e1b62a5365b37cf4418b83e2709fc98bcb5 *18743.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 18743.patch | patch -p1; 	rm 18743.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 10 Jun 2025 17:24:03 GMT
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
	-	`sha256:a6e981f1a42ddcd50c334b14d2ded459d52bdf216813b664571b8f1b93ec56ba`  
		Last Modified: Wed, 11 Jun 2025 01:57:58 GMT  
		Size: 24.3 MB (24324831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d871aa7bcfc8858887ffbb23f69f859d53f1154eddca889df5ebb1cae765d929`  
		Last Modified: Wed, 11 Jun 2025 01:31:39 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed2b1b73a446aae828bf1338f1635c9ae57a4bc7bb904dff9ad20af6bf399b9`  
		Last Modified: Wed, 11 Jun 2025 01:31:42 GMT  
		Size: 20.0 KB (19988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine` - unknown; unknown

```console
$ docker pull php@sha256:68b10879de64d4157b9f25c463be3b0b3d2642bedaf10ae3f752ccc9fc64d95a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 KB (39797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19123c257d8fbb773ebb005c21674cb6b3460d5f7456fca53eddff969f9b164a`

```dockerfile
```

-	Layers:
	-	`sha256:0416eefbc1fa163b501ee0598c77386c38fc6b795481a72a303d5f85c6f479dc`  
		Last Modified: Wed, 11 Jun 2025 01:57:43 GMT  
		Size: 39.8 KB (39797 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine` - linux; arm variant v7

```console
$ docker pull php@sha256:e2a0375da8367ee598aabd1845f0ce26e64d97e255c5357b01f7ea5395a95554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43567655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fec5d6ea5350e0fbe28ac8db11722c7b2e3c004eb0b93dd076906024aca1394`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 05 Jun 2025 23:47:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Jun 2025 23:47:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_VERSION=8.4.8
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Jun 2025 23:47:13 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f58037841180f7071b0cb17f16a917752d43e658ee1f1d1590b910d941697a3`  
		Last Modified: Fri, 14 Feb 2025 21:49:05 GMT  
		Size: 3.1 MB (3120400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03b42d7db9fed02f8be351555a7c1cb492e5de9aeba350f89727c645ea19994`  
		Last Modified: Fri, 14 Feb 2025 21:49:04 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9997ea5283ca84c2230478f14c34317ce0e2df8d2463a0535910174e4ed66809`  
		Last Modified: Fri, 14 Feb 2025 21:48:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6e389261b9c64b81e91f5a16347a7d45abc12e8f8be41e35d9d667607c4416`  
		Last Modified: Fri, 06 Jun 2025 21:10:57 GMT  
		Size: 13.6 MB (13640356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0affa11432fa3e90bc1ff3b1972f85eeb1fe87eea39abbb4936e184cf2faf79`  
		Last Modified: Fri, 06 Jun 2025 18:38:24 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f707d0d3768ee955e16b18e4b3a04705d3c464cade633a7c751133cebdcef4`  
		Last Modified: Fri, 06 Jun 2025 18:32:50 GMT  
		Size: 23.7 MB (23684809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d31afcd4a5de0cdf8e2726e994db9b352e33d746ef5853ef4da9c0a32882865`  
		Last Modified: Fri, 06 Jun 2025 18:32:50 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8305e3e68504f8786de3b46aaef59e9812bd369e22ac30d61a7b37887cf557f`  
		Last Modified: Fri, 06 Jun 2025 18:32:50 GMT  
		Size: 19.9 KB (19871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine` - unknown; unknown

```console
$ docker pull php@sha256:acf2edc6d52a05ea804cc27237ae8bfcda3646b4a05596c1d3b7d626030c972a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 KB (308618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41f32bde30183c63623670390d5f2bb7637459faeb51ec9a533ac8bf61a1a1c7`

```dockerfile
```

-	Layers:
	-	`sha256:23c99dc453b6eb425aec251b36dd71a2c5071bfde1cefcc87fbf955b58869cef`  
		Last Modified: Fri, 06 Jun 2025 19:59:50 GMT  
		Size: 269.9 KB (269933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b30ff4e8b9ec9c5b746ec72502e3f856287ec884ec67a80bb38b7a7742aeef1`  
		Last Modified: Fri, 06 Jun 2025 19:59:50 GMT  
		Size: 38.7 KB (38685 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine` - linux; arm64 variant v8

```console
$ docker pull php@sha256:5c46e6f6c60ced9035a41efe98ce160f314afaffa046fb981c1dd435db823b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47273264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51203008bc9d0f16558e4e2d992da96eb7122379f2ccc9ee306f7e25cc820bf1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 10 Jun 2025 17:24:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 10 Jun 2025 17:24:03 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_VERSION=8.4.8
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/4c7220322bc74b0fc8416e1958cadd7bc51fe1b7.diff?full_index=1' -o 18743.patch; 	echo 'a19e795b24c52d4d1aa3d45b67339e1b62a5365b37cf4418b83e2709fc98bcb5 *18743.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 18743.patch | patch -p1; 	rm 18743.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 10 Jun 2025 17:24:03 GMT
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
	-	`sha256:1c2eb39f0cb5bcdea2b3e83501747c1e38c6f571f44d4c8d84f6e1274d336677`  
		Last Modified: Wed, 11 Jun 2025 09:17:18 GMT  
		Size: 26.0 MB (26002060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4449c6f95bb53dc8785d364ec63a6682da133ab863aa27f04f7fffab20d2714`  
		Last Modified: Wed, 11 Jun 2025 09:17:09 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96366ecb7b8991896504a3459327bed131dc6ec61e32ba66b09a8ac4e8305d64`  
		Last Modified: Wed, 11 Jun 2025 09:17:14 GMT  
		Size: 20.0 KB (19989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine` - unknown; unknown

```console
$ docker pull php@sha256:f84d0454177daf65b86a20f0dad87d754f3c2e97ebac19e94e4ff6e418a7e873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.7 KB (319659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357dfe07f2689c82e1faf19a401a2c7e87ba880eb48df0bebeade0efd972a34b`

```dockerfile
```

-	Layers:
	-	`sha256:68266ceec38c9bd81c79739d3949832d2680db1c6cb043d106399b686eac28fd`  
		Last Modified: Wed, 11 Jun 2025 10:55:18 GMT  
		Size: 279.6 KB (279593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec655d8999c809b867360ba3380980d77b1b043b5e7d60dba78d51c425db0bf5`  
		Last Modified: Wed, 11 Jun 2025 10:55:19 GMT  
		Size: 40.1 KB (40066 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine` - linux; 386

```console
$ docker pull php@sha256:78b70f90da481411c42aa3ca1dda7e237807a166a8154218a40af6caef414cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47841373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5940607f3785e89bf30a855baa38aadedc7691839f815a3138fada24e2c1763b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 10 Jun 2025 17:24:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 10 Jun 2025 17:24:03 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_VERSION=8.4.8
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/4c7220322bc74b0fc8416e1958cadd7bc51fe1b7.diff?full_index=1' -o 18743.patch; 	echo 'a19e795b24c52d4d1aa3d45b67339e1b62a5365b37cf4418b83e2709fc98bcb5 *18743.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 18743.patch | patch -p1; 	rm 18743.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 10 Jun 2025 17:24:03 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00df2b5b2976118186517a0201b5b62445b7e62fcacd65387885f604d76651d9`  
		Last Modified: Wed, 11 Jun 2025 03:36:09 GMT  
		Size: 3.5 MB (3527689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15211ce515864d7679e6f97626b8bfbb0275689087ad6bbbec0d2b2d3493651`  
		Last Modified: Wed, 11 Jun 2025 03:36:09 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a612570992fab43cc15fbc1f12387547f97ed461a91f7c451dc2d9efd26ea9`  
		Last Modified: Wed, 11 Jun 2025 03:36:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2cc968d8b2939de656580fc99e99a27b492f65bce1e309c11f3dacfc9800b38`  
		Last Modified: Wed, 11 Jun 2025 03:36:10 GMT  
		Size: 13.6 MB (13640487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42313de2b5cda73fb8efb7f4ba2c48ab42a1ce14313c2c98a70fa66fbd0f4779`  
		Last Modified: Wed, 11 Jun 2025 03:36:10 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5168bcf6b71ffab5ba57a132cdbe79c5e52ec0d508c5ab666f58ea00074a56da`  
		Last Modified: Wed, 11 Jun 2025 03:36:12 GMT  
		Size: 27.0 MB (27032897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71831b6c4062271689a01f8dee02470c7908ac94e13c486a04524bf4c853927e`  
		Last Modified: Wed, 11 Jun 2025 03:36:11 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446180f5007b7f4e5e222b612c235752552bb0d23ccfbd0aeb43b45bc3daa26f`  
		Last Modified: Wed, 11 Jun 2025 03:36:10 GMT  
		Size: 20.2 KB (20188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine` - unknown; unknown

```console
$ docker pull php@sha256:52f824cc8fcc0d50778ef7951022e69dac1e89a8fa50c04c0c1f8062dc67f130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 KB (322212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2819adbfcef4fbcdae3cabed0816ad7d5c1781993f02e1d9055eb008ec729349`

```dockerfile
```

-	Layers:
	-	`sha256:a9c40a37845baf0fe563f4a7128196059f584f0987571f630b55850f0ef4dc4e`  
		Last Modified: Wed, 11 Jun 2025 01:57:48 GMT  
		Size: 282.4 KB (282434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:526c9ebad476540917b6e0369e7954f61e19e00ffa2924cf6e711016dfe621e7`  
		Last Modified: Wed, 11 Jun 2025 01:57:49 GMT  
		Size: 39.8 KB (39778 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine` - linux; ppc64le

```console
$ docker pull php@sha256:a414ab198b6a31522750e0d7cdbd8e9eb13ca113555458249f89a71f595e75fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48788707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ecffba8dac7cbe7f50cf66f3d2d576899444c6373f5d575f3316754e6dbe03b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 10 Jun 2025 17:24:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 10 Jun 2025 17:24:03 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_VERSION=8.4.8
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/4c7220322bc74b0fc8416e1958cadd7bc51fe1b7.diff?full_index=1' -o 18743.patch; 	echo 'a19e795b24c52d4d1aa3d45b67339e1b62a5365b37cf4418b83e2709fc98bcb5 *18743.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 18743.patch | patch -p1; 	rm 18743.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 10 Jun 2025 17:24:03 GMT
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
	-	`sha256:07f003fff40f6d4e441b8a97f6552e86d4f3dcef9dee01628a511467d4978d0a`  
		Last Modified: Wed, 11 Jun 2025 11:21:33 GMT  
		Size: 27.8 MB (27774781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d129b785da7d8bb8152005d577b06875dbdd33e72610d3edccb08e927873b122`  
		Last Modified: Wed, 11 Jun 2025 09:24:17 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1740901bd7de654ee7951e51e609d8996186859eea42376c887564439d067a22`  
		Last Modified: Wed, 11 Jun 2025 11:21:29 GMT  
		Size: 20.0 KB (19998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine` - unknown; unknown

```console
$ docker pull php@sha256:0b202bc85bc19b68619af8e8e96503e22962263c02b15783a134e75556034a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 KB (317514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cee1c26116f66bae0979901e7b9ea44e1c1e099ffcff9e6092f74859dea7a58`

```dockerfile
```

-	Layers:
	-	`sha256:4f0b0715c615d6b1146c1cb04b7687947254579916c30d314fd82d0aca5f4770`  
		Last Modified: Wed, 11 Jun 2025 10:55:25 GMT  
		Size: 277.6 KB (277596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5911134035c5bf0f5f90dabfabf65523399d2b08ae27b6146692253d87faa33d`  
		Last Modified: Wed, 11 Jun 2025 10:55:25 GMT  
		Size: 39.9 KB (39918 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine` - linux; riscv64

```console
$ docker pull php@sha256:30d9b089432e5cc2266ef4803e2a1932bcffa055f24a6541b11f6b4ce79c23ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46758934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abdcc4832a54e67c00d11bff610c6a0e018b4ff82ca87ffab8e67e4713a19ccf`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 10 Jun 2025 17:24:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 10 Jun 2025 17:24:03 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_VERSION=8.4.8
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/4c7220322bc74b0fc8416e1958cadd7bc51fe1b7.diff?full_index=1' -o 18743.patch; 	echo 'a19e795b24c52d4d1aa3d45b67339e1b62a5365b37cf4418b83e2709fc98bcb5 *18743.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 18743.patch | patch -p1; 	rm 18743.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 10 Jun 2025 17:24:03 GMT
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
	-	`sha256:761c1648e90aaea1cff38da5474b18012fb17b7780bb0144ded4f0ea122e991a`  
		Last Modified: Wed, 11 Jun 2025 10:52:13 GMT  
		Size: 26.0 MB (25977176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85985ce99a88124c1776bf8e704b7aff82c1fcab884eb15c2761b0047d368431`  
		Last Modified: Wed, 11 Jun 2025 04:42:55 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095bd3e963a606deb3693bdc2d1ae2faf099b85a1814f3dc594c167333067b08`  
		Last Modified: Wed, 11 Jun 2025 04:42:58 GMT  
		Size: 20.0 KB (19996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine` - unknown; unknown

```console
$ docker pull php@sha256:2ec0e636381ce857dd20fa0f143cf525614d13d9bbff8fbd2a943b7137368b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 KB (317510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef29157d970d69d84925bc1b1571fa9fb563c9af70898a7d5293db0fd73b315`

```dockerfile
```

-	Layers:
	-	`sha256:d8f31ddce21c90983cb36d955a1c115de73094f6b0f2e72234a7e9ba2a63c8dc`  
		Last Modified: Wed, 11 Jun 2025 07:55:14 GMT  
		Size: 277.6 KB (277592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4e92cf1164b2d0e732da96bbd8298146b9d2a509b585b95800137e6eea893ab`  
		Last Modified: Wed, 11 Jun 2025 07:55:14 GMT  
		Size: 39.9 KB (39918 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine` - linux; s390x

```console
$ docker pull php@sha256:5a3a3b30edb5c7560615d79aec9b87f01257eaba7ca08a6f2165db36a67f46cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48466421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7b20b59ff7c9456d9a974101d99a673de7ecbf1d85a1205dc326d2a5c3aeb1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 10 Jun 2025 17:24:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 10 Jun 2025 17:24:03 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_VERSION=8.4.8
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Tue, 10 Jun 2025 17:24:03 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/4c7220322bc74b0fc8416e1958cadd7bc51fe1b7.diff?full_index=1' -o 18743.patch; 	echo 'a19e795b24c52d4d1aa3d45b67339e1b62a5365b37cf4418b83e2709fc98bcb5 *18743.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 18743.patch | patch -p1; 	rm 18743.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 10 Jun 2025 17:24:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 10 Jun 2025 17:24:03 GMT
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
	-	`sha256:9b8cc96c86e494b678ab043e7f1b933d3f356bb87a04d2dcbcc7f59fb9744471`  
		Last Modified: Wed, 11 Jun 2025 10:52:12 GMT  
		Size: 27.5 MB (27455292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a6a38343bfb40ff546a64584bd6b57e1fbf2e51c56c363993068486b1d8b41`  
		Last Modified: Wed, 11 Jun 2025 06:23:31 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f1d90164824367b843992007b9be6d61c342ea593b1a6cc35a8a554c535bde`  
		Last Modified: Wed, 11 Jun 2025 06:33:09 GMT  
		Size: 20.0 KB (19996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine` - unknown; unknown

```console
$ docker pull php@sha256:ea3c55bd791fcd6343c01c6f70b537c15ed3e28fc3ef308d4f5e5413ec8ea893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.4 KB (317377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556e247309aa677622789d6b7c3aa264ddb60fb88c3c372a0b951e7377131869`

```dockerfile
```

-	Layers:
	-	`sha256:71c180cc4b1587c23398f166c37c227211281123bd4546f4514a9c6490e348ef`  
		Last Modified: Wed, 11 Jun 2025 07:55:18 GMT  
		Size: 277.5 KB (277538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ee6d4219a5b2ead166e1f0d686462b51d37af9cf6bb419da3051faf8386e9db`  
		Last Modified: Wed, 11 Jun 2025 07:55:19 GMT  
		Size: 39.8 KB (39839 bytes)  
		MIME: application/vnd.in-toto+json
