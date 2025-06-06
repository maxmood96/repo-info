## `php:8-zts-alpine3.20`

```console
$ docker pull php@sha256:2b49e7ca20c45ccbfbfb2b2bdc8fd0d6ca2bb189b5d8a5844f6dd1f1993fe680
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

### `php:8-zts-alpine3.20` - linux; amd64

```console
$ docker pull php@sha256:f246a8607bb5845adabca78ed1cb7c20b03c234cd7c1883e7c5e263d46bd146c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46868127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7081c70284a99aae3759fa9336ce58c54977fda4d00e9e8ed1a79b944dccbe0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c624b8cfac0576a2baf892f2831a8cff74c51c59eef4ec91c994b67b131893`  
		Last Modified: Fri, 06 Jun 2025 17:44:56 GMT  
		Size: 3.3 MB (3313806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef66c66f29d924d4df7189849a8a4ef37d4bf69462c25481f7d9bda72a811206`  
		Last Modified: Fri, 06 Jun 2025 17:44:56 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48d693f6a1c6f818c9010f9526a3d7eac2972d92afcb7aa358568b53d1af8a9`  
		Last Modified: Fri, 06 Jun 2025 17:44:57 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24d64c8df53dd425dfe028f3c5c56eb00e099474b079d244ce834f2bcc78cde`  
		Last Modified: Fri, 06 Jun 2025 17:44:58 GMT  
		Size: 13.6 MB (13640113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169948c4235c7194d73859807052b27eda137e9f55f67f407cda59180a775ed7`  
		Last Modified: Fri, 06 Jun 2025 17:44:58 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bc1c09a15ae5ad3f653e66eae14e78c7c4c43a3daf44635f3e152484a3203c`  
		Last Modified: Fri, 06 Jun 2025 17:45:00 GMT  
		Size: 26.3 MB (26263506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01fdb9a4c5c7710aacf9e689a9d3454dbf77deb640019dc782d3b9edb73ede8`  
		Last Modified: Fri, 06 Jun 2025 17:44:59 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad24f5df0944c9f65b84c6eed8bae24e2e765cd9c22e107541a6de27bf80b9f`  
		Last Modified: Fri, 06 Jun 2025 17:44:59 GMT  
		Size: 19.7 KB (19712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:e601044212a4236ec84bfa4096ace5e7857db87a4d35234d97098fd84d2f596b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 KB (303823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9553c9243e329c88c39c2a1b1a7a068366b73132bed29c5c914b6c897460dc`

```dockerfile
```

-	Layers:
	-	`sha256:0a810dcf18a6f1a8510e87f40627862f7564efb8fc5d4fc1ef9e1693a1e79798`  
		Last Modified: Fri, 06 Jun 2025 20:00:09 GMT  
		Size: 266.5 KB (266535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1f0ce1008aba286314becc38ac81ab83ffea24b584cabf71d0b62da4aab3c48`  
		Last Modified: Fri, 06 Jun 2025 20:00:10 GMT  
		Size: 37.3 KB (37288 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine3.20` - linux; arm variant v6

```console
$ docker pull php@sha256:b26f2ab12cc785100e581e38bbf5151aa9d842da4e62f857c5f3502c198ba53f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44817002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f5f2541116e53d68e8aff06db602ec445031ab9043ddd8c8f908c5a2a9becf1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
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
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 19:26:24 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c0f79d4d985a64f9865dca6388accc72536a8134bb71d173eb4214c357889d`  
		Last Modified: Fri, 14 Feb 2025 20:55:09 GMT  
		Size: 3.3 MB (3298263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ffe6d763475cabc6526162b5d931425de2a4941987a9a47a37817994c917fe`  
		Last Modified: Fri, 14 Feb 2025 20:55:09 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82be80b03c756f18e75ec416857bff7aeee3ead6c2ab8410c9194efd506877e5`  
		Last Modified: Fri, 14 Feb 2025 20:55:09 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc4500ae292986fbadf718530b179720f826c2cb674ee5bd71ee2195e3701e8`  
		Last Modified: Fri, 06 Jun 2025 17:58:05 GMT  
		Size: 13.6 MB (13640121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2144a28ff5e35b9481c9acef1046ed731db246391eed174c1dabd53c2579052`  
		Last Modified: Fri, 06 Jun 2025 17:58:02 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bcb016e757cdf1918b59dcf2e5d011df4ccea134e42f76edcf49578d93ddda`  
		Last Modified: Fri, 06 Jun 2025 18:07:55 GMT  
		Size: 24.5 MB (24482484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbfc93ebae84792742cb170baad2dc9f76fca2a5ac904863a23b43794715f63`  
		Last Modified: Fri, 06 Jun 2025 18:07:58 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7341f3d42a64bfec89c1f9c00a4bfcd31fdddd3c219ea6aea0ff75b8ec225891`  
		Last Modified: Fri, 06 Jun 2025 18:07:59 GMT  
		Size: 19.5 KB (19502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:754e2889408054acac908a5139c5d3944661cc4fc4c4fe601fc27b8999191ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 KB (37214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78113c1a0fa22b455e11df8b6f03e4b1e30e20e588fa9eeb05d89406293a2e1e`

```dockerfile
```

-	Layers:
	-	`sha256:a1e3ecdb303092410e32a0fa51094cbd0a22a34a0259d33789e863ab9c85b7ae`  
		Last Modified: Fri, 06 Jun 2025 20:00:14 GMT  
		Size: 37.2 KB (37214 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine3.20` - linux; arm variant v7

```console
$ docker pull php@sha256:c9677114aef71be19533071a1d999142e358241d5df0e182e65fed66d7bb6fa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42900315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5e12f5452f5edd5f4c1a4ab896b0340967a8c279067bfa0e8bfab382c57409`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
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
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 14:35:10 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f435e04ea18170faa15db5a195b7a456fd6855803819a3ec1feb1150cc547b`  
		Last Modified: Sat, 15 Feb 2025 02:56:28 GMT  
		Size: 3.1 MB (3104652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6d965c1f9e2eeb816a67542a273f236e46e8776d2aaeabebc43098c502ee68`  
		Last Modified: Sat, 15 Feb 2025 02:56:21 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151a378a33b3d6443d5e2151a40e50e2c7f67f3b501115627d75e1ce417f91c7`  
		Last Modified: Sat, 15 Feb 2025 02:56:23 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2452f8249b4a5a13da9952ea525c6de3521a09bb0ed1779db4b17248a15b6a3d`  
		Last Modified: Fri, 06 Jun 2025 18:36:16 GMT  
		Size: 13.6 MB (13640101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c969dcc77d2db750860ab4905d460db4c30d44e96c3a2659400ff7409cc5c908`  
		Last Modified: Fri, 06 Jun 2025 18:36:14 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbda755635f24e5846401723d08bd5cbf973f09e816a9c3d9bf466a5dd938c10`  
		Last Modified: Fri, 06 Jun 2025 18:43:30 GMT  
		Size: 23.0 MB (23035983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840ee95f802cbcec8488be8c64ac69937a99726b74d1211bd3976a845a0c4e52`  
		Last Modified: Fri, 06 Jun 2025 18:43:29 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bbc5672299e9848e1c2eaec4f52f2fe7dff9c4d0ad1541714ea686c1a271d4`  
		Last Modified: Fri, 06 Jun 2025 18:43:30 GMT  
		Size: 19.5 KB (19510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:1d337146cd2912ed81d2630e857d1f5c7c86ea45d6d404e6c68d61a0755d13fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 KB (300962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10eb953468d5161673e2d150dabb9ba45795148b42cf82e4ec74eac389489bf5`

```dockerfile
```

-	Layers:
	-	`sha256:9597dfcf830ec6bf55f8d297ccbb86783a745ae79c7f3eaf6840aa5f4aa3461e`  
		Last Modified: Fri, 06 Jun 2025 20:00:17 GMT  
		Size: 263.5 KB (263533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c66a795ac2a66573e0e0e7aebe48afe96feb0c033dbb78a3cf6a332360935b7`  
		Last Modified: Fri, 06 Jun 2025 20:00:18 GMT  
		Size: 37.4 KB (37429 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull php@sha256:2a4629af5687b3f3e5fa80e747bce8428ca9ff272b9c19a941dc69642c107fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47003874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c8967fcd83159c531d7ceb5d0ea80b01d0174b6dda3a891b400b43a4576456`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
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
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fe7c4771a0ce2779a085cfb360803dcb43f4aec08acf546113a69e16e12a1c`  
		Last Modified: Fri, 06 Jun 2025 18:22:36 GMT  
		Size: 3.4 MB (3365210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2714d74e0c8dd17bd99e4fbc958c219ed46d282967f0f88d4a49b6bada1b93bb`  
		Last Modified: Fri, 06 Jun 2025 18:22:36 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ae1eac2ccbda2589b388b901d8106d995ab998d0c33229ec99e52d6042b1f1`  
		Last Modified: Fri, 06 Jun 2025 18:22:36 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bdbbfa3682a62e5cd0d07042756381119a04c0e2a7250bed52d4f1689355b2`  
		Last Modified: Fri, 06 Jun 2025 18:22:39 GMT  
		Size: 13.6 MB (13640111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7937a72b01c354299d165323bfab63be0d82405453549b35b61b8dcca48e703a`  
		Last Modified: Fri, 06 Jun 2025 18:22:36 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08c66c6dbbe31b37fe9e5b3f64df4809592e61b50492f9894da7e9fd02f6fbf`  
		Last Modified: Fri, 06 Jun 2025 18:29:26 GMT  
		Size: 25.9 MB (25883815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db0c99b7711ac068848166133ed1c02bd863433b5020fa4dfb39b0625a10993`  
		Last Modified: Fri, 06 Jun 2025 18:29:24 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914d8075d683c386cfb2478d614e86428bd0833c4b1d4f9b667c04e334f9ef28`  
		Last Modified: Fri, 06 Jun 2025 18:29:25 GMT  
		Size: 19.5 KB (19485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:b9703a8a74be2de3e0c2d7f9e0b1b3dbc660c9f2ec3aada8de019db7ba7f2b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 KB (301020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55c6ef47f584a08bc69350cc05d84d20bf63b7cc4c0356ec0f3e423800f2a8f`

```dockerfile
```

-	Layers:
	-	`sha256:6b2070739f2561b5b8037f7d6e6d0b4bcfcd2af08876fb82e6796c93e4d1a0e2`  
		Last Modified: Fri, 06 Jun 2025 20:00:22 GMT  
		Size: 263.6 KB (263553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:145b238cbdf20724ca97b271919cff124838a6ada581bdc88dab4fb97608ae8c`  
		Last Modified: Fri, 06 Jun 2025 20:00:23 GMT  
		Size: 37.5 KB (37467 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine3.20` - linux; 386

```console
$ docker pull php@sha256:a308dc6b0efc524a444e776dac539711761d219b6163063b60c10fb4a98e96f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47383777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43acbdce0b8b74493c81c04a4b7b65b26040a8efa1d9538230c4711683271bf5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
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
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 14:36:27 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f947ac0caa1b33fa4a3cf32b7a6713df8dce105d90b91a7244b5574a1940378`  
		Last Modified: Fri, 06 Jun 2025 17:41:08 GMT  
		Size: 3.4 MB (3365395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecf060053d27142e0609ca250c975e4c4c1a5d995d23935b7bfbf7b1e078693`  
		Last Modified: Fri, 06 Jun 2025 17:41:07 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356d86d87b034c96a774a28e8b8a105305542681920c0548e7f06b5fdd0c5ef9`  
		Last Modified: Fri, 06 Jun 2025 17:41:06 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc65a3950e1d535070a02343fde57eac1ca07fd7f82760fb4173c48e10593efb`  
		Last Modified: Fri, 06 Jun 2025 17:41:10 GMT  
		Size: 13.6 MB (13640115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b783d442df08bbbce965615a932531f0fab544e741dba3d49cf0f9385c65835`  
		Last Modified: Fri, 06 Jun 2025 17:41:07 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02be7b22c4684b6352aae20b0b0879d6858fe132a8b43135543acce9aa36e1b5`  
		Last Modified: Fri, 06 Jun 2025 17:41:22 GMT  
		Size: 26.9 MB (26882803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ace010a734b076b90f0fda3353ac8eec6f2091bc3ea001174d01db78a3175f`  
		Last Modified: Fri, 06 Jun 2025 17:41:08 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88cf5d58e2ebb8dd558b050117c225af11dd79b2233794eedec91d3d1842f414`  
		Last Modified: Fri, 06 Jun 2025 17:41:09 GMT  
		Size: 19.7 KB (19705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:3530151ecf51f31af88c1c2bd50a3734c3bb41218b64f78b010feca4c8dfa0b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 KB (303756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613219e4abb6c99224ff0302af0c2343ca5cee3dcf3f42277e80ad408dc52abb`

```dockerfile
```

-	Layers:
	-	`sha256:e8798ba59d55b8b3cb0bed173b7420ac7f3c770f4b5d82b94468e234dcde7b07`  
		Last Modified: Fri, 06 Jun 2025 20:00:32 GMT  
		Size: 266.5 KB (266510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cf0cb963dd00553aca4e65da828875f8ed5e5ff15872b94bd75fa4c39e69801`  
		Last Modified: Fri, 06 Jun 2025 20:00:32 GMT  
		Size: 37.2 KB (37246 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine3.20` - linux; ppc64le

```console
$ docker pull php@sha256:9aa0ad6f1fa5da74d7daab7024bb8497e2250afede63b8c436b89d57acda8921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48308694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7beea5d1e9912c66776161f8ab1af8f54f8a9098256078d093c2ee7d8b6725a7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
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
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 14:35:49 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72cc4c14b8946c2696be57abc643eab432e324e1bd43edc5bec26ac34311058`  
		Last Modified: Fri, 09 May 2025 01:56:44 GMT  
		Size: 3.4 MB (3440259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a44720cd36e25286e3fe13210059745ae46fcd1a1ed0435a47f5eb47216db1`  
		Last Modified: Fri, 09 May 2025 01:56:44 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a93263d9053d935be58c6674fdaf718b11aa8ad8cfcf4a32c6d68953e57281a`  
		Last Modified: Fri, 09 May 2025 01:56:44 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4bd5e1190017a1cb6b23206db8c1fd41bb30a738d908e06b45a95e1d188159`  
		Last Modified: Fri, 06 Jun 2025 18:08:30 GMT  
		Size: 13.6 MB (13640125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232a356d641fd2bdbedc52aa7b3176707723ac3ad000314ded2f77e9b4a71e52`  
		Last Modified: Fri, 06 Jun 2025 18:08:30 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90637c61eaa0d8f5a80fec084af4c50686e98a20a09d01a16c630e18725670a5`  
		Last Modified: Fri, 06 Jun 2025 18:15:30 GMT  
		Size: 27.6 MB (27629042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc591eb6290572c12c76020af189c5101a1bdb3c9d5ec4766a1ca50c710f065`  
		Last Modified: Fri, 06 Jun 2025 18:26:45 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c0df4791d78984b6e9cb4639997dbb39cecdfb7247a5dcd278b907eaebc137`  
		Last Modified: Fri, 06 Jun 2025 18:26:48 GMT  
		Size: 19.5 KB (19482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:c5c2e396fdbad6dd0c63b591307a1087e824049a672029e6317eeb697fcffa79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.9 KB (298922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69bd839131c4bd32574768bc7142aa01820f1ca45b3a60ddb1953b97505700f`

```dockerfile
```

-	Layers:
	-	`sha256:b2ccdb37d054096f7f310f873088da5deb7c010b3fb7ec025c11c0cccfe5cdab`  
		Last Modified: Fri, 06 Jun 2025 20:00:42 GMT  
		Size: 261.6 KB (261580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24885d5bd9c3652fb9a2eb2f3021b5376ed59d64e99251eb5e936e976fc420f1`  
		Last Modified: Fri, 06 Jun 2025 20:00:42 GMT  
		Size: 37.3 KB (37342 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine3.20` - linux; riscv64

```console
$ docker pull php@sha256:f53a43c482be5dc79bfb31dcf0def37b8589f31411dc3ded1b85cf139906f7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46503024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a42bd19007ed6af9941f620d4a183aa121f3b35df1a604f8ba9577e22c50a7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 08 May 2025 18:45:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 08 May 2025 18:45:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 08 May 2025 18:45:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 08 May 2025 18:45:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 08 May 2025 18:45:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 08 May 2025 18:45:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 May 2025 18:45:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 May 2025 18:45:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 08 May 2025 18:45:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 08 May 2025 18:45:09 GMT
ENV PHP_VERSION=8.4.7
# Thu, 08 May 2025 18:45:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Thu, 08 May 2025 18:45:09 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Thu, 08 May 2025 18:45:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 08 May 2025 18:45:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 08 May 2025 18:45:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 08 May 2025 18:45:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 08 May 2025 18:45:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 08 May 2025 18:45:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 May 2025 18:45:09 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:69ccf1207daf2e3c381041f63cfe024189987fde3b1e97110475a71eac2581ba`  
		Last Modified: Fri, 14 Feb 2025 19:30:36 GMT  
		Size: 3.4 MB (3373232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f78faa668cf7c574dd9c2d56f59a6bc250dc74af7e4e18fd9791effe1480d2a`  
		Last Modified: Sat, 15 Feb 2025 14:08:16 GMT  
		Size: 3.4 MB (3433648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb3f638d71f849a7c907c65e1460552ada965ad760ca4f24c59cf89e1f65e23`  
		Last Modified: Sat, 15 Feb 2025 14:08:16 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87af6ac6ee454c1a8ef152ca8385e86f0d68ce72adae1c15b5ce36f9a3634e22`  
		Last Modified: Sat, 15 Feb 2025 14:08:16 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f134827737dc95e5aeffde821c569fa01146dca1af1de78592dceeb4ec13548b`  
		Last Modified: Fri, 09 May 2025 04:08:20 GMT  
		Size: 13.6 MB (13638115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025910094cf44270bae13305d6d88a55a080fc27029de0afd5639b52da2f3c8b`  
		Last Modified: Fri, 09 May 2025 04:08:18 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4980899425d2e88fc06329f46ca4e3ad40c8cdd87f37f796216da3cf89f40347`  
		Last Modified: Fri, 09 May 2025 06:06:13 GMT  
		Size: 26.0 MB (26034423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe5bb8e979fa0f83cda4045847f917f405600af4b8d73ab0d0f9d7dd43dca25`  
		Last Modified: Fri, 09 May 2025 06:06:07 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c9abc652820361a8d09d8f41bd205c9d89e8c18a7ec2860d8000752ebd34e2`  
		Last Modified: Fri, 09 May 2025 06:06:06 GMT  
		Size: 19.5 KB (19499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:20a0e5c8f60db558712d0d498c13c7e6d09ee9fee5e708d8a549b9914907be9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.6 KB (295551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c93889a781aa6f0e8e5e538d63b253db250ffc786ac1921ccc50eebfb412dd`

```dockerfile
```

-	Layers:
	-	`sha256:32f4ef04a1b5592f9494fc2e83709bcb4715df963ff2b84325e98a6161add770`  
		Last Modified: Fri, 09 May 2025 08:41:05 GMT  
		Size: 258.2 KB (258210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a27a37eb1caa4e851e28663e89735892f2578788a93dbda7d6056b6d1ab340d4`  
		Last Modified: Fri, 09 May 2025 08:41:04 GMT  
		Size: 37.3 KB (37341 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine3.20` - linux; s390x

```console
$ docker pull php@sha256:7dd08a3e96530b241e258883fb48b552c42cc26f341ca1fe1dc4160233324801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47901532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bbda787cd586611ea591392f14183b2d254b5848c69c707c4f9ec8cb6cf7bdd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
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
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 14:36:22 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b51761754164317abf3a048eab04b1e9d7242eea2f2ddb56edb014ca1521ee7`  
		Last Modified: Fri, 09 May 2025 02:06:08 GMT  
		Size: 3.5 MB (3507195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b99d984a879d65ca26f1c14f24481ecaf885777889ea2da9244d9de3b0d931f`  
		Last Modified: Fri, 09 May 2025 02:00:35 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a833716061e3e27c54210c327d3ba9133d0cff91bb31eee70ae2317d20da3cf2`  
		Last Modified: Fri, 09 May 2025 02:09:02 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5929c299c74cd21ab1cf406167c70af4f5e28f1316231d38b6d48e2d84fe91aa`  
		Last Modified: Fri, 06 Jun 2025 18:03:50 GMT  
		Size: 13.6 MB (13640109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8d741a8d0484110626c93a98bde325bd68936939d0d5287694064c1f998d3a`  
		Last Modified: Fri, 06 Jun 2025 18:03:48 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa26f363cc4ce99451bb3995db4b923a0b3b42217fb3ba110dbb738942583082`  
		Last Modified: Fri, 06 Jun 2025 18:10:50 GMT  
		Size: 27.3 MB (27266515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c0730225b7f0ae07924c1257449c188eb3878b320465ef93ae5899fb67e4ab`  
		Last Modified: Fri, 06 Jun 2025 18:10:47 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3914526b646d5d8daf82e25bc973e8522c73a95da1a47b3dc89fd4dd80719b6e`  
		Last Modified: Fri, 06 Jun 2025 18:10:48 GMT  
		Size: 19.5 KB (19493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:6893b0d7124008f8081f98c4c8c17693b0514eada9b57cc37ed9e17db9a58eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 KB (298834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e42bec33a9419704411d38226b78c4253edb070d275d07e6c0c6f966827601`

```dockerfile
```

-	Layers:
	-	`sha256:e37d3656d7a6b3e1b02b068e74ecab1808d1565ca61849e8be6120add3fc32de`  
		Last Modified: Fri, 06 Jun 2025 20:00:58 GMT  
		Size: 261.5 KB (261546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24aec178b7ef77adb3e6be1990973425ba1638adadc8284f7419a71e75ee2018`  
		Last Modified: Fri, 06 Jun 2025 20:00:59 GMT  
		Size: 37.3 KB (37288 bytes)  
		MIME: application/vnd.in-toto+json
