## `php:zts-alpine3.22`

```console
$ docker pull php@sha256:466bbf6eeac77ebf16f89f594227147614594a54d1b717dc81cd5a27a47ed924
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

### `php:zts-alpine3.22` - linux; amd64

```console
$ docker pull php@sha256:66228d4898f13f0ba7a72dbaf05ac14dac9dab02ced157ea9f55a1f4426161e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50373676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebcda5fa76bf5e527bbec69e3cd0297d41d5b4c593fe3c684b14e91d4f9dc88`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 05 Jun 2026 01:15:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 05 Jun 2026 01:15:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 05 Jun 2026 01:15:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 05 Jun 2026 01:15:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 01:15:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 01:15:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 01:15:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 01:15:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 01:15:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 05 Jun 2026 01:15:16 GMT
ENV PHP_VERSION=8.5.7
# Fri, 05 Jun 2026 01:15:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Fri, 05 Jun 2026 01:15:16 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Fri, 05 Jun 2026 01:15:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 01:15:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:18:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 01:18:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:18:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 01:18:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 01:18:13 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdd138981f518ef6dc38d84051da0bc1cfaa13456fc69994c50e65db387cccd`  
		Last Modified: Fri, 05 Jun 2026 01:18:21 GMT  
		Size: 3.5 MB (3464905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a606b752fc791d0580b100232305b6e76f0963fbc32bc03fa19b4aee5eb7e4e8`  
		Last Modified: Fri, 05 Jun 2026 01:18:21 GMT  
		Size: 937.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433a55922d57c1b620923ebc6c66edd7252525f6c6ecd017685e7368056efc7c`  
		Last Modified: Fri, 05 Jun 2026 01:18:21 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf8170f024358ba94080cd7d7f6f870ef37043a2e9acfd0b50f766a3b5d875d`  
		Last Modified: Fri, 05 Jun 2026 01:18:21 GMT  
		Size: 14.4 MB (14419453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111da8ed8b47c1af4528803232b7ebd36e5aa5c37860bb4f1f0994696390eded`  
		Last Modified: Fri, 05 Jun 2026 01:18:22 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68eb5ecfefb2b50657f1618f85e1918ebbec13f927ed1beb9e92344de209add9`  
		Last Modified: Fri, 05 Jun 2026 01:18:23 GMT  
		Size: 28.7 MB (28657021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734ba0a0084ef5005f28af24c43dea44f7f4413df6be1a068720f8cae49287cb`  
		Last Modified: Fri, 05 Jun 2026 01:18:22 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f144686ac4e97588c084c04fc2382bd4c93a8d541758950b64681115b283b8`  
		Last Modified: Fri, 05 Jun 2026 01:18:23 GMT  
		Size: 20.0 KB (20022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:21efc9124e699cfcf32971e8ddace3e7a7ca22fe7b57ece00d4b9caca68d8016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 KB (314731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6103dac2bf53d2fc05c3806c9c607f1016ed59747bcef4040bd637d1ed6a23a3`

```dockerfile
```

-	Layers:
	-	`sha256:def1adaa884c2306531749f124ad8b0b972ddeaba22e832c5f48bb68a52a2f81`  
		Last Modified: Fri, 05 Jun 2026 01:18:21 GMT  
		Size: 277.4 KB (277398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40cf6247b62a24c76b44dc2bf9df986957dfa2dc86f257a209a6535b6423f196`  
		Last Modified: Fri, 05 Jun 2026 01:18:21 GMT  
		Size: 37.3 KB (37333 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine3.22` - linux; arm variant v6

```console
$ docker pull php@sha256:f47d8000922fa7cf5deb492abdbc8a35564cb46b5ccd064a89a5b7ee2031aa51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46249354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfe8ff1f350e3ad5968a412bd9380b06a408fa334799c0c3931e0ed8efdf8d3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 05 Jun 2026 01:18:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 05 Jun 2026 01:18:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 05 Jun 2026 01:18:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 05 Jun 2026 01:18:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 01:18:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 01:18:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 01:18:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 01:18:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 01:18:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 05 Jun 2026 01:18:18 GMT
ENV PHP_VERSION=8.5.7
# Fri, 05 Jun 2026 01:18:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Fri, 05 Jun 2026 01:18:18 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Fri, 05 Jun 2026 01:18:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 01:18:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:21:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 01:21:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:21:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 01:21:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 01:21:40 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa3b8f9c13db25a57eaeb3b4b24a97156f975812ae99f37859883f090c617a4`  
		Last Modified: Fri, 05 Jun 2026 01:21:47 GMT  
		Size: 3.4 MB (3428177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a387170b666aff2041fba023fd1e5ce0ca87310867ec5431eba595b2368e1f54`  
		Last Modified: Fri, 05 Jun 2026 01:21:46 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c377899ec2b78bac096c8fe548e8dd46cc9fb3f034b17c0df1272701dc81a2`  
		Last Modified: Fri, 05 Jun 2026 01:21:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d1640b5908b5de9f7187222d0d2739b04534eb98e859774d5d35f2055a2db1`  
		Last Modified: Fri, 05 Jun 2026 01:21:47 GMT  
		Size: 14.4 MB (14419498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb0deefb051cc218f5ff61a3406361581ebe6f5fc88c5689a83035344af15bc`  
		Last Modified: Fri, 05 Jun 2026 01:21:47 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39e8eb2cc9209d1a4d93a96f2b33f469514d80501bdb566e53df7446ce695da`  
		Last Modified: Fri, 05 Jun 2026 01:21:48 GMT  
		Size: 24.9 MB (24870378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4ff567225d8123e5fae4ba1b17580235853ee2919bc2e9ea377cb5a5acd012`  
		Last Modified: Fri, 05 Jun 2026 01:21:48 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9333a4def2558816a5812c32714c708da860a7da8d1b6fe485c19615c471b69d`  
		Last Modified: Fri, 05 Jun 2026 01:21:48 GMT  
		Size: 19.8 KB (19835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:1cfdd3f573d60efd09cd7a7d5bbc4a503bbffff8174e23339ac2c0f709745086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 KB (37263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5311d574e44e7ba87f09500ba21b5349afa2d6f21ec7584fdc03ca22bdf37e06`

```dockerfile
```

-	Layers:
	-	`sha256:f323d69e4abd761a5a9775d85a57afb4a65b34a971a090f46e46f395c727c47a`  
		Last Modified: Fri, 05 Jun 2026 01:21:46 GMT  
		Size: 37.3 KB (37263 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine3.22` - linux; arm variant v7

```console
$ docker pull php@sha256:5b62580e7c2c207572fb952d24705913174f65339d2df78a4c35f66e4dcf1b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 MB (44371403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932fcd3afbf94e962c65bb7c5448c4590215747e75b4dbb94b9b48821518f704`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 05 Jun 2026 01:19:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 05 Jun 2026 01:19:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 05 Jun 2026 01:19:19 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 05 Jun 2026 01:19:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 01:19:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 01:19:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 01:19:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 01:19:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 01:19:19 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 05 Jun 2026 01:19:19 GMT
ENV PHP_VERSION=8.5.7
# Fri, 05 Jun 2026 01:19:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Fri, 05 Jun 2026 01:19:19 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Fri, 05 Jun 2026 01:19:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 01:19:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:22:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 01:22:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:22:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 01:22:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 01:22:46 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d35b52b32a93c9df6dcfc284804773f027fbe75e814e9bb01f95cdeb199e47`  
		Last Modified: Fri, 05 Jun 2026 01:22:54 GMT  
		Size: 3.2 MB (3244376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cebbd2905ed52cc3b0059007f1b1930f7793d97731d8ae37351aba336e25bc`  
		Last Modified: Fri, 05 Jun 2026 01:22:54 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c36926b86c30c5e191f7a0494b05cb9874e5becbcb464e2dc8c7b9519d1bd9b`  
		Last Modified: Fri, 05 Jun 2026 01:22:54 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357eb0e1f85f036e5210e7d19761631ff9b4a247a31762682d2b4acf12a14517`  
		Last Modified: Fri, 05 Jun 2026 01:22:54 GMT  
		Size: 14.4 MB (14419489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48335fa9e76451cd3b194706e96f639fc41390565af06fa410d67c7de02ffce`  
		Last Modified: Fri, 05 Jun 2026 01:22:55 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c383f6a530f64e495c2cad13410000f5cac1d7e57e7439da61b22505300a74eb`  
		Last Modified: Fri, 05 Jun 2026 01:22:56 GMT  
		Size: 23.5 MB (23457807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f5dc9b5ecbaf0f1fd0a137ca57a36fc3052d6f3f8f4c74b21fe113de244876`  
		Last Modified: Fri, 05 Jun 2026 01:22:56 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10dece7dceb5915bad9334ab6786b07a2c931fd45887455faa0ffb04e6aefbf`  
		Last Modified: Fri, 05 Jun 2026 01:22:56 GMT  
		Size: 19.8 KB (19813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:6e988fbdee137173d26e68b75652280a175cc7afe2475388ce93078148910134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 KB (311922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8325a6e46bc3ab52e5a5c1229ca7d85637be0ee0af9bcee605d88fb6ea41d1e`

```dockerfile
```

-	Layers:
	-	`sha256:71481cd5549c31ca20bfebb757eda7eac376912bbf70441c7ce3eb01f3e01f1a`  
		Last Modified: Fri, 05 Jun 2026 01:22:54 GMT  
		Size: 274.4 KB (274444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b3f9918f37ca4b6a1a2ba95462135503278bf34097733db3f8924d9cf8141c8`  
		Last Modified: Fri, 05 Jun 2026 01:22:54 GMT  
		Size: 37.5 KB (37478 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull php@sha256:514af65ddb4b850373a76d7c7368bd005bf628036d14bbfc8162fd469394b87a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49999929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee042bca33c097abe7681b2e514df8955681f5ab96ee4e8f4a935cac6c97d663`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 05 Jun 2026 01:15:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 05 Jun 2026 01:15:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 05 Jun 2026 01:15:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 05 Jun 2026 01:15:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 01:15:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 01:15:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 01:15:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 01:15:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 01:15:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 05 Jun 2026 01:15:33 GMT
ENV PHP_VERSION=8.5.7
# Fri, 05 Jun 2026 01:15:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Fri, 05 Jun 2026 01:15:33 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Fri, 05 Jun 2026 01:15:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 01:15:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:19:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 01:19:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:19:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 01:19:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 01:19:25 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f793f4e69bc30c09c403396fc97bdb12fd8889a17065166515ff0239733cea2d`  
		Last Modified: Fri, 05 Jun 2026 01:19:33 GMT  
		Size: 3.5 MB (3467693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0297320f6c131ec12e28e8ac4a45585d2fb4d488dee51398257c75de8a2b55c`  
		Last Modified: Fri, 05 Jun 2026 01:19:33 GMT  
		Size: 938.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0076b4ff4cf73ab56f6f317310266bcd5e66148b91f443dad3c3e907cf1dccc`  
		Last Modified: Fri, 05 Jun 2026 01:19:33 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5008e830179559597953f70e0447d17711fb34acfda9a6a23672aed5a0441930`  
		Last Modified: Fri, 05 Jun 2026 01:19:33 GMT  
		Size: 14.4 MB (14419479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad4062b152ddbefa2ec3e1bbcf57699ba7b5ed27e30e5a0b62bb29396a45672`  
		Last Modified: Fri, 05 Jun 2026 01:19:34 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111f4a428ac0f3dfd4a12c8e76d0c364c127cbd16105d2ce6837a3062882bd75`  
		Last Modified: Fri, 05 Jun 2026 01:19:35 GMT  
		Size: 27.9 MB (27946950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b3870757b88feb2aec422aceb182d14ab37abdb470be4d7c54c96aa2d9ee76`  
		Last Modified: Fri, 05 Jun 2026 01:19:35 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9970afea5082e2cf827feba084c61ccfc5ed6a1bfb704c8e90bb60c13e068c30`  
		Last Modified: Fri, 05 Jun 2026 01:19:35 GMT  
		Size: 19.8 KB (19823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:87604b67c0a371f1017ce1a61390e621273cdb96805dc5e7a357357272249faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.0 KB (311976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6fa47b872d27a88cb8cc865e8e0de4ece705594e0549ba8e6130e3c01cc5ce`

```dockerfile
```

-	Layers:
	-	`sha256:ddd75942c7ba09015ef1cb04d9a1131966d3dea74c448b931a6aae6e144c57df`  
		Last Modified: Fri, 05 Jun 2026 01:19:33 GMT  
		Size: 274.5 KB (274464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79ca9ed5c0708a3e03d634993124cd931fbe95f83057113757453c36b46a188`  
		Last Modified: Fri, 05 Jun 2026 01:19:33 GMT  
		Size: 37.5 KB (37512 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine3.22` - linux; 386

```console
$ docker pull php@sha256:b7b040374b0b2e089024db82ae0561d81089d6fe5231d7edf0206bcfa72ad74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50952008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e450b067697768443c2ee6eacf79f92529f92450c4e35f947e2be34b8709f3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Fri, 05 Jun 2026 01:15:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 05 Jun 2026 01:15:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 05 Jun 2026 01:15:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 05 Jun 2026 01:15:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 01:15:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 01:15:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 01:15:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 01:15:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 01:15:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 05 Jun 2026 01:15:17 GMT
ENV PHP_VERSION=8.5.7
# Fri, 05 Jun 2026 01:15:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Fri, 05 Jun 2026 01:15:17 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Fri, 05 Jun 2026 01:15:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 01:15:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:18:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 01:18:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:18:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 01:18:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 01:18:23 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9752d9856a7d7415d6cb91decea93aded4a2b3d2d3a37273996497fb404d2f`  
		Last Modified: Fri, 05 Jun 2026 01:18:30 GMT  
		Size: 3.5 MB (3522712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a606b752fc791d0580b100232305b6e76f0963fbc32bc03fa19b4aee5eb7e4e8`  
		Last Modified: Fri, 05 Jun 2026 01:18:21 GMT  
		Size: 937.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce6729cb43bc90a38d885732e1f87ef57f3c964ffa66e9fe7bef7c569e0f4f4`  
		Last Modified: Fri, 05 Jun 2026 01:18:30 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf5a99ad47f5af00bbfcd75df23cd47ffcf6fd99290c9d73bfcdb911b824f71`  
		Last Modified: Fri, 05 Jun 2026 01:18:31 GMT  
		Size: 14.4 MB (14419459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602399e4c57b21df1e0452577322270275de3de89fc805769e5d202a4a655293`  
		Last Modified: Fri, 05 Jun 2026 01:18:31 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07acbf751d86ee42e8d56fedc7d10434321f22dcab41e7e8926e0a731a44dd24`  
		Last Modified: Fri, 05 Jun 2026 01:18:32 GMT  
		Size: 29.4 MB (29361003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1949f69fdbec83100e8762e6d75fa74c1d573b29860d49f587e0182d8d4c7253`  
		Last Modified: Fri, 05 Jun 2026 01:18:32 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c84a3eda17148905bcf7ea9438caf58d088ab5d1dc3f0494ceb40c3ee4c6ad`  
		Last Modified: Fri, 05 Jun 2026 01:18:32 GMT  
		Size: 20.0 KB (20021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:e4b8fb166f6fc6cd5bd1a066a5849ad8a6ee20028957d3b00632181b62ce42f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 KB (314662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5fafb6a42c201e84abfb08157981e7d722b82314c15f0b55f3bf6e19dc2318`

```dockerfile
```

-	Layers:
	-	`sha256:b1bd73e8b08630bc3cb432bf8e9424c2c05d89f38fa4ee681115535a4d31f281`  
		Last Modified: Fri, 05 Jun 2026 01:18:30 GMT  
		Size: 277.4 KB (277373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e74faf4740ffd42cc20f20e30d757f7c0d22031f3a2f9b50d0f2051f0f0f6ffe`  
		Last Modified: Fri, 05 Jun 2026 01:18:31 GMT  
		Size: 37.3 KB (37289 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine3.22` - linux; ppc64le

```console
$ docker pull php@sha256:0623d69d3f6767b12efbb40dd9994808ec640ab17e27146da0fc81743adf56dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50742655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bb049923e74b362bc8501f172bbb5c0a92be7a39f85cd33d0c95c91127fdb6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:19:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Apr 2026 00:19:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Apr 2026 00:19:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Apr 2026 00:19:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Apr 2026 00:19:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Apr 2026 00:19:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_VERSION=8.5.7
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Fri, 05 Jun 2026 01:42:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 01:42:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:54:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 01:54:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:54:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 01:54:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 01:54:36 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b158ada90b6cc8f44737ff5d95bedaf7f63979acc7eb3452859f5d0ace79a5`  
		Last Modified: Fri, 17 Apr 2026 00:25:56 GMT  
		Size: 3.6 MB (3615071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b99d415a1788bb58d298132317074efb0a3a7801f8a3fed0809ed39f6869175`  
		Last Modified: Fri, 17 Apr 2026 00:25:55 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9eb866ab296180559ca8a3add579c6854d381da1068c287f30bf1ddcaa1eaf8`  
		Last Modified: Fri, 17 Apr 2026 00:25:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af78c2b9be930d3bfca6d9c5d98914a3ca2676bb7b3951f252adfc0b6f4f24a`  
		Last Modified: Fri, 05 Jun 2026 01:48:40 GMT  
		Size: 14.4 MB (14419518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd934ad5eaf9340d82ba9aa021468563c91541fa549c823a5babdf4cea89a19d`  
		Last Modified: Fri, 05 Jun 2026 01:48:40 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672f45dc987abac437457f7b12b784a5da04f7f2c75ee8355414ea7b416a5a5a`  
		Last Modified: Fri, 05 Jun 2026 01:54:53 GMT  
		Size: 28.9 MB (28947475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71e940b770ae8ae6053505787a0c6539a3e4b84ffe817be50ee9547a9198a1d`  
		Last Modified: Fri, 05 Jun 2026 01:54:52 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6a37d315bfb7e6db7cb0a9ac980df57c59e3e7d0e59e634ab462d5a3588fe8`  
		Last Modified: Fri, 05 Jun 2026 01:54:52 GMT  
		Size: 19.8 KB (19840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:2e73211b38bf31d6d04b631e4b3c85f55d34e6f867eca50dc9b1c4a39efd2baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.9 KB (308927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:309a81d51f8bec06d31c3a495e21f581166d5986e1dca7909dd0236374f18d26`

```dockerfile
```

-	Layers:
	-	`sha256:421e748d138255c43ef3b2ff1887bcada577051fb581efef036a88ced0edc81c`  
		Last Modified: Fri, 05 Jun 2026 01:54:52 GMT  
		Size: 272.5 KB (272491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e5e7914b23aefc9de95caaea2e3a3f6f3c5ad659bbe64711985d72ffabfbbdb`  
		Last Modified: Fri, 05 Jun 2026 01:54:52 GMT  
		Size: 36.4 KB (36436 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine3.22` - linux; riscv64

```console
$ docker pull php@sha256:df4d927271132b4d91a3597db8aa1a2b75704b23e80cb5380a01892ec0edfebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48472244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737adef2c021dc1f55aa1a63b440ffa024523a9e31a8375408774448c6cc6d42`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Sat, 18 Apr 2026 11:02:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Apr 2026 11:02:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 18 Apr 2026 11:02:26 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Apr 2026 11:02:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 18 Apr 2026 11:02:26 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_VERSION=8.5.7
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Fri, 05 Jun 2026 07:43:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 07:43:08 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 10:45:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 10:45:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 10:45:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 10:45:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 10:45:51 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aba8e387b0f52a066bd16fc16548380bb5c1ba358c87f632f41bf0e1538804c`  
		Last Modified: Sat, 18 Apr 2026 12:03:48 GMT  
		Size: 3.6 MB (3600194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e0aef12c28ba880017fb96a48e3e22f4b4e363ee1be8f9a85075a131d12b72`  
		Last Modified: Sat, 18 Apr 2026 12:03:47 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6a7d02aa931427745ea3ec5ed71cd22b97056886e6224d2e88e3226411519f`  
		Last Modified: Sat, 18 Apr 2026 12:03:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae2613ed4a3e869f6c55d87b3babbffcc862b86c10e7c4d15ec090cd5053e49`  
		Last Modified: Fri, 05 Jun 2026 08:43:32 GMT  
		Size: 14.4 MB (14419468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af80e7cb29dfe9b2e4aff888245a456ba3eafbcc0ab5c19a6c677cb0ca672fe`  
		Last Modified: Fri, 05 Jun 2026 08:43:28 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ae516f421398e0fee075596961f599b167dda849fec85cb280d1cdc218edbd`  
		Last Modified: Fri, 05 Jun 2026 10:47:10 GMT  
		Size: 26.9 MB (26907765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72feb391aadf3810ef249d5c1dc6dac840ecc877b992407aa6e983425305f876`  
		Last Modified: Fri, 05 Jun 2026 10:47:06 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a61efcb3de50e4f60eb29ade19ef2e158ddc302127d33d428a268a94ce26207`  
		Last Modified: Fri, 05 Jun 2026 10:47:06 GMT  
		Size: 19.8 KB (19833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:623c801a6657401afe164fa7f24a9285cac30c8b52dccfb7d8c0bdefa1718918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.9 KB (309874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8125d029426d55bc6031356e222fe87cefa406c3796bd2f435a65d26b6d4ce9`

```dockerfile
```

-	Layers:
	-	`sha256:e23b97178f028106ec66c7f2bfb325de2ea98ad9e67d27bdc7d2497363ad10eb`  
		Last Modified: Fri, 05 Jun 2026 10:47:06 GMT  
		Size: 272.5 KB (272487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:798f03b4474606171364e370e70c334149aee18cf5494beacc5b6be202d33da1`  
		Last Modified: Fri, 05 Jun 2026 10:47:06 GMT  
		Size: 37.4 KB (37387 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-alpine3.22` - linux; s390x

```console
$ docker pull php@sha256:1ac08aa560735e7fb9f3c718188d18d1bafbba65940a5f04de5e0f9c82c66cb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49403581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28c9764cb594e98f817a76a7ed4675c4ea982a61c77575836068d4687b29977`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 06:10:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 02 Jun 2026 06:10:41 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 02 Jun 2026 06:10:41 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 02 Jun 2026 06:10:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jun 2026 06:10:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 02 Jun 2026 06:10:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jun 2026 06:10:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jun 2026 06:10:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jun 2026 06:10:41 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 02 Jun 2026 06:10:41 GMT
ENV PHP_VERSION=8.5.7
# Tue, 02 Jun 2026 06:10:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Tue, 02 Jun 2026 06:10:41 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Fri, 05 Jun 2026 01:27:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 01:27:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:33:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 01:33:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:33:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 01:33:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 01:33:06 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c75735c7840576081d137f73c9e1d671fef683197275ebf98b3f89df2d6f047`  
		Last Modified: Tue, 02 Jun 2026 06:14:13 GMT  
		Size: 3.7 MB (3691317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6467f2db1ecdfa183e05296de22d16bef58101b59f959d209d6247d1f495d947`  
		Last Modified: Tue, 02 Jun 2026 06:14:13 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17247e4c91d7dc91ceb5e0d3f79b6712c2173b99d17a3c9edfbf048e100777ee`  
		Last Modified: Tue, 02 Jun 2026 06:14:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff11588a3caf58ad81c5155c6e1372335e0a2d6a86222b96cc84daef958ac8e3`  
		Last Modified: Fri, 05 Jun 2026 01:33:17 GMT  
		Size: 14.4 MB (14419503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1fb8967fb08536e9d1df5ada307b6557c57eec7fa27fbf14a261c6e0ac7d76`  
		Last Modified: Fri, 05 Jun 2026 01:33:17 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3bb7ec89ea8f49e7843db3d7c45b5ed32b2300b780723b47a2c0b39d53361e7`  
		Last Modified: Fri, 05 Jun 2026 01:33:19 GMT  
		Size: 27.6 MB (27614960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb32dda0299dfc331c65969587f347f8a1efb862cbe86de22d03be3d0a4f92b8`  
		Last Modified: Fri, 05 Jun 2026 01:33:18 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80a8488fd49d4d1216334a9cc77bff647d529f63d4facb8110214268264a6c6`  
		Last Modified: Fri, 05 Jun 2026 01:33:19 GMT  
		Size: 19.8 KB (19826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:8aa6015d605cec9c74cf7d1b6f33c27d62e815f48805cc7b81376ffad4ef5e14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.8 KB (309788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ee89f10fcbaf33e3e0b314bc23565ceecb9cc89c10fd572b5f5517f394ff3c`

```dockerfile
```

-	Layers:
	-	`sha256:07c7fa7c9da041d3755e15894e72941214d73af68fff2c9c4669014041a05749`  
		Last Modified: Fri, 05 Jun 2026 01:33:19 GMT  
		Size: 272.5 KB (272457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3a0afce74c17e5346409aca445a29bdb8492c92ccf2e7e4ab0b1cb7abd2367b`  
		Last Modified: Fri, 05 Jun 2026 01:33:18 GMT  
		Size: 37.3 KB (37331 bytes)  
		MIME: application/vnd.in-toto+json
