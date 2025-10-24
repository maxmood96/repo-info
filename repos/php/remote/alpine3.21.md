## `php:alpine3.21`

```console
$ docker pull php@sha256:844f1fe49e35482bdf675db9ff61dd809c155a74fc4cc24f8fbf277743863893
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

### `php:alpine3.21` - linux; amd64

```console
$ docker pull php@sha256:8df3e817841ecdda526c9d1e4baad7c937d0ad01661c003b6814720709240bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40666296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd75e7b7d81cba9dd1e5679790f387d7e4e066318a7b08c8adfca1b1beea2108`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 25 Sep 2025 18:46:43 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Sep 2025 18:46:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 18:46:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_VERSION=8.4.13
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 18:46:43 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9d8fa4ac8c0b818a31c78d7b16a64544669548afb39f6c70970e61559802fe`  
		Last Modified: Wed, 08 Oct 2025 22:48:21 GMT  
		Size: 3.4 MB (3367265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daeb153cd27a12fa4fdf9516242937e5e4b11461f61dc7399872e041b4357b0f`  
		Last Modified: Wed, 08 Oct 2025 22:48:21 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4bfc408f0a7759b504dff97ace4757333f7eee6ccd2af91d73f6b42f09a265`  
		Last Modified: Wed, 08 Oct 2025 22:48:21 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04556cf0878e174bc61b9b944cfab192a35fec810d672e27ced296b333b4d5cb`  
		Last Modified: Wed, 08 Oct 2025 22:48:41 GMT  
		Size: 13.7 MB (13667216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc65cf4278ca17f99d28023148aba8b306196b0a0e2fef16c110487090e7634`  
		Last Modified: Wed, 08 Oct 2025 22:48:21 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8de9a86c0fb639ee6021387d549fcd1beab5545bf22d9c65e8324b19ab8e81`  
		Last Modified: Wed, 08 Oct 2025 22:48:22 GMT  
		Size: 19.9 MB (19945233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43d13ae613ecaac26a6b8ea0f131c5650494e7bb3ebfa638984025846aeb23d`  
		Last Modified: Wed, 08 Oct 2025 22:48:21 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02003f9b58b01ff9af82ff353f0592ad1e58075b599846030ed069ca0edd57c1`  
		Last Modified: Wed, 08 Oct 2025 22:48:21 GMT  
		Size: 20.0 KB (19964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63eb75287b2e77f9653d88c34516ca2c5aa62f9877032fb83e9b28436a6c766`  
		Last Modified: Wed, 08 Oct 2025 22:48:21 GMT  
		Size: 20.0 KB (19964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:8d98b1591fb050194f2f783f84b3cbd638e3873d19dd5d0be1b948e79e25c728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.8 KB (319756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6671f6711ecdf321596c0b23b51caf0e8ba2783c5e5391f7596f0fa3ea2a22b`

```dockerfile
```

-	Layers:
	-	`sha256:3735a76108a89b6db6080d22032c855b7afe5889c53fdd358325442c375987df`  
		Last Modified: Thu, 09 Oct 2025 01:54:32 GMT  
		Size: 279.1 KB (279063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46fd2f0bbaf811f332da34506998ce16119b7ac2a2057d0958ccf925facb8fa`  
		Last Modified: Thu, 09 Oct 2025 01:54:33 GMT  
		Size: 40.7 KB (40693 bytes)  
		MIME: application/vnd.in-toto+json

### `php:alpine3.21` - linux; arm variant v6

```console
$ docker pull php@sha256:37271c46dcc3f992665f03025e8346c0a1210f5555071ad6d71fffaa225e99f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 MB (38470057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d11a33bc4d8d49f99a13f71f26b99bd5064d89021c6a018d03bf78c661133d0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 25 Sep 2025 18:46:43 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Sep 2025 18:46:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 18:46:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_VERSION=8.4.13
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 18:46:43 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b755bde420789a3b82c763b832866b06b08081d724ca623c4e169786b1f2acd`  
		Last Modified: Wed, 08 Oct 2025 21:47:04 GMT  
		Size: 3.3 MB (3337185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70e66c5c83c3bb58f10dc97c277bb551c2dd8af3980dc4ce1852c37c691d793`  
		Last Modified: Wed, 08 Oct 2025 21:47:03 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b88aec03d5022a381956f4a02be1ac0b5cb856f7cc4a442b271942eb2761c4`  
		Last Modified: Wed, 08 Oct 2025 21:47:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1aaf19494f9bdfdb4a92a66f119354b39b7e4d9d6db5b25e55ae4bd6828d1df`  
		Last Modified: Wed, 08 Oct 2025 21:50:08 GMT  
		Size: 13.7 MB (13667223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba55e5092f1f147296840d5b838993295ab8e3d81015488b703294839764549`  
		Last Modified: Wed, 08 Oct 2025 21:50:06 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c0481a9551b6a390ec9cb6b7b49fe63ca8ecea70df31543c765f13dcf90360`  
		Last Modified: Wed, 08 Oct 2025 21:50:08 GMT  
		Size: 18.1 MB (18056526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d0e75ab0d88c405f753e785588f9dde94774d28bd5d2ebe66c9c5eee284c81`  
		Last Modified: Wed, 08 Oct 2025 21:50:06 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123e2b06513b07bbf8585f49c7d5146dafe7dfbce19fa1fe5f28a09b4e0a7a51`  
		Last Modified: Wed, 08 Oct 2025 21:50:06 GMT  
		Size: 19.8 KB (19781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422ecfeb06131e6fae6a85ef35024bb37d2648a3a2cfa76d75b954d1b59facf7`  
		Last Modified: Wed, 08 Oct 2025 21:50:07 GMT  
		Size: 19.8 KB (19778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:175c9b4e30a6da01c9a0b327fe7c41d733cbc11eef475c11ff873b39add3ae78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 KB (40669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3e4346a9c7eabe19a03f094e16499884d32e5b929d01c28158d53cc7be2c4d`

```dockerfile
```

-	Layers:
	-	`sha256:cf81dd3401c99602b049d0e692314096a0ec044142b455ceefd88da59dd1d5f6`  
		Last Modified: Wed, 08 Oct 2025 22:54:54 GMT  
		Size: 40.7 KB (40669 bytes)  
		MIME: application/vnd.in-toto+json

### `php:alpine3.21` - linux; arm variant v7

```console
$ docker pull php@sha256:83b0b88dca01d2f2ff033bc0a6ff2735cf7c146846f07479eec235f80bdfb767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36988134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3697082f27826578174e2a73dab8504f02058500b8faaf7f1febab07d818b62`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 25 Sep 2025 18:46:43 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Sep 2025 18:46:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 18:46:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_VERSION=8.4.13
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 18:46:43 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 16:24:34 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039410f9bf4014b0d786e60ab4b4b8ee6f000a17a083ed5cfa6086775ee9ee1d`  
		Last Modified: Wed, 08 Oct 2025 21:27:34 GMT  
		Size: 3.1 MB (3143466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d059e7ff1636f09d8ae585ed74885cb7517b342fc047935f19934e010d864d`  
		Last Modified: Wed, 08 Oct 2025 21:27:40 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a695ec4f34cb492d4e690e01b784d6e53ba5e82a0594edaf7ecb1ab552924540`  
		Last Modified: Wed, 08 Oct 2025 21:27:43 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24addbc677ec3068494b8b6e206cc7b2702320a841d3f02124d4e5985df4af3d`  
		Last Modified: Thu, 09 Oct 2025 03:24:50 GMT  
		Size: 13.7 MB (13667218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946799efc1c8e3543bb465b8d577d90d9a66ffb8244a2d7a01e9065c58f3fc7e`  
		Last Modified: Wed, 08 Oct 2025 21:27:46 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643efb18d90e4c619f3066a196a8c7e6e4132e6b6021d71514f23b4b0e95a1be`  
		Last Modified: Thu, 09 Oct 2025 13:26:27 GMT  
		Size: 17.0 MB (17035192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ceee3247e45c003730df49af8bb86434ba455d4a8040a2356fd5a68e9704520`  
		Last Modified: Wed, 08 Oct 2025 21:27:49 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08ea6b0ab181012b53e435b007578cc64a7fe743822596716c7e657090e95bf`  
		Last Modified: Wed, 08 Oct 2025 21:27:51 GMT  
		Size: 19.8 KB (19781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff19baad12b103618d4c0581efa12db5918b18afaecf617199db7812f5fbbd80`  
		Last Modified: Wed, 08 Oct 2025 21:27:54 GMT  
		Size: 19.8 KB (19777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:a8047837fcfdc0470bd525d9e2f060e8d4d09cd3159ede67c33406af8801767f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.0 KB (317025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ada7114fd29d247f9ffd6a608e44ccffb0158d8e01534794ac7702e991c4c3`

```dockerfile
```

-	Layers:
	-	`sha256:20e0c46eb41938e7b239b5d1b50d0c3ffe6e6423f6006faea1f4e67e3f42cfc7`  
		Last Modified: Wed, 08 Oct 2025 22:54:57 GMT  
		Size: 276.1 KB (276141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6066856778e49a4a3f68ebf48786555b04a3a8df1af5f40f76289e7760e627`  
		Last Modified: Wed, 08 Oct 2025 22:54:58 GMT  
		Size: 40.9 KB (40884 bytes)  
		MIME: application/vnd.in-toto+json

### `php:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull php@sha256:274fc9f15afa3bb587a0a05abe509d2f5afa02a64e9a1f0b02301eb905370792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40566390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4016212fa1b16a2df1cc3835fd6017ca93ae0d0715e59eb9437dfae5ca398a1b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 25 Sep 2025 18:46:43 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Sep 2025 18:46:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 18:46:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_VERSION=8.4.13
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 18:46:43 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b08325afc5322c8b990ae0bd9ee52a9663e0ecef0de440d9c1e200dee7b7331`  
		Last Modified: Wed, 08 Oct 2025 21:34:15 GMT  
		Size: 3.4 MB (3361517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06871aadfd027b8064d7fb68436684f159268ec9ab241012bf259e9cd099d53d`  
		Last Modified: Wed, 08 Oct 2025 21:34:15 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36be133cfad2bce984bd124b32d39ab505f07e13a47a72356a312af78830ff16`  
		Last Modified: Wed, 08 Oct 2025 21:34:15 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41c45a6ca0dd28469af8e35185ceef9be0bf6a4c5696321dc5ac03e9af89bf6`  
		Last Modified: Wed, 08 Oct 2025 21:34:16 GMT  
		Size: 13.7 MB (13667227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e036f5939afc0f0d59bb76027994f6347535b3b58ed9d5181003e53a4b389142`  
		Last Modified: Wed, 08 Oct 2025 21:34:15 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8019b6965e6cc1d2ac5495b57e8f29d14165d806549ada227f679daabb7a02`  
		Last Modified: Wed, 08 Oct 2025 21:34:16 GMT  
		Size: 19.5 MB (19501626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2754ab906dbd680012033b70bf8776678dbcc6cfeefd97c951bc701d538110c`  
		Last Modified: Wed, 08 Oct 2025 21:34:15 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f946fa346f252887a93faa5e8c1b3026dacdf97c1845a4b20a68c9339e0edb`  
		Last Modified: Wed, 08 Oct 2025 21:34:15 GMT  
		Size: 19.8 KB (19792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ed4f0206c6819d6c5f8220d97fc861b58f1a7348b151c7e7d38861d1ebcaeb`  
		Last Modified: Wed, 08 Oct 2025 21:34:15 GMT  
		Size: 19.8 KB (19788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:0f2527d0c1971bc9ea7b91aa5038e5e624f53950c1713488e27d988b5805960f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 KB (317113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736307b746e95a0dca0053b8fc94259d15642738d63a7215fe9d458b1c3f6240`

```dockerfile
```

-	Layers:
	-	`sha256:e3957ba865b25bb56ecf9511996731c238c2c6f0be54af453406d7982a77825a`  
		Last Modified: Wed, 08 Oct 2025 22:55:02 GMT  
		Size: 276.2 KB (276177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce0edcadc9a8619d7b3764819cec29e805d7b9355fb68b0f1b57dd56ad6fbee1`  
		Last Modified: Wed, 08 Oct 2025 22:55:02 GMT  
		Size: 40.9 KB (40936 bytes)  
		MIME: application/vnd.in-toto+json

### `php:alpine3.21` - linux; 386

```console
$ docker pull php@sha256:6e9e00762fe9f0eec80d29fa614e13d213682bd2743923b7b125770a76007520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41065496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab16404082f5f4432b5b7b1ff99eed2c3a6a0039d64db9566efb51fc6e3e5e8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 23 Oct 2025 18:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Oct 2025 18:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_VERSION=8.4.14
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Oct 2025 18:46:40 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286bc319663ca948ff89680a59b8e843251203a1fcb108a1be6068bd34e511ba`  
		Last Modified: Fri, 24 Oct 2025 18:42:22 GMT  
		Size: 3.4 MB (3411129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad60adb88be338246d08d1abc8e55c3a3409463889186bcd95246b4a26ebc94`  
		Last Modified: Fri, 24 Oct 2025 18:42:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c70117e4637ad387f4dcb7532f3a978e0a2cf53005af36fc65585d91c00d7b`  
		Last Modified: Fri, 24 Oct 2025 18:42:22 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b1a8c059b5f67bde29893b62cc9b348e505b33938b988ff0055a2f429ce574`  
		Last Modified: Fri, 24 Oct 2025 18:42:23 GMT  
		Size: 13.7 MB (13665734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f3028adfd74f896d78c3d837f1a25efe17186e5a9fa7f389e34caffbc3d8d3`  
		Last Modified: Fri, 24 Oct 2025 18:42:22 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06c5148189bcec4bf75c25ff81775f2c9bef0746ae44067bbff662b330058fa`  
		Last Modified: Fri, 24 Oct 2025 18:42:24 GMT  
		Size: 20.5 MB (20479927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7299a19d6d611e444f3856ae82275c1b652072a5fc7c598a928b8390a9275989`  
		Last Modified: Fri, 24 Oct 2025 18:42:22 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37723f6598c3432ea9b24a054579765098788bdf3a420672a1a8e16e5ed2881a`  
		Last Modified: Fri, 24 Oct 2025 18:42:22 GMT  
		Size: 20.0 KB (19964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce591c7a4ed0c1db42400f08b4ab653fbf2e9ecd1f283a16025e802964084f4a`  
		Last Modified: Fri, 24 Oct 2025 18:42:22 GMT  
		Size: 20.0 KB (19952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:e5a2a9a44d1f1c4f898f44d27bad802de3df8c965d25eb3ad68604fad01e192e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.6 KB (319647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8c145419afe2d0dc851df2188d67f2031452b158ae33e5867dcfbec2d71cb3`

```dockerfile
```

-	Layers:
	-	`sha256:fd00bc7e863515212072a986edcdc08898f16bf81759d7af335b08d1cc98aed3`  
		Last Modified: Fri, 24 Oct 2025 19:54:48 GMT  
		Size: 279.0 KB (279018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a0b40bfaf4303921aa29cacca282a0613de2e7d2138dc9a1195eb6cc6729d13`  
		Last Modified: Fri, 24 Oct 2025 19:54:49 GMT  
		Size: 40.6 KB (40629 bytes)  
		MIME: application/vnd.in-toto+json

### `php:alpine3.21` - linux; ppc64le

```console
$ docker pull php@sha256:c4c6ffedc310017a824a1cb35ca369f8037b463f79f6cba46b8404fe3c6a1956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41654842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7401150938f2574552b27507099ee3c79d77737ceed78fad364a7b79b44baa`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 25 Sep 2025 18:46:43 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Sep 2025 18:46:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 18:46:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_VERSION=8.4.13
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 18:46:43 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 16:25:03 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05a34606c24896e36ea8bdfe146c7d0b83c28b1470998ac131a82d3cbf692f0`  
		Last Modified: Thu, 09 Oct 2025 01:04:17 GMT  
		Size: 3.5 MB (3513487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c41ef4ee60bf72c2b853908cfc0b6f6c5cc89255619d152b030b79cf281488f`  
		Last Modified: Thu, 09 Oct 2025 01:04:16 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a59e8dfa4a38d292b2272817a061750157530cfd7774765e1be1250c61c3e94`  
		Last Modified: Thu, 09 Oct 2025 01:04:16 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb6c65afb93abdb80cfb82ac3355b4e18436c530fd54a03ff0eb1332d483fa0`  
		Last Modified: Thu, 09 Oct 2025 01:28:05 GMT  
		Size: 13.7 MB (13667223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba495e293d0bec921f3030094f70a10ca2d8526fc719b832036ae6ac4a6c03bc`  
		Last Modified: Thu, 09 Oct 2025 01:28:04 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0431def994dfc5066697fd9e547c9f0b5db0224d71d28567511a9fd10b84f6`  
		Last Modified: Thu, 09 Oct 2025 01:28:06 GMT  
		Size: 20.9 MB (20856410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcec2ee43c3a800f1bf884eb8fc30f0fd76a97dfd3b5ab8e445dce48c4b1cdf`  
		Last Modified: Thu, 09 Oct 2025 01:28:03 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2757c04aa642f8cc1b7e76d03ebdf66748f46e239bbc8d7c0e5213fb3e54a0fa`  
		Last Modified: Thu, 09 Oct 2025 01:28:03 GMT  
		Size: 19.8 KB (19778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18e524948e1c8bcc5fd46fd61ad4025903dc2f8ab6e7e980a5d72e0c61c1bb5`  
		Last Modified: Thu, 09 Oct 2025 01:28:04 GMT  
		Size: 19.8 KB (19778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:7ac5fa5d3da84a0856fe8d61b1a326b8143258dbd169f7df5bc3fe10e064c6bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.0 KB (314954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf570a28bb858c0ca7f6b16439a145c377a4468996e6af8997373b0e3d4e353`

```dockerfile
```

-	Layers:
	-	`sha256:2ea58b9406164a26a0ee612dbcc78d8c9750bd68e370a78adbceeefc9709b36c`  
		Last Modified: Thu, 09 Oct 2025 04:54:39 GMT  
		Size: 274.2 KB (274180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e9f211783802916fcdb03433f0a8d93a93ecce07e5035ca0599916a127d923b`  
		Last Modified: Thu, 09 Oct 2025 04:54:40 GMT  
		Size: 40.8 KB (40774 bytes)  
		MIME: application/vnd.in-toto+json

### `php:alpine3.21` - linux; riscv64

```console
$ docker pull php@sha256:46aa37e14f15f541675525e70c96695f8e0d8c5369738f1576afcc2fa705b873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39914608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d192a67ec0d4bf7cfaa14ef6da66a9a10df8b0263834f95cff6b0f79027882`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 25 Sep 2025 18:46:43 GMT
ADD alpine-minirootfs-3.21.5-riscv64.tar.gz / # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Sep 2025 18:46:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 18:46:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_VERSION=8.4.13
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 18:46:43 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:f874295bfcd01a87ee99265d45f0786d35242cd9d53bc2744cb330bf3be277f5`  
		Last Modified: Wed, 08 Oct 2025 21:19:05 GMT  
		Size: 3.4 MB (3351001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b4b6b5df65583dbfb630ea00737b31431acd95351a8911538e0d48988041fe`  
		Last Modified: Thu, 09 Oct 2025 09:24:19 GMT  
		Size: 3.5 MB (3492377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058411602b31aff80dc2a52786ab3585b8b01a5029568e3b5135401574e8618d`  
		Last Modified: Thu, 09 Oct 2025 09:24:18 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287d635bbdb57d4de98951a4f3c3c7c37a8517af3c6f9118b910bc76c6421f56`  
		Last Modified: Thu, 09 Oct 2025 09:24:18 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4f154f0eb375506b62d9bcb6719d9eafd599b9880a007b01f21188ff44caac`  
		Last Modified: Thu, 09 Oct 2025 15:16:02 GMT  
		Size: 13.7 MB (13667217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b04eb301cd16304b9db216dcf48410f0364dc94018cc7d9bb8f9785f1a92a0`  
		Last Modified: Thu, 09 Oct 2025 15:16:00 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d849bb6314ad164eb4a9b9568fc0bec35f68e6611f12882c21edc64a26c151a`  
		Last Modified: Thu, 09 Oct 2025 15:16:02 GMT  
		Size: 19.4 MB (19360407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b13ad4ae73d44b145ffc7d0b994af57e7e1d59daacfec95b7318c2d49f8fb49`  
		Last Modified: Thu, 09 Oct 2025 15:16:00 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05c2fe6e30cbe44484e699fb5bb73656e4a3bdb568480dbe98605d04e792842`  
		Last Modified: Thu, 09 Oct 2025 15:16:00 GMT  
		Size: 19.8 KB (19755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78da450ff26ff4358f5424ff54b2ac56567efe8f6152326c178256a2587f90b0`  
		Last Modified: Thu, 09 Oct 2025 15:16:00 GMT  
		Size: 19.8 KB (19752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:b021a869720483753098be99fd8845c4a31a82cc6fd5c7653339f7f5cf264eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.9 KB (314948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20aa20bf2c5be6fc794a797653f7530f5baff386a65150c2449cf1e38c8b8379`

```dockerfile
```

-	Layers:
	-	`sha256:477644c1d3fb1f19f4b7f8bc6a36aee3aaa4b30c6c1c994578b852a995677669`  
		Last Modified: Thu, 09 Oct 2025 16:54:38 GMT  
		Size: 274.2 KB (274176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f28413826a31362db1476dd983a08915c32724b3538aab85947392717701cbff`  
		Last Modified: Thu, 09 Oct 2025 16:54:38 GMT  
		Size: 40.8 KB (40772 bytes)  
		MIME: application/vnd.in-toto+json

### `php:alpine3.21` - linux; s390x

```console
$ docker pull php@sha256:3cb71633d7b12de8e4ca8d254b3d47411c0b8fdf5fa9b61cfe76812ce3caaaff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40737977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7eaf7f9a5aa60ef1a3e366712dc4e1bb1dc1c0411e6ed0e56a36b79d02e8a92`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 25 Sep 2025 18:46:43 GMT
ADD alpine-minirootfs-3.21.5-s390x.tar.gz / # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Sep 2025 18:46:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 18:46:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_VERSION=8.4.13
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 18:46:43 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:9f2ceebb28b6c8480d6ae26501eda06bf0b6029f7c797c80673b95a60276e050`  
		Last Modified: Wed, 08 Oct 2025 16:25:19 GMT  
		Size: 3.5 MB (3466434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49540c560fe10b1e05647baff6bd09f225aaf3a526cf39dba0a8343e1c6057c5`  
		Last Modified: Thu, 09 Oct 2025 06:27:30 GMT  
		Size: 3.6 MB (3596736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2692170ad3b9023fe7d1f440cb17914dc95961c0c7494e0b1d28ba2eaf006812`  
		Last Modified: Thu, 09 Oct 2025 06:27:29 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ee6723e50491cb091c047add64e5dbaff649181c8f4090ad9e6de28ec4afbd`  
		Last Modified: Thu, 09 Oct 2025 06:27:30 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad8aec0f58ab63aa939398f677d1bf4547d76bea3af98d948490f21499dc9e4`  
		Last Modified: Thu, 09 Oct 2025 07:54:55 GMT  
		Size: 13.7 MB (13667216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a77de5a48e0ff338e1daa57f59b608ea3276a91e2095ec4e4fc1c84e7406a1`  
		Last Modified: Thu, 09 Oct 2025 06:50:16 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2edd15341cc4ab5279f068f1288a081f4f7b0dd89a59dcd4653c0fd801a8f0`  
		Last Modified: Thu, 09 Oct 2025 07:54:56 GMT  
		Size: 20.0 MB (19963940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038fc55d479454092861a783b97369f56e13ab65bdf4ce2004eae2ab359a2cfa`  
		Last Modified: Thu, 09 Oct 2025 06:50:19 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4352ec5ad8818c05c580bdd6589a6d09b2ffca37ba3acd8ae087bdd4edaaad`  
		Last Modified: Thu, 09 Oct 2025 06:50:22 GMT  
		Size: 19.8 KB (19783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bae85eb3c86151f093e2bfc6222126aeacdfeadc5f8ff6fd813d7ea8588db9`  
		Last Modified: Thu, 09 Oct 2025 06:50:32 GMT  
		Size: 19.8 KB (19781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:alpine3.21` - unknown; unknown

```console
$ docker pull php@sha256:7b4f878ce7492798f8285d038b854ae0b9c7f00ac4005e17d68703ac6a262637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 KB (314816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aae521b0442b9ec32cd37c8c46e10530a037677f2c522c83f609ac4e2156e32`

```dockerfile
```

-	Layers:
	-	`sha256:6bd9d9983c67c502fb518e0a3ddd9d14877e75329d4d0d0414e4a41a86f6b495`  
		Last Modified: Thu, 09 Oct 2025 07:54:35 GMT  
		Size: 274.1 KB (274122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8647d49ab3dd7c015f735ec924eaf71c8a02351be991f39f95b2e56eadb404c0`  
		Last Modified: Thu, 09 Oct 2025 07:54:36 GMT  
		Size: 40.7 KB (40694 bytes)  
		MIME: application/vnd.in-toto+json
