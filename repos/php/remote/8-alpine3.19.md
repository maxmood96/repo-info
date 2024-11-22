## `php:8-alpine3.19`

```console
$ docker pull php@sha256:347efd00e57c7953b4b30f9b4784313dbec5f245ce62d3adb92e68f76be70944
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `php:8-alpine3.19` - linux; amd64

```console
$ docker pull php@sha256:b3b2c6c0c14833988e9a9f1ea2bb8f1c40f4db966575ea38c0e1adc51e8c0263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42634015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a9933aefb6f01d5f309d8d31af7cc8f637b6b891673642e8903d031b0af3f9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cbd4e92d4aad2da810857d5e0707b9d345bba542202d5c78e000ba01c6bc7d`  
		Last Modified: Thu, 21 Nov 2024 18:00:25 GMT  
		Size: 4.9 MB (4872450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb311e71f75d9e6699fe5ce74e8eb8e4cbaa22fc8425c974295b8eacde196fe`  
		Last Modified: Thu, 21 Nov 2024 18:00:24 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296342bcbcd78b6c8ae47aa46360dc393aa70dd5639a5af99895b7eeb69d075c`  
		Last Modified: Thu, 21 Nov 2024 18:00:25 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e274a821e9506b7a3c01fa99ff1722552c943e541c113a30d0d3bc09c742f4`  
		Last Modified: Thu, 21 Nov 2024 18:00:25 GMT  
		Size: 13.6 MB (13572762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5e855d634bc0fbc242a224d82f31847a239501f3dcde6ae276aa8de037bb5a`  
		Last Modified: Thu, 21 Nov 2024 18:00:25 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2a946d63e6df37ce6b38755466c1b8af965283612449cdede9125dbbc3654f`  
		Last Modified: Thu, 21 Nov 2024 18:00:26 GMT  
		Size: 20.7 MB (20745205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac12611a387940ae63f808c7b633d01ff2e1c1d3a54355b8b719ceb52dc3df9a`  
		Last Modified: Thu, 21 Nov 2024 18:00:26 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182f867c2a19813deee33fe4a850823b976b9f3a8333f2b23032e1dd2501b3f3`  
		Last Modified: Thu, 21 Nov 2024 18:00:26 GMT  
		Size: 19.5 KB (19489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-alpine3.19` - unknown; unknown

```console
$ docker pull php@sha256:f00abfe80892ffec2123add29bfae72f6fa307a6e1871b430d02fe8f76172607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 KB (299833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd8a55391cc3c29bca44c71724dd5169afdade42c982e543f0d89d8a6020522`

```dockerfile
```

-	Layers:
	-	`sha256:e6be0aed9cf704fefb4ec43267909014bcccc0b60af8af41db283757c88d9ea2`  
		Last Modified: Thu, 21 Nov 2024 18:00:25 GMT  
		Size: 261.9 KB (261920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24adafc6cbaae04dc457b2c9a1ef1b962890d5e53a8d9014130f8460cfe5acce`  
		Last Modified: Thu, 21 Nov 2024 18:00:24 GMT  
		Size: 37.9 KB (37913 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-alpine3.19` - linux; arm variant v6

```console
$ docker pull php@sha256:97927b27015c3d561c57d8c6739537310fcaab1f0670e5ed354d0493d808bff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40341439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f7823228c6a5cfea3207ab279b08ed77bb09e1ed12ae87f9841e4bd0b57dcf`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d506df09dbdf91185add3a7b93df87df3f96e9e86244bb5a36ce976bad384da`  
		Last Modified: Tue, 12 Nov 2024 03:04:19 GMT  
		Size: 4.5 MB (4549552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2565c5d4979fc78805381ae54974577a69443306d5cd6ce30896d12062df3b5f`  
		Last Modified: Tue, 12 Nov 2024 03:04:19 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2a131775c3bd5253ef21285ac1b265871981ec4c9eb57a1a2dfc43a3072104`  
		Last Modified: Tue, 12 Nov 2024 03:04:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922a311395dc3bc52f7dda5d9cdf0cac4b40e36c60a1cd6f3cdaa0a2aa4658a6`  
		Last Modified: Thu, 21 Nov 2024 18:09:37 GMT  
		Size: 13.6 MB (13572767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67560d51bf4721b5ca134b2309bcb37020ed0fe719c7430131b9034f41c113b0`  
		Last Modified: Thu, 21 Nov 2024 18:09:36 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762ae4d25e0449866cfb7c9b05e19ed0a950fe317a40255f3e065d75969af57e`  
		Last Modified: Thu, 21 Nov 2024 18:09:37 GMT  
		Size: 19.0 MB (19018965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1111603501993e37f2fd780de0ad2e9bc103395836326c0e4f298009086232a0`  
		Last Modified: Thu, 21 Nov 2024 18:09:36 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b89eea1af0dcd727d4368cc0d29c5b6b5d5af9f5101abdafc22267b9e8f1b67`  
		Last Modified: Thu, 21 Nov 2024 18:09:37 GMT  
		Size: 19.3 KB (19329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-alpine3.19` - unknown; unknown

```console
$ docker pull php@sha256:aef155379c96e128c947fe2039fd7ff7f739ea6dd5e366a59f1e81a0285bffea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a802aeaae9764f0c86c24249e0730d9fbead76b5588ad77c33159592e281943`

```dockerfile
```

-	Layers:
	-	`sha256:0699ec097dbd271e6ca8f4234cfa97ad153e82abdcd011ae74497d0723895cd9`  
		Last Modified: Thu, 21 Nov 2024 18:09:36 GMT  
		Size: 37.9 KB (37872 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-alpine3.19` - linux; arm variant v7

```console
$ docker pull php@sha256:4b92cc192c747875d91649c82a69f5590539b9c4b462ee5b947da9d076aabf08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38716189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b43656c11df1aaa0adec91220e5aef218f6e9345b2ed0e8fc3b378a39c7af15`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:02dfd5e2e7e47e8d8f9020a0d7f4d8240d6646afc6a52b168c0899bc0c3d06a3`  
		Last Modified: Mon, 09 Sep 2024 07:03:23 GMT  
		Size: 2.9 MB (2927731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0436284ed3df1ea72ee7578e1acedcb3f1d13662da3f84c96df0f7250b0e65`  
		Last Modified: Tue, 12 Nov 2024 04:13:48 GMT  
		Size: 4.3 MB (4273946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f71fe689f2c66318ac16bb591f4263243d0ee583bf8e58b422159d0e8e5f74`  
		Last Modified: Tue, 12 Nov 2024 04:13:47 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459364abd934a595a7d02d68c9dbf45d3769fec662e99f1aa3c9c4f8554b53a6`  
		Last Modified: Tue, 12 Nov 2024 04:13:47 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a4f19ff012447e24d4f4a1bfb8f9300ce5c9b69094c1d4a145ea5628d39e67`  
		Last Modified: Thu, 21 Nov 2024 18:39:28 GMT  
		Size: 13.6 MB (13572761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4687c20ab71582a44c12d4ca91aeaa6b5b9f24dc5b8143f0dab5687379d2c707`  
		Last Modified: Thu, 21 Nov 2024 18:39:27 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5a7e8ee55eb628a14ff422e81149c9c4cecb9a083eb15bbf2a03ab403c4fad`  
		Last Modified: Thu, 21 Nov 2024 18:39:28 GMT  
		Size: 17.9 MB (17918050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bb33c5e20bc9006068b2a5a5e3763937c1a49b5955576dff85bb77e6db0c94`  
		Last Modified: Thu, 21 Nov 2024 18:39:27 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087aad502db2dddf9ed54ac2c203f0f00bba0367547048f462fdd79254208397`  
		Last Modified: Thu, 21 Nov 2024 18:39:28 GMT  
		Size: 19.3 KB (19310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-alpine3.19` - unknown; unknown

```console
$ docker pull php@sha256:ccfaaab0e562abbaed2dd1cae0e4caea7a8ab7d1123695ebd8e13ad4b1d60c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 KB (297211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2734edf34f65616af00cada9466ef69b9204de0e9bfd26205891974df1e229aa`

```dockerfile
```

-	Layers:
	-	`sha256:87e6555628c57e66c845df339daf5321bf750ac3f2ae29b01ebd2f887e8c3ff6`  
		Last Modified: Thu, 21 Nov 2024 18:39:27 GMT  
		Size: 259.1 KB (259124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760de3439cf498dc12369dc0c338b5cb2bb63e815c65f253dc231e4ee926f274`  
		Last Modified: Thu, 21 Nov 2024 18:39:27 GMT  
		Size: 38.1 KB (38087 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull php@sha256:f37a0674588c0868fee07466d51822b8ba556346b8c95ec0577f0f0adaf211e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42126898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c94eb08d8e8e8392ddf6f92cb806cc2c6cad0730f91858206c89c45e706687c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3839b7b4a4d9b48a146f2ba462de35a529a61c987f81f1db5ff4a6b43f6a973b`  
		Last Modified: Thu, 21 Nov 2024 18:36:59 GMT  
		Size: 4.8 MB (4810691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbfe97051f5d60c8fe7d94f354f5fbe1abcabf1d39303a8ace22c4c46e51507`  
		Last Modified: Thu, 21 Nov 2024 18:36:58 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c42a6acff4f600ebd3d688f9a445895bec79183ecc9f84c783162c57ec1f0c`  
		Last Modified: Thu, 21 Nov 2024 18:36:58 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a3d2f5988d22a34a48d19213ddf825853b69fb212d95a40ad31a8dfecc34f7`  
		Last Modified: Thu, 21 Nov 2024 18:36:59 GMT  
		Size: 13.6 MB (13572764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9023f272683d8561eb7ec4e0769596895ba3674a45acd167180f0c1debab601`  
		Last Modified: Thu, 21 Nov 2024 18:36:59 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8044f67e6880cde72720c29d39b01ac3c57404f34cd45a31062fefd8e0bdb590`  
		Last Modified: Thu, 21 Nov 2024 18:37:00 GMT  
		Size: 20.4 MB (20360501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f237d858f521fd560576d760c064bfe49e518a1ad1d31c8b5c158c5041de312f`  
		Last Modified: Thu, 21 Nov 2024 18:37:00 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dbb25f4876c96ff228209b91f78c1ab77e21782c54160db81e316e60268ec0`  
		Last Modified: Thu, 21 Nov 2024 18:37:00 GMT  
		Size: 19.3 KB (19321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-alpine3.19` - unknown; unknown

```console
$ docker pull php@sha256:d4d19c5bad35a57ab1f68d557b9380a839e851decf88949a502b38973fdf8352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 KB (297301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0b471cfb6e01d97ce52471799a01b238292125e072b61143f22566db70a046`

```dockerfile
```

-	Layers:
	-	`sha256:767fe6a8453d8be0e27eed11631dfbdb30afcc010f8d91a637d53e1feb0ec8ee`  
		Last Modified: Thu, 21 Nov 2024 18:36:58 GMT  
		Size: 259.2 KB (259160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:428007e4ccc0de13a2c352ee80560256c7abb8c6bcf48c177ab170d3f4d3b776`  
		Last Modified: Thu, 21 Nov 2024 18:36:58 GMT  
		Size: 38.1 KB (38141 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-alpine3.19` - linux; 386

```console
$ docker pull php@sha256:259a0f39dedaeee905b0a0c79b724c02b028540bb7357faa1ee6c445f3ad0d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42892259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d8750252ccb2fd6e0394ba1e06796b96d5ad4935e24ec06340d932101aac54`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb4688e3868be618a2a78fda9daac09377516a57afec1a9708503ad7fe3cf65`  
		Last Modified: Thu, 21 Nov 2024 18:21:12 GMT  
		Size: 4.8 MB (4760577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef85bc4873fc9b7fe98d73222111f991b7fbe11496be7b83798db74a82a0c18`  
		Last Modified: Thu, 21 Nov 2024 18:21:12 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1359ef641c62002e931c8cfba2daac73f743d40329a719b672eb3fb825ca7d02`  
		Last Modified: Thu, 21 Nov 2024 18:21:12 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6337fc2b38af3c4b012d2c6bfe246017befd52077809c34cde57205b1925d1cf`  
		Last Modified: Thu, 21 Nov 2024 18:21:12 GMT  
		Size: 13.6 MB (13572764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cca4a275f90035b083c2073106d093ad4a536a0c89bbc2a51e8107facc42609`  
		Last Modified: Thu, 21 Nov 2024 18:21:12 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e80a44c909f7b03b8e726ce3a6615a9885168a1a4cf2de9cf2b80230da103ad`  
		Last Modified: Thu, 21 Nov 2024 18:21:13 GMT  
		Size: 21.3 MB (21281364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7eda0aa97516ffad92530d5c2db820a2d928a9d6a3d449d4178a7ad9bf8bc71`  
		Last Modified: Thu, 21 Nov 2024 18:21:13 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63d6a73e06aa5e04f0a810b407af5293c921021bb6f0eb59c81cf6e3e8a5172`  
		Last Modified: Thu, 21 Nov 2024 18:21:13 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-alpine3.19` - unknown; unknown

```console
$ docker pull php@sha256:9bfb4e83c986e5b42cbdcdc1d606dd2442d481275713b3a856bd2dfa3f92d511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 KB (299727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b049b1e42b57d07548d4a2abb1723fd923b15141972bab7d12d099e39db23a`

```dockerfile
```

-	Layers:
	-	`sha256:be06ccfd85084e68e6dbf06ffd0e7e1fb4ef9776aee310ffa76005d5500ab3a7`  
		Last Modified: Thu, 21 Nov 2024 18:21:12 GMT  
		Size: 261.9 KB (261875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af52238360ca6ca28ba0f942c0aa3ff7ed524f87fab0e10c31aaed9d2d4dd929`  
		Last Modified: Thu, 21 Nov 2024 18:21:12 GMT  
		Size: 37.9 KB (37852 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-alpine3.19` - linux; ppc64le

```console
$ docker pull php@sha256:14a5839b33b220350f54af7ad346e1970edfd83e06011a5113ab894ed3637a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43474757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75fb6d658c5621cc0f9263cb3d11104b80c8ca6c151760ba3a3a21a29d82124d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:c3045cb4f0dd3320c62c35c3443bc350e64a45c48666004b29e9912a645e7b35`  
		Last Modified: Tue, 12 Nov 2024 00:55:44 GMT  
		Size: 3.4 MB (3364499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35b5b574e5e7a1963997e6adc5fc6c41ea62b3d72487780713b6d09006e673c`  
		Last Modified: Tue, 12 Nov 2024 03:49:43 GMT  
		Size: 4.8 MB (4816871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4503eb1a8e49f698eea61c5c4dce1fa0040ce6ceca1d52253836027f00e9d7`  
		Last Modified: Tue, 12 Nov 2024 03:49:42 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c453f6eea919490bc644797b1f6b8249d5e157a311bebf21cec14cdc7315bd97`  
		Last Modified: Tue, 12 Nov 2024 03:49:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423f6f945e927d2611800bc8517b1d1d7691ac797944f29b067b6337b1128009`  
		Last Modified: Thu, 21 Nov 2024 18:25:29 GMT  
		Size: 13.6 MB (13572761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad1342d77685ba38abed0b9a66041bda5ae3d4cabeebbfc49923f7388609bd9`  
		Last Modified: Thu, 21 Nov 2024 18:25:28 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05d810a099c2868ca734e496d3a311340245230053cddf6e09ec35bae0bd57b`  
		Last Modified: Thu, 21 Nov 2024 18:25:30 GMT  
		Size: 21.7 MB (21696915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934c6a38f412554be48f2552f80e219cb40e0e9b05f68351f46d4fd73afd4222`  
		Last Modified: Thu, 21 Nov 2024 18:25:28 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73924f7d1a9b14762df02d440df7018b1b47bc0e311d00c8eef4677dd20f1e67`  
		Last Modified: Thu, 21 Nov 2024 18:25:29 GMT  
		Size: 19.3 KB (19315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-alpine3.19` - unknown; unknown

```console
$ docker pull php@sha256:d889394fe33c80754f98657d5571b772777c3d71b4c1a18bd4b97c83a32de857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.2 KB (295152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0b6178627703c8f79c8bd9d3cab4e2ce328c99b1c9faeb4f5c8130d39c5519`

```dockerfile
```

-	Layers:
	-	`sha256:dd1126b7c5df7bc8400c113c6b258ee6c32a81432dad5dedf2ed9eb414c22b53`  
		Last Modified: Thu, 21 Nov 2024 18:25:28 GMT  
		Size: 257.2 KB (257160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5dcf37df49950d0252da107997b79eec1343f62b78e8bb1fe2ecd897fce4cb8`  
		Last Modified: Thu, 21 Nov 2024 18:25:28 GMT  
		Size: 38.0 KB (37992 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-alpine3.19` - linux; s390x

```console
$ docker pull php@sha256:ebf31148d0356f84bcb5a93fc4dea09f5d0fb915219cc318a7f9741a15e4375a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42882723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c481c1cf1de9fdd62b829b44ed5c220d516206894bcbd55f8ce2ad1d42b01098`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:6281353bb84e1beeb4deabf01093d4ab69b089bed69f3a95c18702b149677456`  
		Last Modified: Tue, 12 Nov 2024 00:56:12 GMT  
		Size: 3.3 MB (3253396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ebb87545715444ed87e790ef4054fd17853711b917372939fcec005a51ddbd`  
		Last Modified: Tue, 12 Nov 2024 03:53:06 GMT  
		Size: 4.8 MB (4799270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93607338abaacd48124e4ac15fa9ced5b6d5b12eab2b3a8dede0efab1212c45a`  
		Last Modified: Tue, 12 Nov 2024 03:53:06 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afbaeae156c89776da7468752d9ee2392816ff4e3ccfeade1d8ecb4f8b6cd24`  
		Last Modified: Tue, 12 Nov 2024 03:53:06 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5671517d76e13b79979841f54ef69d73729f99435440b741be4c1a3405d1802`  
		Last Modified: Thu, 21 Nov 2024 18:37:02 GMT  
		Size: 13.6 MB (13572763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0094d5567a18c925a876a5a93ad225d69d0a17965856c06a00a3d13827d64c2a`  
		Last Modified: Thu, 21 Nov 2024 18:37:01 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fa416c825a5a516b9c3e15bb18e1101bf3b9c211ef7c8a0bf776aee38d0d5a`  
		Last Modified: Thu, 21 Nov 2024 18:37:02 GMT  
		Size: 21.2 MB (21233579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dded8a3d5b3415c378d465748dfd8f15688acd384968c374e8aed6606720dd17`  
		Last Modified: Thu, 21 Nov 2024 18:37:01 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a939e84626d5c988469a166ded6fc707b989e073f09f7a43f833ea2bf807fe50`  
		Last Modified: Thu, 21 Nov 2024 18:37:02 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-alpine3.19` - unknown; unknown

```console
$ docker pull php@sha256:d25f07f13614e8812d7f62403bdde74854b48df67b9e467bdac792553da5c3d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.0 KB (295016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8fa29a3db2a88f3c18a7758e57ce04a1b760d8ec0e7fad4d55cf9acf42da4c`

```dockerfile
```

-	Layers:
	-	`sha256:e3346e5b7b2c5d25eba1a2f033e6d59dcfa255355dd45a4ae6e7a2dfecaa65e1`  
		Last Modified: Thu, 21 Nov 2024 18:37:01 GMT  
		Size: 257.1 KB (257102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06ea70ad09c8bc2c09ba49913dcf912d567d3d0688ae81bc425887ef95f28f81`  
		Last Modified: Thu, 21 Nov 2024 18:37:01 GMT  
		Size: 37.9 KB (37914 bytes)  
		MIME: application/vnd.in-toto+json
