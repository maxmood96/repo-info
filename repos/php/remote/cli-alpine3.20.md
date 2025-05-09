## `php:cli-alpine3.20`

```console
$ docker pull php@sha256:3719321d500b29a7718b2ee2528a3494ffc6da7df33695dc5b80383e92c29416
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

### `php:cli-alpine3.20` - linux; amd64

```console
$ docker pull php@sha256:07160e81df7c0a33ac8286140a19e48e2308e847f0211f398bc89e14a15d4cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41411801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed82fe2c2855bf7b1dad3bd24a70a22078e2b57dda480a56811e1a3dce7f77d5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd488ab83751cfec75b2dfab5e7c4775bb09764990f0f69d38d0eac5d2acf60`  
		Last Modified: Thu, 08 May 2025 23:03:37 GMT  
		Size: 3.3 MB (3313805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348f1c83998d7f4b241a45c555ba966101f7e7837db003508a3d8cfe09ddb6fa`  
		Last Modified: Thu, 08 May 2025 23:03:37 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8904082336ba6d37fb1e0e3823c2095844b64895858c43285e873e3e87f3a695`  
		Last Modified: Thu, 08 May 2025 23:03:37 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a66866ca38c36c6c7fe8436f526efb2b26b73935ec21aa9c5889d99cb75324`  
		Last Modified: Thu, 08 May 2025 23:03:39 GMT  
		Size: 13.6 MB (13638102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82188cd6afbefec86d7a6dde1afe62458fa5ede50ed5e37f498e198e8733f2a6`  
		Last Modified: Thu, 08 May 2025 23:03:38 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23943e451988e10c8afda91618988a47f05ce38fd25b9992bebd1381d707bba9`  
		Last Modified: Thu, 08 May 2025 23:03:39 GMT  
		Size: 20.8 MB (20809204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7f64f1267777232a364b5c5a89cd65f48e81bec2090b2c7b77eb9c6989e7c1`  
		Last Modified: Thu, 08 May 2025 23:03:39 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3351bce3869eda6d32b00ca98d936953cabf8690b9c934df890a97b933cde6`  
		Last Modified: Thu, 08 May 2025 23:03:40 GMT  
		Size: 19.7 KB (19703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:cli-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:47496f9816094f1ff04059d1150c730a93d85e0726889f6f750f2a9ddac0d9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 KB (300927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14e6790523967171f01df7b35fac098f373c5fa0447d37c790110801fe89734`

```dockerfile
```

-	Layers:
	-	`sha256:bec8b77c2a65a63463e66ee9280003e01d7109e15b594e4598fc06db9573cafb`  
		Last Modified: Thu, 08 May 2025 22:54:59 GMT  
		Size: 263.0 KB (263021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be346cccefe5a070e5aa08c30982388f991d6bc9446fd9370ca59a4823764c68`  
		Last Modified: Thu, 08 May 2025 22:55:00 GMT  
		Size: 37.9 KB (37906 bytes)  
		MIME: application/vnd.in-toto+json

### `php:cli-alpine3.20` - linux; arm variant v6

```console
$ docker pull php@sha256:7c46be0c3f9ae26fd9cbe6642aaf78f1c63d1de831d5aa2ef51904c4a135a1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39566323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c92bb48463398e63bbb5c2b747202b2da92799fb4363036dadd257d2c626387`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:c8dc9531ae9517fd60474f3917cdd66ccce7d5ba37c0e42a0ed6f037a0ae729d`  
		Last Modified: Thu, 08 May 2025 21:39:48 GMT  
		Size: 13.6 MB (13638120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e946172571716f8664926da67e083f4de47c7822a33dc739878efe23d8ae4c18`  
		Last Modified: Thu, 08 May 2025 21:39:46 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf852f9acbf1989bfe967835a5fde699c0b680de50375000df0e904fc6f4219`  
		Last Modified: Thu, 08 May 2025 21:39:50 GMT  
		Size: 19.2 MB (19233805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f918e36f14dcec634099d51342a16de8e1ef0ff9088e17d587766bdfd55fc28`  
		Last Modified: Thu, 08 May 2025 21:39:47 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc95a89cb067e919c7ef8af2253b84a97c3d71c1516caea6b3a4793999307c39`  
		Last Modified: Thu, 08 May 2025 21:39:47 GMT  
		Size: 19.5 KB (19502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:cli-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:979b3c10573023949da5e4460aa7cdd4f5e80a429409396dc1c606261d18298d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a79b9e19cc58d9e3fd11ad581828892d69cb53cd9a3708f5767337435912821a`

```dockerfile
```

-	Layers:
	-	`sha256:975f7ff0e99d2f6997aae5172400e65215e1ce564d1f908027e1beecc1089c27`  
		Last Modified: Thu, 08 May 2025 22:55:03 GMT  
		Size: 37.9 KB (37865 bytes)  
		MIME: application/vnd.in-toto+json

### `php:cli-alpine3.20` - linux; arm variant v7

```console
$ docker pull php@sha256:91ff8adccffcdd7c8df90378e3acc37edb2463970f51509d69ec6947ce316a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (37978546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df1520063b6fcf58a49a9a792ff07f6f9c958d06edd02784738abf5b1811bee`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:e8264a5478fce8bdb4ad907387dcacf7051d3a71a43cf8c5758c0492414f6f3a`  
		Last Modified: Thu, 08 May 2025 23:40:52 GMT  
		Size: 13.6 MB (13638112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae3177c593b36416199f71e95602afec648c2d41647b6c78ed0990f6571450b`  
		Last Modified: Thu, 08 May 2025 23:40:50 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c5282f79965df61c9f00a864866bc9fba87b66f0b545d4c075682bdf32efaa`  
		Last Modified: Thu, 08 May 2025 23:40:54 GMT  
		Size: 18.1 MB (18116202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba69cba90576441ba60beffd5e76f5726e226a64ef645cafea1da42bddda985`  
		Last Modified: Thu, 08 May 2025 23:40:50 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ca181370ff32da2b01b1771368f22f36af4e5510097249190eb6bdf57e404b`  
		Last Modified: Thu, 08 May 2025 23:40:51 GMT  
		Size: 19.5 KB (19514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:cli-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:38eac85d21c1963babd46cd74254f2e4c81825c67b361b2182c6b02769094795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 KB (298308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ec16e11d4f6f7fd0f02e528c53c694295af5617a5dc598269500dc57c0f800`

```dockerfile
```

-	Layers:
	-	`sha256:96d30dfdd7e264acd518876432c33a9c74f5b26c2c6c8670ff8383a31661e6c5`  
		Last Modified: Fri, 09 May 2025 01:55:06 GMT  
		Size: 260.2 KB (260228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4818f12fc7195f51ebd6f5725200ae6c254eaad80d86d8bf8cdefb9dcaeb7be`  
		Last Modified: Fri, 09 May 2025 01:55:07 GMT  
		Size: 38.1 KB (38080 bytes)  
		MIME: application/vnd.in-toto+json

### `php:cli-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull php@sha256:6817fa3115b68625568b39c3bce50f75f196846313362670d058ba0d5a33f06a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41533115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be5174be4bb66436d1302967bfd48ea5ec9afade6f9b0a9671852ae7c3c121c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0591d05ec1aa85f6e2727eba86850c3694f8943058bd5b08d774e11cfa0b5f85`  
		Last Modified: Thu, 08 May 2025 22:46:21 GMT  
		Size: 3.4 MB (3365210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73872144433743769b2cf4ccefc2ab8fe7fa91cf352ec222abe941d8b351fd9`  
		Last Modified: Thu, 08 May 2025 22:46:21 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf361011faf88a180c9c1b01639ab94213cfbff5067f942216f462849133823c`  
		Last Modified: Thu, 08 May 2025 22:46:22 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afaac84bd8947641a21ef393c60d7d6f3498d1976436b6d71df299f28605648`  
		Last Modified: Thu, 08 May 2025 22:46:24 GMT  
		Size: 13.6 MB (13638105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa64937cfab682412e3877310ce53051e29147c00d77f8ed46448cec0fff541d`  
		Last Modified: Thu, 08 May 2025 22:46:22 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc0bb66330f4ac84baaa47b41c3ddb109de22852f474ca05ed60b5d49547558`  
		Last Modified: Thu, 08 May 2025 22:46:26 GMT  
		Size: 20.4 MB (20415064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abce6e1de58aa75f915b637773498e9090daf500c8fd9976861da5afaeff094e`  
		Last Modified: Thu, 08 May 2025 22:46:22 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a08330eaab67a3cad8f1dab02acb59269f41ef7010f99a6fba5f155039263b`  
		Last Modified: Thu, 08 May 2025 22:46:22 GMT  
		Size: 19.5 KB (19483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:cli-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:3458ed3fe63fb3466c05c7622014e1aa94a539e75f2afb90f0b03cad82cf94b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 KB (298398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4369390339dfc65ff82f835deafc58038375147858de8571853e3d17d3c956c`

```dockerfile
```

-	Layers:
	-	`sha256:6b6844bcfe0e29ba9ea956108c8fbf3504878f17f2c838d878fd39b7d7ee8898`  
		Last Modified: Fri, 09 May 2025 01:55:09 GMT  
		Size: 260.3 KB (260264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ef8d73618353cee7d26250d8c05f12f41bf6bd4c40cab3fab24c5859971f349`  
		Last Modified: Fri, 09 May 2025 01:55:10 GMT  
		Size: 38.1 KB (38134 bytes)  
		MIME: application/vnd.in-toto+json

### `php:cli-alpine3.20` - linux; 386

```console
$ docker pull php@sha256:d854bffcfe0782ba65877561fa968068454dc8ef3b135f6d437b28f415099c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41843596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54890136ad681ab2e57a4f1a673ced4a27b5902fd82bdd709c289cbb1eee39fe`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 14:36:27 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15eb6f7494317e6d5b5d1a16335bae852c1e7c5c5cc1eeb9a218306206fda2ab`  
		Last Modified: Fri, 09 May 2025 01:18:24 GMT  
		Size: 3.4 MB (3365391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480828aa0a2bd9f8755c7a33ee788c112c1916c494c8a0f38604984f7bcb287e`  
		Last Modified: Fri, 09 May 2025 01:18:13 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c12c8abb01758f166222dc560fb62ca74c73e1096bdc96610d77a9015cb73a`  
		Last Modified: Thu, 08 May 2025 23:04:18 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c68dbc88bb30d9a4ac95a811bd680730d444de636e60a741b4731f268e6cec4`  
		Last Modified: Fri, 09 May 2025 01:18:10 GMT  
		Size: 13.6 MB (13638110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0915e657a6607969234dd8af86febf7dc3cdc9a67be7fbacd7e7ef29dbfd61`  
		Last Modified: Fri, 09 May 2025 01:16:37 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2635f025b3dd84c230b2710217b30e2df9f24242dbd29946ffc2fa2c32e5027b`  
		Last Modified: Fri, 09 May 2025 01:15:21 GMT  
		Size: 21.3 MB (21344628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8018201e253726a25d2efb695c7763768042ab8a025134c067b79e4fc922c0c9`  
		Last Modified: Fri, 09 May 2025 01:15:17 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f1d1ed87e15afa2b94d74ec68c914c79471103af2bb43317b61a3e36cc2899`  
		Last Modified: Fri, 09 May 2025 01:15:14 GMT  
		Size: 19.7 KB (19706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:cli-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:b5445ed9586163bd5fe17fadc51259f9f9e96e82f9af3a5119755b178a49d627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.8 KB (300820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429020368b7678a406b8566786f7a33a719d42164ad7a8425d265549fa2a72d5`

```dockerfile
```

-	Layers:
	-	`sha256:5b497d89c0efd9681196ba7c529f07c2686fc9fa87e974ee6c309421e85f4b90`  
		Last Modified: Thu, 08 May 2025 22:55:11 GMT  
		Size: 263.0 KB (262976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ff37b03d7fef9d111d69b84abb6bc8949e64e0bf81d1cf97c417160b4f7e906`  
		Last Modified: Thu, 08 May 2025 22:55:11 GMT  
		Size: 37.8 KB (37844 bytes)  
		MIME: application/vnd.in-toto+json

### `php:cli-alpine3.20` - linux; ppc64le

```console
$ docker pull php@sha256:2352243528e3d7e6e6dbe14349409964f8affe68ec1776428fa970dc6fcb8126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42424825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac00d332cc4035acbd6515c8eec99c2756a50d2c2f5aaff29af11f8afe5a5a05`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:2e4ac4e90998ead82279b558960f371b832ec4bf205c42a6a9dad41d1d60da45`  
		Last Modified: Fri, 09 May 2025 01:56:45 GMT  
		Size: 13.6 MB (13638113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e21a47cb21933832bb54737774a1859aae9fa74499c10506c9a384bb9830bb`  
		Last Modified: Fri, 09 May 2025 01:56:44 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f142e3f9c226693c888bd1a36f8d4ac23cb2a32eeda467069f99560a26b15eb8`  
		Last Modified: Fri, 09 May 2025 02:42:20 GMT  
		Size: 21.7 MB (21747183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf2274a5c52df21b0e7a1e0e61b7ec96e62f4f96de3f84d084f092ef2b917d9`  
		Last Modified: Fri, 09 May 2025 02:04:11 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f89ecd3d42706a45a7b38cf8ee94811d730196ab20121c02fc9811f886154d`  
		Last Modified: Fri, 09 May 2025 01:58:06 GMT  
		Size: 19.5 KB (19490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:cli-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:a9133a46b5dff960f8e1ca60946604f1c6a4fc0cff460160801a43d90277ca44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 KB (296252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb73c62aecd58886d6648a94adf87c65f797313723bbaebe7ce915b3b41fb2e3`

```dockerfile
```

-	Layers:
	-	`sha256:c3454a8c46e8d61b0371e6718a231de804dc91606930cf511478ac4cbfc6ba7d`  
		Last Modified: Fri, 09 May 2025 01:55:15 GMT  
		Size: 258.3 KB (258267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad973ffdfac43845bc51eaf3a4b091409bc19bf60ece8d2fa352fe476e773381`  
		Last Modified: Fri, 09 May 2025 01:55:15 GMT  
		Size: 38.0 KB (37985 bytes)  
		MIME: application/vnd.in-toto+json

### `php:cli-alpine3.20` - linux; riscv64

```console
$ docker pull php@sha256:be24321aff4ca2c62d418cdefb681cc2a76820f2622592f08290fa1138ba7be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40921920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a3ea2da793f5e31818836ef5026d68d98c40a22068ea5848649aba4ce8e257`
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:7ab5f2ae2036902dcc7e51f1af6b00907e5c7249fc2be1e0e2f368aa8fedd2dc`  
		Last Modified: Fri, 09 May 2025 04:08:47 GMT  
		Size: 20.5 MB (20453320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4896fafa3bcd8d1178aa79ee5880c841388dbbfe35c9c8a640adf18dca096a14`  
		Last Modified: Fri, 09 May 2025 04:08:20 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2967f8986ccd694fc860ed511528d52416eecdd7e61715e5e6a32a98195852e`  
		Last Modified: Fri, 09 May 2025 04:08:21 GMT  
		Size: 19.5 KB (19498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:cli-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:a1107e3b4631fc5f1c535ab053447e766d163d19911d6c90ff639b9df8a5c1a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.2 KB (296248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3432fa3e0bc267a8fc1f4e0c5cdae8f25ae79785923a1d8d1d8599694416e7e9`

```dockerfile
```

-	Layers:
	-	`sha256:747e614f67fa53601ea361bd336cedb28f2a4c10c76743d02b171f0ede64fe97`  
		Last Modified: Fri, 09 May 2025 07:54:37 GMT  
		Size: 258.3 KB (258263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d51dc28a70544d4f6bd85b8f6144d036b02b43c98f106edefa3e796bc9fd66e`  
		Last Modified: Fri, 09 May 2025 07:54:37 GMT  
		Size: 38.0 KB (37985 bytes)  
		MIME: application/vnd.in-toto+json

### `php:cli-alpine3.20` - linux; s390x

```console
$ docker pull php@sha256:77e6bac323ee626b201a1ffe8ecf5994d1115d7ff7661486b9122988aa3f84fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41912060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7a7f101371977a0aee4bf463ecde9150d204c7076b4c8317e0c6bced9056ba`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:a47342b2c537d7ea82820d35479b12ba69991776d0448d5cd21f452d245b6a8b`  
		Last Modified: Fri, 09 May 2025 02:42:33 GMT  
		Size: 13.6 MB (13638098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3ce4aa4cb7e56ccbca555a58311d0cae38dc3c7b0c241b03b4361424b51b50`  
		Last Modified: Fri, 09 May 2025 02:00:18 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb7e54b34201745bb7f7a014dccf003acdb09e312cc779b50d7988ed3650a1c`  
		Last Modified: Fri, 09 May 2025 02:42:16 GMT  
		Size: 21.3 MB (21279058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783fab842127cf5687a14ab8cd8d3dfb6de42be3e8c78c9a6bfd7518459be50c`  
		Last Modified: Fri, 09 May 2025 01:55:48 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b443b0352b754aa1d49064143dd24ed316339276a5517077536b98fda9754bd7`  
		Last Modified: Fri, 09 May 2025 01:55:02 GMT  
		Size: 19.5 KB (19490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:cli-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:44fcba08fc9cd8061c24532968080122ef6d32c535de2a5c4cb473bd115e7b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 KB (296116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4719610ed8c70178f7e7fdf73ac3f7901ea6674600675ebd6dd44ff3b5cbba8`

```dockerfile
```

-	Layers:
	-	`sha256:716a02b1a4837ce6fd58487cd87119a06db2805eefd5f26707f942acd6f9ba97`  
		Last Modified: Fri, 09 May 2025 01:55:21 GMT  
		Size: 258.2 KB (258209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e888530a612bb246bdb3e39eb94eba9c0be10e624f4e8d218bf7ec102234b85`  
		Last Modified: Fri, 09 May 2025 01:55:21 GMT  
		Size: 37.9 KB (37907 bytes)  
		MIME: application/vnd.in-toto+json
