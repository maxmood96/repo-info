## `php:alpine3.22`

```console
$ docker pull php@sha256:0340b5c274e2b3b8315ad2628244851b7456629c0bc8e58431c4f8ebf08e35a7
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

### `php:alpine3.22` - linux; amd64

```console
$ docker pull php@sha256:7312bec7f935c80133ef7028fbf6d82d312be50fb833aa7f7fee0d405996352b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40930862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f15a9784f58526f27c331a278aaf911139ee1c3dee0231dd20c4018d94c347e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 25 Sep 2025 18:46:43 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2f8e296f161a6df6f9e38f530b29164527358ae5a835ec9540902834c703b1`  
		Last Modified: Wed, 08 Oct 2025 22:43:17 GMT  
		Size: 3.5 MB (3463764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a14574d9b443903c59a6beaf7e1bcf42b816683f83bfa06b936dbedd14d72a`  
		Last Modified: Wed, 08 Oct 2025 22:43:17 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a5ec08747e2aa91406eff3773626f48070eaa9c93fed1ba8f3d7a612080daa`  
		Last Modified: Wed, 08 Oct 2025 22:43:17 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6901834d8559b2c1803d20e64f1b861135d90a4a7a049abdeb15717307346efc`  
		Last Modified: Wed, 08 Oct 2025 22:46:36 GMT  
		Size: 13.7 MB (13667314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50bd3180ce9ecb80744aacb36dc0933c9d12b3332391fd411e067313fca537e`  
		Last Modified: Wed, 08 Oct 2025 22:46:35 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff98099a8db7c665ce7e7dd334499f5758ca075b1a9da6eaa66010b933dbac0`  
		Last Modified: Wed, 08 Oct 2025 22:46:37 GMT  
		Size: 20.0 MB (19953089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7dc8240588654a17245c46bbd1437bb7f3a0cef7b7c1913c120392c2744b44`  
		Last Modified: Wed, 08 Oct 2025 22:46:35 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da04ac4906203e5a1123b373aa69bc666c10b8af52b1b19d19a6dc6a1dce0f7`  
		Last Modified: Wed, 08 Oct 2025 22:46:35 GMT  
		Size: 20.1 KB (20080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b8cf85bbba77f139b425fb70a0e7ff062dc49b1b567d17d431182e88944851`  
		Last Modified: Wed, 08 Oct 2025 22:46:35 GMT  
		Size: 20.1 KB (20076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:4f851b239be0f0b0071e918374b4a14014faca3679c172d6dd752fb77ec05972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.1 KB (326102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c844e512fb22ca4a3d3d513b4f457f19217e028a4afc4f62a8bd2b1be90e915`

```dockerfile
```

-	Layers:
	-	`sha256:f92cfe7dcd4e9a81ecfbdf5ced18de046d2c5d857a8759bab2ebb6b60fcc3931`  
		Last Modified: Thu, 09 Oct 2025 01:14:28 GMT  
		Size: 283.0 KB (282988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34ed36c1eab70ec5928aceed9446ef5743486bb073ba0d705a49d572f2f2226b`  
		Last Modified: Thu, 09 Oct 2025 01:14:29 GMT  
		Size: 43.1 KB (43114 bytes)  
		MIME: application/vnd.in-toto+json

### `php:alpine3.22` - linux; arm variant v6

```console
$ docker pull php@sha256:c3ac7e260e8fea0c284ea0a7c17ca06d4f99a8773406da7f1186987d77d647e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38704718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05ba17492fb5b140d5869e89efaa61d457ee369f4f17b9d46827694caf195fa`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 25 Sep 2025 18:46:43 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3cdcb39afd821d13b22ca21c865ff19e58569c683f9e18b9a0ceb95c92b680`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 3.4 MB (3428334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8740db6975c9b8c5220191ade53612421b7da5301d9f3f7da94286205eb5ec`  
		Last Modified: Wed, 08 Oct 2025 21:46:04 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc4035a2fd0c27d5270cc96e2d8cfb3e6e50f6a5677241510df3134795ece31`  
		Last Modified: Wed, 08 Oct 2025 21:46:04 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af805f84b73172d2698327554e5ef818e84bd82d65b59787d50f39d913ec0719`  
		Last Modified: Wed, 08 Oct 2025 21:49:25 GMT  
		Size: 13.7 MB (13667315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ecd21a0f014808366ec5d7f9adbb28ba24786074378c263c9610a2c0b9c1cb3`  
		Last Modified: Wed, 08 Oct 2025 21:49:23 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d663aabedbb3d1ba629f80af329ccdf6c5a8b92c4cf49e3123e91e60a2fb04e1`  
		Last Modified: Wed, 08 Oct 2025 21:49:29 GMT  
		Size: 18.1 MB (18061177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658ad9203fc8268414c179c489dd5f4ce2c94d17d67435f5d22871139094f29c`  
		Last Modified: Wed, 08 Oct 2025 21:49:24 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fcf7c704cf2e4ccf1aea8964807324adcaeb6684d1ab689a54286b1e46e6e5`  
		Last Modified: Wed, 08 Oct 2025 21:49:24 GMT  
		Size: 19.9 KB (19859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6f9deaabae512f3463286ee62cee947cd5f939c7609e15dcd026bd4d4b2b42`  
		Last Modified: Wed, 08 Oct 2025 21:49:24 GMT  
		Size: 19.9 KB (19865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:72785ecfe949afe60bd7c4a4eee7a9b05e5522506efdb04105e9273c044b7a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 KB (43153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432d7edb89a73f44ab806e5b491e0cb20966222471e79019e5732e8c43f469d1`

```dockerfile
```

-	Layers:
	-	`sha256:143a3231d4745ea0f31563d18eff7529900493d829ec36862d861238441b8777`  
		Last Modified: Wed, 08 Oct 2025 22:54:37 GMT  
		Size: 43.2 KB (43153 bytes)  
		MIME: application/vnd.in-toto+json

### `php:alpine3.22` - linux; arm variant v7

```console
$ docker pull php@sha256:286ff7aab638f19ebff2027120be1eef966c4dac4df283843f7f97484a55e4f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37223947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e47e104dda4242e03f0db902511a8cd30ddbf8722f4c88689862a38dd425da8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 25 Sep 2025 18:46:43 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
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
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14232435a9d5a78b508485f7ba6646d09f5330d829ee27b6f714a9ff16408dea`  
		Last Modified: Wed, 08 Oct 2025 21:47:23 GMT  
		Size: 3.2 MB (3244396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc16a2a591d83db2a7b6cdd4bc60ba2040f6e08af56d4f7d5fc9a19596620c4`  
		Last Modified: Wed, 08 Oct 2025 21:47:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1772d91c410a4cb9c7da6a0769ca9ad85328a555a07962517a4104c0c6db024a`  
		Last Modified: Wed, 08 Oct 2025 21:47:22 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864c5041486e797edb0920a3301fb8283d8855120db150dd85130bce0745e2b3`  
		Last Modified: Wed, 08 Oct 2025 21:51:06 GMT  
		Size: 13.7 MB (13667309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bde1bfa87a5a7e6a8f38a5c5ac57dd5b4e27cedd87d4b1dc5953bdcab360ea`  
		Last Modified: Wed, 08 Oct 2025 21:51:03 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39b3c725e407cdcff27ec45897eae42e9217f2d15ce0995023f4a5cb0f9715a`  
		Last Modified: Wed, 08 Oct 2025 21:51:03 GMT  
		Size: 17.0 MB (17046899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59afed8748dfe2019637acb00616632a2a1274e4cd59b01a76d062f3c7803f60`  
		Last Modified: Wed, 08 Oct 2025 21:51:03 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620d884d5f012c160d6a2ec1ea76e51f0414ac47e5765ba861f1a33a52a3113b`  
		Last Modified: Wed, 08 Oct 2025 21:51:03 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5acded551c0d436df4dbb14a8914a41ef5c1a7ff53356c21620a27c5e2bdf3b`  
		Last Modified: Wed, 08 Oct 2025 21:51:02 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:55b233546000c51e066797ecb17f5054e2d9dcb9e70d4494ba92883814067e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.5 KB (323497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5614cd24154aabb130e0273f120cdf2f27d91540d3496aa72a5dc0ab5d2791c`

```dockerfile
```

-	Layers:
	-	`sha256:134ac9d87ffb1dfd5c14693e3761272f062a47e59d398343f4ac431b7eaec34a`  
		Last Modified: Wed, 08 Oct 2025 22:54:40 GMT  
		Size: 280.1 KB (280130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e6b69888da0a4f4aeecfed7d09a9b57d851eb47abf2c5c51a4146315b7ecc30`  
		Last Modified: Wed, 08 Oct 2025 22:54:41 GMT  
		Size: 43.4 KB (43367 bytes)  
		MIME: application/vnd.in-toto+json

### `php:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull php@sha256:c57a48ce937cb6a68a9f8ce3a342931e3a3d311bda33bcdab6da6ead0addb513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40817235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f11f875e796dad0274b282a97601ce96116bac9d274bb25ca6f2d87348965e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 25 Sep 2025 18:46:43 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26784e313670b56e69795268d2e407d73bc78055f90f0dbf24a1aa1283af0908`  
		Last Modified: Wed, 08 Oct 2025 21:17:07 GMT  
		Size: 3.5 MB (3466803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169a48ab992296218bbeee86df1f62f55d9d0853824d3c4ec52d75245cce70dc`  
		Last Modified: Wed, 08 Oct 2025 21:17:04 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51874f995123a12daa87151694471cd9e57e7276a004856c4a9780fa48deaeb2`  
		Last Modified: Wed, 08 Oct 2025 21:17:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafaf123d0c69fb7a6d9e82a01036d05f990ae61bf951ac5bb397d310343d7e2`  
		Last Modified: Wed, 08 Oct 2025 21:33:13 GMT  
		Size: 13.7 MB (13667308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed8838ced9ac2822d8eea8a2629ab4f0f6a71c00b95732014b28889400a6c1e`  
		Last Modified: Wed, 08 Oct 2025 21:33:08 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449c6f2405e22f2d27b93e324235cb4c261a94c219924cba229f56973c3c1290`  
		Last Modified: Wed, 08 Oct 2025 21:33:21 GMT  
		Size: 19.5 MB (19501246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b51c2000d76268236b24481c3b81dd2b1c7b75f2a99b7651ab6e84a06f489c1`  
		Last Modified: Wed, 08 Oct 2025 21:33:08 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c89e9489e9fea72733215f44c195f570122703beda69755396d066678d7f9b`  
		Last Modified: Wed, 08 Oct 2025 21:33:08 GMT  
		Size: 19.9 KB (19860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8690164bd55e213499bba4862969eb46ccbfa1d82ae6faa253921952b7ae6b02`  
		Last Modified: Wed, 08 Oct 2025 21:33:08 GMT  
		Size: 19.9 KB (19854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:8a28acef15987694dfae77dcc1fec82630b271050191f6709f968d3cca750ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.6 KB (323649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5267f317097feb9bdeb215446d5358983a02c67490bbba3b6bb206fc2c36e2c`

```dockerfile
```

-	Layers:
	-	`sha256:defc70814e6a18e48647586d00cba469277456c2513f96ab1ff9df5eea334dd6`  
		Last Modified: Wed, 08 Oct 2025 22:54:45 GMT  
		Size: 280.2 KB (280198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bfb74b69f85819c9084bfd077b89b69edb1e536afb8c9e2bc3e8c924b3c769d`  
		Last Modified: Wed, 08 Oct 2025 22:54:45 GMT  
		Size: 43.5 KB (43451 bytes)  
		MIME: application/vnd.in-toto+json

### `php:alpine3.22` - linux; 386

```console
$ docker pull php@sha256:4650b43f98976e96cb91b6c66f5ee02d7da8d9f2247b936b0473bd0f9b648fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41339383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc7f804182c7c1551141b31a50b468477ddf1cbfb7f43290ab7c5b5a90fe0cf`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
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
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd1047cb7f567073e37680da0f0c36a8876c5b443c64da4595cdec94c95024d`  
		Last Modified: Fri, 24 Oct 2025 18:41:55 GMT  
		Size: 3.5 MB (3522934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5432291532ac93ec85b0f03092c7de1698ed58f22f782a88d04612ec689a74`  
		Last Modified: Fri, 24 Oct 2025 18:41:55 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf46d8c3be72e693a97a1954ee7b7b2eb20280f895d12d327877769ad0e67ff`  
		Last Modified: Fri, 24 Oct 2025 18:41:55 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b239e840753cbefa4bb180374d7c4de7017b502a460c7c620aa2de485dea4a`  
		Last Modified: Fri, 24 Oct 2025 18:41:57 GMT  
		Size: 13.7 MB (13665807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ab54154fb78163d7eead7c5a48c6368ac258df68dbd81a9180669ba7b65578`  
		Last Modified: Fri, 24 Oct 2025 18:41:55 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2180045f81b8fe7a4380661a927a38a4193ab8d6c9b475c85cc78fb37e4c37`  
		Last Modified: Fri, 24 Oct 2025 18:41:57 GMT  
		Size: 20.5 MB (20487530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e06449af4deae637dc8823eb2707a0a77708c33956bad55ca2ef902a5079f9`  
		Last Modified: Fri, 24 Oct 2025 18:41:55 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b940b91cf49295a1961490a462be09ea0d948cec5dffe19693d07fd6482738d2`  
		Last Modified: Fri, 24 Oct 2025 18:41:55 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8433c5c2f5580dd81b3dcce9aa438908101b76876633367f4c63eecbc4f218`  
		Last Modified: Fri, 24 Oct 2025 18:41:55 GMT  
		Size: 20.0 KB (20041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:1ecb9f2b137d0402965cd6b3b6a7b01bcae389d579a9f09737836b62367eb96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.9 KB (325913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f89ffcd00456f941ebc575f531f9dd0f4e6fbf0c25d68a6e66f3f42dfb99d16e`

```dockerfile
```

-	Layers:
	-	`sha256:e8faae2204415901b381368c476006d2faea47d29365aade16b7c827704ae919`  
		Last Modified: Fri, 24 Oct 2025 19:54:41 GMT  
		Size: 282.9 KB (282903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cccc234782bdf5a90ec9b17cb64412969720b2f50face5591d77cfe1a12d2143`  
		Last Modified: Fri, 24 Oct 2025 19:54:41 GMT  
		Size: 43.0 KB (43010 bytes)  
		MIME: application/vnd.in-toto+json

### `php:alpine3.22` - linux; ppc64le

```console
$ docker pull php@sha256:4c8f6d5d09d660fc5c3d582e186b6462a49cc19624e18d122b587c3b352cc285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41916752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e562b9aa2efdf26a30a34260d1c70d97ae906f1ea075040ab9955c9f3001bfb7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 25 Sep 2025 18:46:43 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
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
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95a0b03903475651b081c7c705a4ab0f68ab5f5bba328735e8dae6e168526c7`  
		Last Modified: Thu, 09 Oct 2025 00:56:03 GMT  
		Size: 3.6 MB (3614664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436cae3ea479232d2bcf67ca55e6705ab3775fa412e53331855937a2a7340b65`  
		Last Modified: Thu, 09 Oct 2025 00:56:03 GMT  
		Size: 937.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1164e359044b0e56f99538c30031735fcef9128820673f06e10663118d04d0e3`  
		Last Modified: Thu, 09 Oct 2025 00:56:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c541cc61ee10a80b399d52e1f4bb8a5279855a7fa2c9a76b046ab010b008a3`  
		Last Modified: Thu, 09 Oct 2025 01:16:11 GMT  
		Size: 13.7 MB (13667307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccbe14cfb5f112f9165213e6c598f4ea32a7c520ab6aa2a8b2e62b24a58478a`  
		Last Modified: Thu, 09 Oct 2025 01:16:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03340f1e3e44fd83f3b7db1acc126ffeb5a590f53bdab6ca579db0ae5fa52f6c`  
		Last Modified: Thu, 09 Oct 2025 01:16:11 GMT  
		Size: 20.9 MB (20858704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de31c9e8e61a6c9596dd41c2b70045f4d409bb66963fba6e71103aa5056ea81`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71522eac8e5e3d7e2dbd1df9937339ed30d1ec9b9680938e271a69acdb62839b`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 19.9 KB (19873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b073119ff38c21d5615a254aaa7d93099fc3d9ffa24ba1014d9a4e26028463`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:d5ccf29ebb2f8847057f68bf1a5c8b2efe96b4da26a1054c45aba3a75beedfcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.4 KB (321395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6017caf2549496571337065b9047baca3082d56b07f5241cba8efade1bed32fa`

```dockerfile
```

-	Layers:
	-	`sha256:f3dd8404ee2f1eb6dd0d4e46591142fdf5273be5136c2e02a0a30edb088db0ff`  
		Last Modified: Thu, 09 Oct 2025 04:54:31 GMT  
		Size: 278.2 KB (278153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b294fac5f2af35e5cd71c60ab42b866c7077375f5c04c9adb3d60ad923f0395`  
		Last Modified: Thu, 09 Oct 2025 04:54:32 GMT  
		Size: 43.2 KB (43242 bytes)  
		MIME: application/vnd.in-toto+json

### `php:alpine3.22` - linux; riscv64

```console
$ docker pull php@sha256:856fcdfe7c69ba42972e47a2d3ca682ba23705f3fbaf60964b193e884acf22a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40200422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5421a0db7c7b51a651f6bd82892b8f7ad7abe3e020205615423b3d3d19d933ac`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 25 Sep 2025 18:46:43 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58e9f10e445dbf7ba866462dd44d0f912a09342dc97a4685769a2d057bcc7a9`  
		Last Modified: Thu, 09 Oct 2025 06:22:36 GMT  
		Size: 3.6 MB (3600269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2579c35b4a5055268b9ccb82f8c3307c0a781af77168952679399ed4bde3b60a`  
		Last Modified: Thu, 09 Oct 2025 06:22:36 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b6a920874b5f6759a41702af348a1eefb32a0674eeae4cd9d750418594caed`  
		Last Modified: Thu, 09 Oct 2025 06:22:36 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffe3756686e8121120603c46e2bcc7c25a6a0c923bdc47741ddd8ac23f7505c`  
		Last Modified: Thu, 09 Oct 2025 12:23:13 GMT  
		Size: 13.7 MB (13667307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c66a307993ff99b5b3658ed178834c47681fdc3296384c58149d6a03f07ef86`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f92261afff37de278981985cbf1b23f5b946658937d6f613c95988742502fc1`  
		Last Modified: Thu, 09 Oct 2025 12:23:11 GMT  
		Size: 19.4 MB (19373788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f739a05185d11834b1e53840782634f634ce0d1eca4746926c47033d6cf1ded8`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be024fc29f2390a64fe4d73fb0873a93a6ccb37995d0b252dd9bb174cd1e4895`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8011cdcf4f7bc91f25ad15e332853b7a1c42a076454400c738594f3962209b8`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 19.9 KB (19858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:c445d6e437c7ddc274d4374b8c8c94d9863b9fed5eee75148b2a1231f5f9aa8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.4 KB (321391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387092bc7acd4490e6a7cdf07e15f145dd3b320102586101540702b1a6d52264`

```dockerfile
```

-	Layers:
	-	`sha256:02c7f7bde24fccaf9bf653af7824564f38a0c026a31370cceb67ea9e56d36494`  
		Last Modified: Thu, 09 Oct 2025 13:54:36 GMT  
		Size: 278.1 KB (278149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f0f0030c5bf0534aa33d13c6061ff29653dd8b99213412c15c3619aee93df2`  
		Last Modified: Thu, 09 Oct 2025 13:54:37 GMT  
		Size: 43.2 KB (43242 bytes)  
		MIME: application/vnd.in-toto+json

### `php:alpine3.22` - linux; s390x

```console
$ docker pull php@sha256:f4e63fe40ab5b0a85d0be169f4eb7cdb1c70693da15fef1b85d285decbfb3c0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (41022615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:362487ddfc5a7c0b82c2d1337ba336fdf73580caa1729710c8874be81fed2670`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 25 Sep 2025 18:46:43 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
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
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d2dd4bd3263db65246a0eede02512575e505bf72959ea5d8d1c7f5b3dea5e`  
		Last Modified: Thu, 09 Oct 2025 00:54:03 GMT  
		Size: 3.7 MB (3692716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e39eb5e282665e4bd0e90c53a85f696e72ef63e8ef403c40cc9e67742ffe824`  
		Last Modified: Thu, 09 Oct 2025 00:54:03 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0608d8b4902677a8ba1ccd4d718738714fa13e782091c89842c948b06a52f8`  
		Last Modified: Thu, 09 Oct 2025 00:54:03 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b695282d592a178e4c36aa152fd59e9134e630400a7f212f7414d972457a8035`  
		Last Modified: Thu, 09 Oct 2025 01:06:21 GMT  
		Size: 13.7 MB (13667331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5874309b732361867c2db5075f339f7d251d35a1999132dcbd51c4fe56c9f89b`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3e822974d38b51bcdf4e8d50473316964925d3354c2f94b653b31f9886cf6a`  
		Last Modified: Thu, 09 Oct 2025 01:06:20 GMT  
		Size: 20.0 MB (19969497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a883aae99b872ee9827b2eaacabac2e42e262e2db3ecbfa459de9906907f78`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4dd335651ea2da6132f7a2def407e03ec362587a03fe3560afdcc27f769573`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 19.9 KB (19874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171f5a27fa65467dec23807b65f8edbd31acd8a6a19f0fcfbeafd66e63326096`  
		Last Modified: Thu, 09 Oct 2025 01:06:19 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:8bc6c81301dcaa3106157050a52e551f0793b3b61a6500fd72a10ffbd99f10f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.2 KB (321161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257ff41e7130669f0eb7754f4fe0f9f84db9560bdd209d0ad964e1d3ad82bc4c`

```dockerfile
```

-	Layers:
	-	`sha256:849c448164c5cfb49b313246d8c7759fc33c40e4070f8779ed56e0ca237d7bbc`  
		Last Modified: Thu, 09 Oct 2025 01:54:39 GMT  
		Size: 278.0 KB (278047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ede152e1b7438afbc032e320339d629cc69e04bb2ee1066d55e082960f97b98`  
		Last Modified: Thu, 09 Oct 2025 01:54:40 GMT  
		Size: 43.1 KB (43114 bytes)  
		MIME: application/vnd.in-toto+json
