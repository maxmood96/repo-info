## `php:8-zts-alpine3.20`

```console
$ docker pull php@sha256:48b2a1b1544f34f4cb6b9e74589b49783d7375f27fc88935a6b7f4af05b30e20
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
$ docker pull php@sha256:d4de59dda2eb7c6b60120f61d64bd7949ffd5aa251fc28a27846019933b3fe84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46801346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc2d72ff06209f8e46ebd6c2da7ac26244fc284ca9fadd4ca1e4943b2b3c2a55`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 13 Feb 2025 21:31:38 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 13 Feb 2025 21:31:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Feb 2025 21:31:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_VERSION=8.4.4
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6084902a576dd2ed0a55e2baff723c6789271a86f5045a1f58f7e5880cdb72`  
		Last Modified: Fri, 14 Feb 2025 19:23:11 GMT  
		Size: 3.3 MB (3313889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff343e9f1e1070dbe44bf1cbff7254ace5709e26c12720239f1562f1261a6dbc`  
		Last Modified: Fri, 14 Feb 2025 19:23:10 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2bd07d759ecd4e3f249f6e5d6de11fd7509aa5c836221c877e53744af0b3a9`  
		Last Modified: Fri, 14 Feb 2025 19:23:10 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4b4075cd40d7ab5fbca6c438e8bcb3e8250328d143abdceffa03de088ffc6e`  
		Last Modified: Fri, 14 Feb 2025 19:23:11 GMT  
		Size: 13.6 MB (13609647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6ef3bb7f6f45e99e33dfe4d70f8ebd82848b5dc3bb126d65b0e5590015a9a8`  
		Last Modified: Fri, 14 Feb 2025 19:23:12 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a7dd85967b8e8e13ec1cd530058e1e8e2fb7088ab1a19aad8da00d23ebea44`  
		Last Modified: Fri, 14 Feb 2025 19:23:13 GMT  
		Size: 26.2 MB (26227114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e91191fb237242cf5a67c975754fe6039a9b5882d3c27ef6bf830364ebbdf6e`  
		Last Modified: Fri, 14 Feb 2025 19:23:12 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dba661d014977b58f258e8b5d7f5b1429b080d4568a9005dbbfdb3868c649c1`  
		Last Modified: Fri, 14 Feb 2025 19:23:13 GMT  
		Size: 19.7 KB (19708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:87a7f3b13cab38a91a5107b68059e61f008db2d7b87a4dfef2a81ffe166f4454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 KB (300279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612da146e52811769492628ae6cdb784319257db4cbaba180e7f2411c8862de6`

```dockerfile
```

-	Layers:
	-	`sha256:3348b7c23aeeca21eb7a3134b3a4c57f55af9938d187ca5706abcf11a2683baa`  
		Last Modified: Fri, 14 Feb 2025 19:23:11 GMT  
		Size: 263.0 KB (262992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d017fbc61eb214b8b3f1072f6f2e5b09cd711819100fa28c37afc786404d9392`  
		Last Modified: Fri, 14 Feb 2025 19:23:10 GMT  
		Size: 37.3 KB (37287 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine3.20` - linux; arm variant v6

```console
$ docker pull php@sha256:9d5b0b0c76f81d9999483cd907741d721ce036f1d5e81a8f8dce8376511b42ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44622142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5142a5c992e2d4b99df01812b4017f9a83742067fbd6bca14d63a00c8e90ff0a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 13 Mar 2025 17:27:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 17:27:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_VERSION=8.4.5
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 18:28:14 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c0f79d4d985a64f9865dca6388accc72536a8134bb71d173eb4214c357889d`  
		Last Modified: Fri, 14 Feb 2025 20:14:52 GMT  
		Size: 3.3 MB (3298263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ffe6d763475cabc6526162b5d931425de2a4941987a9a47a37817994c917fe`  
		Last Modified: Fri, 14 Feb 2025 20:14:51 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82be80b03c756f18e75ec416857bff7aeee3ead6c2ab8410c9194efd506877e5`  
		Last Modified: Fri, 14 Feb 2025 20:14:51 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a1f17aebf1957169ef43b2af83c2333b23e4ca4a266ad12d3863d614e32bf6`  
		Last Modified: Fri, 14 Mar 2025 00:37:11 GMT  
		Size: 13.6 MB (13625746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0309d58b9f9a9e15d8d38abccc35ae2eb6735b6a379aa84a013cc8806f5c2072`  
		Last Modified: Fri, 14 Mar 2025 00:37:10 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8d128a7733242b820774e44229937682d35dde255d0af9b2cf186c193e136f`  
		Last Modified: Fri, 14 Mar 2025 01:30:16 GMT  
		Size: 24.3 MB (24302000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c257e3c8eb7077b0c4558145410b2faafc1d492c273298f8e968ec3a5213be`  
		Last Modified: Fri, 14 Mar 2025 01:30:15 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4dde2845960e3e4c78a95bfcd5791953b8c74296c6502e3402790f58d7ef48`  
		Last Modified: Fri, 14 Mar 2025 01:30:15 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:02f83be264d7211a569c38ea55109c85d65b72ba1e7cad8e06efccf50d01268d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 KB (37213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b162ae5b0ed185c2d4dcc6745cb3474d78aa4d917c9e58d914d1da80ddaf6751`

```dockerfile
```

-	Layers:
	-	`sha256:6483d86ae8a6204c65c84c9e87c7459e5df94b5fada7b498ecdd3fd2041453b7`  
		Last Modified: Fri, 14 Mar 2025 01:30:15 GMT  
		Size: 37.2 KB (37213 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine3.20` - linux; arm variant v7

```console
$ docker pull php@sha256:78dc13e9bccb178b7a72521af953b285244f576e0be2380556352958285cc4d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.7 MB (42681306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d558a06ffdbc3a26a7443e72bd114bcd218c4e153ed5d30cb71ec1e1d83184`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 13 Feb 2025 21:31:38 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 13 Feb 2025 21:31:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Feb 2025 21:31:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_VERSION=8.4.4
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f435e04ea18170faa15db5a195b7a456fd6855803819a3ec1feb1150cc547b`  
		Last Modified: Fri, 14 Feb 2025 19:57:13 GMT  
		Size: 3.1 MB (3104652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6d965c1f9e2eeb816a67542a273f236e46e8776d2aaeabebc43098c502ee68`  
		Last Modified: Fri, 14 Feb 2025 19:57:12 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151a378a33b3d6443d5e2151a40e50e2c7f67f3b501115627d75e1ce417f91c7`  
		Last Modified: Fri, 14 Feb 2025 19:57:12 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2081f27c5add62f3abdd10359086d7c7de1fca9aac3bb0cb334b5a0ad175ad5`  
		Last Modified: Fri, 14 Feb 2025 19:57:13 GMT  
		Size: 13.6 MB (13609638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2726418c80eb5c4954c50ae3fc9a5992152257e7d79689d82f4e73c8065f30`  
		Last Modified: Fri, 14 Feb 2025 19:57:13 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff1eeef39e8863bc19cbe38ffef1ddf2e479a6db67f45a903be9b021c413b3b`  
		Last Modified: Fri, 14 Feb 2025 20:05:00 GMT  
		Size: 22.8 MB (22847448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd1a4ffbc17b62b041d0880873ce2d1b125f7b7f30d11b8487d4ea30e853a03`  
		Last Modified: Fri, 14 Feb 2025 20:04:59 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cb85b8aaa5afe597ec3b8183bf7aa98983719d1bcc5e3318da97a84315f563`  
		Last Modified: Fri, 14 Feb 2025 20:04:59 GMT  
		Size: 19.5 KB (19506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:9158ff4502764823d2d57e8509a800afa91efd9274752637b8dcad3c3ed462d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.6 KB (297596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb256dc6846cd70ee7206cb48990629e331e87ba47fe739b61ca7d2b19a575e`

```dockerfile
```

-	Layers:
	-	`sha256:9c9ab8f11e63b98d114b7f77d2724d0d59db9931e2c44ccbe73cc9126fa3c5ea`  
		Last Modified: Fri, 14 Feb 2025 20:04:58 GMT  
		Size: 260.2 KB (260167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c64f30e3a398bd737db846231eccff38e9a0b87cfc7e9a17a318d1f19ea1cf1f`  
		Last Modified: Fri, 14 Feb 2025 20:04:58 GMT  
		Size: 37.4 KB (37429 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull php@sha256:009fe48d540de93df77c4212df119f09d12e55a46e58d4aa3fa49d608cda24a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46977096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d2721b0e3536013bfdb8e64c5d77a0cee589fca8d586888f29cb0c80b6d6a0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 13 Mar 2025 17:27:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 17:27:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_VERSION=8.4.5
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64278622ee4008648cd0d08a890af70672bfae53a983eb2b10fe4a65ed3b936`  
		Last Modified: Fri, 14 Feb 2025 20:06:51 GMT  
		Size: 3.4 MB (3365209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95666ce1b88aa4cfd448a2dfecfe7a221115807ae27fb0bd41f2d5920815884`  
		Last Modified: Fri, 14 Feb 2025 20:06:51 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa970535345bac62ab689111e4438c3ed5b2c57f743763f4381c198f307d845`  
		Last Modified: Fri, 14 Feb 2025 20:06:51 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce95fd188c67967a5908cfa5e40650ce73a57eeec9fa9d0f0e749345554e995`  
		Last Modified: Fri, 14 Mar 2025 03:03:26 GMT  
		Size: 13.6 MB (13625734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfc3496ad4af40ec8e3347372cd5065bd79f5b5ac2c0a62f9062822a5a928c9`  
		Last Modified: Fri, 14 Mar 2025 03:03:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4993ca131a12e73df2d3bfe0bc43e744873344cb02eff38cbbc8aaef004a5e0`  
		Last Modified: Fri, 14 Mar 2025 03:03:27 GMT  
		Size: 25.9 MB (25871422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf852bce35ffedd590ec59c98e68cc67c991e39bf1f9d6a0ba08706585e5007`  
		Last Modified: Fri, 14 Mar 2025 03:03:26 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e9dcfdfd8bbfece954986fe27561796047654a6a50c9981eca2a17b9630220`  
		Last Modified: Fri, 14 Mar 2025 03:03:27 GMT  
		Size: 19.5 KB (19471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:fe7a6ca1cc1ab3593b7ba29af83c827ff3695b1e4d863b23249d77802cbc094b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 KB (297654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b25290e277b85b6c71dafe876152544457abdabe4c185b201dbeec56a5a675`

```dockerfile
```

-	Layers:
	-	`sha256:fbeddac5d89cf2bf4f6453b1cab6478143d93dbaf651aff90fac2fe63f131a00`  
		Last Modified: Fri, 14 Mar 2025 03:03:26 GMT  
		Size: 260.2 KB (260187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffeb3e813e775b6b76e7270efae528f23cfcc45643f39a3f2a8767f13987f8fd`  
		Last Modified: Fri, 14 Mar 2025 03:03:26 GMT  
		Size: 37.5 KB (37467 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine3.20` - linux; 386

```console
$ docker pull php@sha256:c78e37ce1097cd29e7ccb279395639a6e10e218551240659d4334ab17b1033c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47315013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe2fe2753ec0e91f88b890ac7cc91def0962542d64194196da8c8abeebc37b0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 13 Feb 2025 21:31:38 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 13 Feb 2025 21:31:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Feb 2025 21:31:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_VERSION=8.4.4
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8861e48547296b015529274970b88802cf57c958e57dde8d261dae3832127fbe`  
		Last Modified: Fri, 14 Feb 2025 19:23:25 GMT  
		Size: 3.4 MB (3365481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907c00ec80f4f85ffd498bbeb8fc75104bd24e2b11c393aea895bcac9d2fe084`  
		Last Modified: Fri, 14 Feb 2025 19:23:25 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52408df4ce6a6f581feba8557725b240c273b916f37b47d7e7e5c1debc7af4f0`  
		Last Modified: Fri, 14 Feb 2025 19:23:25 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ec1b73d1bc90d00e19e3e0b76ac5dee153f7f92a3d57d3e8e2fa3b381a16fc`  
		Last Modified: Fri, 14 Feb 2025 19:23:26 GMT  
		Size: 13.6 MB (13609643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f0d2b045dbd339798c1bfdb2238c1e6a46e9ac37928aa53b3993dd4d3465df`  
		Last Modified: Fri, 14 Feb 2025 19:23:26 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae86eda79fdd9f99725c56b861ce434182df3c2c1cbcdd71f8eed583c933fc10`  
		Last Modified: Fri, 14 Feb 2025 19:23:27 GMT  
		Size: 26.8 MB (26844420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f568114ffe3f80242d9cdd3ed8650cdf8cf028cdedfae49d803c27042b80eac`  
		Last Modified: Fri, 14 Feb 2025 19:23:26 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efc2c2346a2613f84d4fbdb0145182ecaff7c06ff8a91914156895b032cdbae`  
		Last Modified: Fri, 14 Feb 2025 19:23:27 GMT  
		Size: 19.7 KB (19709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:3941c31d89d1fb101f692bb7e57fceeeb5eed046ec4737905d8b435e032f711c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.2 KB (300213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff27e5df8f38d5fdd64bb9197fcaf47479f26bb934efe269cf2d5b596b5b9d5`

```dockerfile
```

-	Layers:
	-	`sha256:2d2f0ff7babefcc331ce4d6b9febfd2ae40e20cb38b49359a6c9ff5bae37a57d`  
		Last Modified: Fri, 14 Feb 2025 19:23:25 GMT  
		Size: 263.0 KB (262967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89ac3489dac1c0839a7cbb03fb201f3c7dce01d3ac6fef0566ef15578f989f8f`  
		Last Modified: Fri, 14 Feb 2025 19:23:25 GMT  
		Size: 37.2 KB (37246 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine3.20` - linux; ppc64le

```console
$ docker pull php@sha256:105333c7faa0f557adbaaaad6e348c4ce11452d427857c600661d50654c4b8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48288014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f08a2a8344b9187eb2159f2dda35f7cad6da16215cef946d6dfc4316ddaf7a7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 13 Mar 2025 17:27:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 17:27:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_VERSION=8.4.5
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718db6fd9663f5523b8df9dc0bcd9d39b076fe66cbf8b070276f7f03946d69a3`  
		Last Modified: Fri, 14 Feb 2025 20:00:10 GMT  
		Size: 3.4 MB (3440270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a6b0a520a6ed496f43bb191ac088029379c10ac94401a28b7441591d37bfae`  
		Last Modified: Fri, 14 Feb 2025 20:00:09 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d31ee6d075a91e74c7b2a672c463e871265f9016719d4905ed788b321d083a2`  
		Last Modified: Fri, 14 Feb 2025 20:00:09 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc6130d8dcb5196ba7130d4f5b735fe0da73f4eb6baab4c8be25c13132fa111`  
		Last Modified: Fri, 14 Mar 2025 02:24:31 GMT  
		Size: 13.6 MB (13625749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d06f382ff8442ae5371fbb1f31be32b42ffb3547ab4dc3d9ac0b8d474a7ca1`  
		Last Modified: Fri, 14 Mar 2025 02:24:31 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65dfd18b342d804b682e2372606d9bfbfc0501cb8daa43b10c56d30213f0de7`  
		Last Modified: Fri, 14 Mar 2025 02:24:32 GMT  
		Size: 27.6 MB (27622735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed0aac28a536bf9ffa1f92bd753bd0fe503ed39a21e2263cf9efebefe517699`  
		Last Modified: Fri, 14 Mar 2025 02:24:31 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c1d5b96a1b0a82eef5ae3f3c635fa2bb15a1ca5e9beccb8f6c6933aabf72d7`  
		Last Modified: Fri, 14 Mar 2025 02:24:32 GMT  
		Size: 19.5 KB (19476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:9cb9db2dae00d2435b29edf6978463888f1801682a3ac3395952c1b86e69364f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.6 KB (295556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25742ecb57f1cd3d7bb7469865e51bf8ef404f34449c03711d559ebd86f17ecb`

```dockerfile
```

-	Layers:
	-	`sha256:720c4360ab5a848514156afe8bee81417b09748a32375fe40e175eb72275a641`  
		Last Modified: Fri, 14 Mar 2025 02:24:31 GMT  
		Size: 258.2 KB (258214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aefcd32bf16386bb7e37aad561ecb95385e2cc2f9682f6b63d1866b6b3c4c7c8`  
		Last Modified: Fri, 14 Mar 2025 02:24:30 GMT  
		Size: 37.3 KB (37342 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine3.20` - linux; riscv64

```console
$ docker pull php@sha256:fd0ba241d3aba8cc9ea0f9038cb63b08d143c3224a5a4bc7a98e2228ce3c81b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46271730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1519baf5652f044297c0a04619921316500d944e936a07e673a4a3159c627e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 13 Feb 2025 21:31:38 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 13 Feb 2025 21:31:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Feb 2025 21:31:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_VERSION=8.4.4
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:69ccf1207daf2e3c381041f63cfe024189987fde3b1e97110475a71eac2581ba`  
		Last Modified: Fri, 14 Feb 2025 18:57:42 GMT  
		Size: 3.4 MB (3373232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f78faa668cf7c574dd9c2d56f59a6bc250dc74af7e4e18fd9791effe1480d2a`  
		Last Modified: Sat, 15 Feb 2025 03:36:13 GMT  
		Size: 3.4 MB (3433648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb3f638d71f849a7c907c65e1460552ada965ad760ca4f24c59cf89e1f65e23`  
		Last Modified: Sat, 15 Feb 2025 03:36:12 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87af6ac6ee454c1a8ef152ca8385e86f0d68ce72adae1c15b5ce36f9a3634e22`  
		Last Modified: Sat, 15 Feb 2025 03:36:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc5479694e06d5396dae49cb0a3b946de56bf9968c8f979ed01713a9fa01a0c`  
		Last Modified: Sat, 15 Feb 2025 03:36:14 GMT  
		Size: 13.6 MB (13609652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec4633d9f33632f85cad404366a6fae0c9b7f12b4c5ccece38be99698322fc0`  
		Last Modified: Sat, 15 Feb 2025 03:36:13 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f916b539efda0b3d014234623fe805dc984837d63b7c1a619c7f8ac27c90a5`  
		Last Modified: Sat, 15 Feb 2025 05:33:49 GMT  
		Size: 25.8 MB (25831594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ea30a45624ac6196470948b74e39339117dc52b4b3dfe8f19feffc4f711a82`  
		Last Modified: Sat, 15 Feb 2025 05:33:44 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312e7993fe9c95e7a551c84a04873c1a608177b0c69b769ef6b9d563d1a62e73`  
		Last Modified: Sat, 15 Feb 2025 05:33:44 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:b414a0188f4ae788749a824497a060ffcdc971c3d7c08ec8dcc8b04d56f1e76f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.6 KB (295552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424b6717d45327117d8d0d9b0cb16bfec06afc3355019d2c9c4596131e120eea`

```dockerfile
```

-	Layers:
	-	`sha256:90b8ab9a87f944115d5759fb83010b12cd6a9f95ffbb103e31d01e93de2378f3`  
		Last Modified: Sat, 15 Feb 2025 05:33:44 GMT  
		Size: 258.2 KB (258210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67d437ee588c7b1d0e3816f672adf9e873b1ae54bf3076e7d12d969f651e119c`  
		Last Modified: Sat, 15 Feb 2025 05:33:44 GMT  
		Size: 37.3 KB (37342 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine3.20` - linux; s390x

```console
$ docker pull php@sha256:88f45086133be0d30d1f5431b7b608159254a1e14535c670fc79b941985d0796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47874831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:505c1f990faefbbcbd924b604ee250418019101d7ddc429a5b2ce433bc56abfa`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 13 Mar 2025 17:27:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 17:27:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_VERSION=8.4.5
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4683ab30aba68efec0e2ca4cbd43732f742f065f5166f0823fccc53a1442ec2b`  
		Last Modified: Fri, 14 Feb 2025 20:05:19 GMT  
		Size: 3.5 MB (3507248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51174c28ade76e443d57a717e1e8717bf8083c3163cd3db4d02012e3c317ecc1`  
		Last Modified: Fri, 14 Feb 2025 20:05:19 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b8be851aac921eca8fd7c62858736f1ef819ffbcf1db33078cfa5c544a77a1`  
		Last Modified: Fri, 14 Feb 2025 20:05:18 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:decff49c6d6b69166870b14381ffffc9029262d645d876b382b21addabce293c`  
		Last Modified: Fri, 14 Mar 2025 01:51:03 GMT  
		Size: 13.6 MB (13625735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ea434c61a946bbd72b16c987bea43344dd683fcb57fbded4d73eda172be452`  
		Last Modified: Fri, 14 Mar 2025 01:51:03 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ae997b008cbb5a76d0026839df68b05985c6227a279342e79f4728515a8242`  
		Last Modified: Fri, 14 Mar 2025 02:05:35 GMT  
		Size: 27.3 MB (27254138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc901632c79eee01fa13139e4c1126926bc3350340e172b4b626ca38318d8232`  
		Last Modified: Fri, 14 Mar 2025 02:05:34 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db28f430215dec88fc757d827d16b14f59b3b631c12fae59d3710426d3abbc8`  
		Last Modified: Fri, 14 Mar 2025 02:05:34 GMT  
		Size: 19.5 KB (19482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:7419f8b4aef9438e1648006bed7e204377d7f8a31af7f564b7072cfeeda3d593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 KB (295467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58c3bcddc523fe671ca2f3ffa0c9203e5c488a9599f78eb62000e7fe289ddf1`

```dockerfile
```

-	Layers:
	-	`sha256:80610b1a9198c696994a18a5b98e5930ae81be58e34a41fb85f4ff4f83cf1104`  
		Last Modified: Fri, 14 Mar 2025 02:05:34 GMT  
		Size: 258.2 KB (258180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad738381c69e244e516744a19b402cde5554b16d59988b3254ec5b680179ee92`  
		Last Modified: Fri, 14 Mar 2025 02:05:34 GMT  
		Size: 37.3 KB (37287 bytes)  
		MIME: application/vnd.in-toto+json
