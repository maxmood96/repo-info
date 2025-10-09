## `php:alpine3.22`

```console
$ docker pull php@sha256:24fcf08efcc336d19553d1cde50231577af2170e00f45cd2b3eb10bda789491d
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
$ docker pull php@sha256:89afc43ca8fd39c6d972c988fdc3c3b93313867b539141ba30bd556e726a82fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41335353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5562f313d673db6105d3bb5b96ad7bcbde2f5584dcf0dc945c5a936e8db787e8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 25 Sep 2025 18:46:43 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
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
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10b1c8f28dcc9eea59bc468507a822f9cee5923019a234682b17fffc0e0399e`  
		Last Modified: Wed, 08 Oct 2025 21:29:25 GMT  
		Size: 3.5 MB (3522947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c8476eb364d29e72f440167fb044ac72dfa85ef77b1c2bc1cfa03c4d8793b9`  
		Last Modified: Wed, 08 Oct 2025 21:29:24 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7115926f8e2adaddbca9f8b1778fc2142df7ec3fdad63b6c6e1c8399109e3b71`  
		Last Modified: Wed, 08 Oct 2025 21:29:24 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0eaf5c5fa7e4fae1e5ce91a8aa7a311895c774277dae69bf3b4395bb7e4b344`  
		Last Modified: Wed, 08 Oct 2025 21:29:27 GMT  
		Size: 13.7 MB (13667288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1741bf9292a6bf0fd75328cac116ab9a15c37b4cd92a34c0964795f4c66197b5`  
		Last Modified: Wed, 08 Oct 2025 21:29:24 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e823544634a764020faf2c3de845a5526f9e25b58f14201554eeaf3904b430c5`  
		Last Modified: Wed, 08 Oct 2025 22:18:58 GMT  
		Size: 20.5 MB (20482000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a22d23a64f20ed5066e1e907d56e071ee2749128c4ab89e8b1a55c4ee87a9d8`  
		Last Modified: Wed, 08 Oct 2025 22:18:55 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08c4f12bf256ee1557a66c448651365a2ee0bc85462fe9c0af12695f340f45b`  
		Last Modified: Wed, 08 Oct 2025 22:18:55 GMT  
		Size: 20.1 KB (20051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8bd18e3369a3b74096dc033c7debca5b89dc5e89fa8b08524a2b70e5c9bb0c`  
		Last Modified: Wed, 08 Oct 2025 22:18:55 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:56bfc3046f0700aedebad484f487d4655c058016f0a9919d691a876721bcb65d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.9 KB (325913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009f5dc104c4ad46099266995e7db77bed30931f245b47b4d9b629b90a63be5b`

```dockerfile
```

-	Layers:
	-	`sha256:b212ad8467f904fa316e15a832f2b9e1b8b4ef975bcd0464802b2742f2c0a220`  
		Last Modified: Wed, 08 Oct 2025 22:54:49 GMT  
		Size: 282.9 KB (282903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:456bafe74ddfa31ec3e79d863a3bc60b0563f36b3e49c0d06a140858dae61f25`  
		Last Modified: Wed, 08 Oct 2025 22:54:49 GMT  
		Size: 43.0 KB (43010 bytes)  
		MIME: application/vnd.in-toto+json

### `php:alpine3.22` - linux; ppc64le

```console
$ docker pull php@sha256:e34b1c5ce1f667a184476ce2f9c1156a9cce44e893ffef3529a3cdc1cf77cff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44708067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc60d4d05c4eea9cf5f94668b4f42e06c60cbe64fd2280394608608c8c30b9f8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c06a09b74ec526da3ee14df3d2b5a91f72a4fa277f482bbf918bb4cccb1652b`  
		Last Modified: Tue, 05 Aug 2025 00:06:20 GMT  
		Size: 3.6 MB (3611165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed9e57a166c2abcf7305f3cb2afd6de830c6af45dd6c91b2a8218f7a4912f6c`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e0e72d666cf9be46385f732d53bc45342fa962757abf4c31f4b45015775159`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d165415cc65159456128153815546067ca89254c2ee16739d9a593915c2bbe`  
		Last Modified: Thu, 25 Sep 2025 21:50:59 GMT  
		Size: 13.7 MB (13667229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf9d58c2d24e175afe73c83186c70a54653d4a7a9e169b42a187588df2f087e`  
		Last Modified: Thu, 25 Sep 2025 21:50:55 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c6b86280f0d78ca867fdc85683b4bd147d316f6690434860270cded233fe23`  
		Last Modified: Thu, 25 Sep 2025 21:51:00 GMT  
		Size: 23.7 MB (23658979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a03266532d2f40547f2998637ec30ab8daead8d5647cda1092bf759010e726`  
		Last Modified: Thu, 25 Sep 2025 21:50:55 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68735b727384e36cb229e8a569527bed6d29607ef0fcc184b9ec6245142bbaaa`  
		Last Modified: Thu, 25 Sep 2025 21:50:53 GMT  
		Size: 19.7 KB (19739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a327693df1b9b6206d9f570299a84275c02003ba38d4a91e11c142da596913b`  
		Last Modified: Thu, 25 Sep 2025 21:50:53 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:3f4c41832dc25e6f663c2fc3e5b1f5468b1d0da8892621d584319ae9785f55af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 KB (318782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc6a48610556ebb7b9fdd33742e5a5a4cee0ab68fd035100fbd0d8a20485907`

```dockerfile
```

-	Layers:
	-	`sha256:99f715a292b28dbeda803abe8b7a76097ebd30549d7c628f5fb09cfb08418c08`  
		Last Modified: Thu, 25 Sep 2025 22:55:30 GMT  
		Size: 275.5 KB (275540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5f5f470a7ba586571bd330f82633f66855170300865f50f4ef174de4964dc95`  
		Last Modified: Thu, 25 Sep 2025 22:55:31 GMT  
		Size: 43.2 KB (43242 bytes)  
		MIME: application/vnd.in-toto+json

### `php:alpine3.22` - linux; riscv64

```console
$ docker pull php@sha256:9c8a0e4edbd928bd6b1d240773c4c379a7a84ca92fb6ae2114e55f08603d39a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42799255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f214c46f1574ee793626ffb79777cf34e15dcf853943d1bb1ddbddb83abba3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c293b040c7a67eeac13c53a522990f19f36e1b39939bdc55cbe7dbeefa2c82`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 3.6 MB (3594168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4153c5fef55d21621d3f69b9fd9a25c43bda1995413d8f4dcacf545b0d8d2a0b`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc109449c55003e3c992ac8133ad0a1b0794f6911cb2e1cc81ff0acc6e85daa1`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce54772840e390ce79b2bd312dffccae5a0404b88de7d2cec073f06bfc4a7447`  
		Last Modified: Fri, 26 Sep 2025 06:57:14 GMT  
		Size: 13.7 MB (13667214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f6b22cf755134f26369ac0039e67fee0e571a02ceb8a94e09289af33125353`  
		Last Modified: Fri, 26 Sep 2025 06:57:12 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac0365b3ab37d3f9b715bd780ad485c95ad15ed5c5b1c3bfd8970387dd36daf`  
		Last Modified: Fri, 26 Sep 2025 06:57:18 GMT  
		Size: 22.0 MB (21981498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b317aeae2dc6ed4a866738e3dcf9f1437efcbb8375680cb0494c81ae062b0a`  
		Last Modified: Fri, 26 Sep 2025 06:57:15 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbf49bc5c019b48fa352706ee9f2a45f3f399db6053ebef12e34dc331889673`  
		Last Modified: Fri, 26 Sep 2025 06:57:15 GMT  
		Size: 19.7 KB (19742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f239dc1f19e52fdc0efc9ea8ed3770da45c53b5f01033f7ed075a4ca9389f8`  
		Last Modified: Fri, 26 Sep 2025 06:57:09 GMT  
		Size: 19.7 KB (19735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:ef91e81d4bafa4f7844c412ad9cd10f81f6e606c9ca38e3d4d21fffcc411650f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 KB (318777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d1560cb2ac00eba8e7f2d2902a985bfb34011a3d8a6f5aea2524ca4e4fcf27`

```dockerfile
```

-	Layers:
	-	`sha256:93668a2ff96422e15bfa43af9545042706b143f2198b5cff2fdea069ee04ed49`  
		Last Modified: Fri, 26 Sep 2025 07:54:33 GMT  
		Size: 275.5 KB (275536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b4a43810a44a8946756870cc39aa1e15386ef839ced8aa3b871e6958c3953c1`  
		Last Modified: Fri, 26 Sep 2025 07:54:34 GMT  
		Size: 43.2 KB (43241 bytes)  
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
