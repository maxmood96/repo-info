## `php:8-zts-alpine3.22`

```console
$ docker pull php@sha256:77e00cead56fb2cbe763c35ad743943b200c697d3358b80b454d8c089de11664
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `php:8-zts-alpine3.22` - linux; amd64

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

### `php:8-zts-alpine3.22` - unknown; unknown

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

### `php:8-zts-alpine3.22` - linux; arm variant v6

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

### `php:8-zts-alpine3.22` - unknown; unknown

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

### `php:8-zts-alpine3.22` - linux; 386

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
		Last Modified: Wed, 11 Jun 2025 00:03:55 GMT  
		Size: 3.5 MB (3527689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15211ce515864d7679e6f97626b8bfbb0275689087ad6bbbec0d2b2d3493651`  
		Last Modified: Wed, 11 Jun 2025 00:03:55 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a612570992fab43cc15fbc1f12387547f97ed461a91f7c451dc2d9efd26ea9`  
		Last Modified: Wed, 11 Jun 2025 00:03:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2cc968d8b2939de656580fc99e99a27b492f65bce1e309c11f3dacfc9800b38`  
		Last Modified: Wed, 11 Jun 2025 00:03:55 GMT  
		Size: 13.6 MB (13640487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42313de2b5cda73fb8efb7f4ba2c48ab42a1ce14313c2c98a70fa66fbd0f4779`  
		Last Modified: Wed, 11 Jun 2025 00:03:55 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5168bcf6b71ffab5ba57a132cdbe79c5e52ec0d508c5ab666f58ea00074a56da`  
		Last Modified: Wed, 11 Jun 2025 00:03:56 GMT  
		Size: 27.0 MB (27032897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71831b6c4062271689a01f8dee02470c7908ac94e13c486a04524bf4c853927e`  
		Last Modified: Wed, 11 Jun 2025 00:03:56 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446180f5007b7f4e5e222b612c235752552bb0d23ccfbd0aeb43b45bc3daa26f`  
		Last Modified: Wed, 11 Jun 2025 00:03:56 GMT  
		Size: 20.2 KB (20188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine3.22` - unknown; unknown

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
