## `php:8-cli-alpine`

```console
$ docker pull php@sha256:8d513643d465da2801a395dae4a203c04ed05c01ba8336adacd807ba4ad40644
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

### `php:8-cli-alpine` - linux; amd64

```console
$ docker pull php@sha256:6d15520dc9f2178430ff79f52b914de9dd7a31bf87de2fe464fc4953a4568211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41463229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096716fb313a2505d122ada2f78726acbebcbf74825256b51223d933bd8c6926`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 19 Dec 2024 20:11:07 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 20:11:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 20:11:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_VERSION=8.4.2
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df9007d6a249a1f8d9e6c7300691ee49e1128179bbbdbc2f6a96ae71030f723`  
		Last Modified: Wed, 08 Jan 2025 18:05:21 GMT  
		Size: 3.3 MB (3333620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0cdff53646d0d46dd03c5ff1118c3bf5b1938610564d1e7b52e30d875f5e38`  
		Last Modified: Wed, 08 Jan 2025 18:05:20 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b69154dc5c43ea0e9f1605edcea7534d1ee9f95e41a1c99116fed0a0e14aaa`  
		Last Modified: Wed, 08 Jan 2025 18:05:20 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f798125fe343aa0431e005b8b1a397169fb718d33cd5e698b18e131f67f2c2`  
		Last Modified: Wed, 08 Jan 2025 18:05:22 GMT  
		Size: 13.6 MB (13580427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41f4d91af7b8b7ae2c5493ca60e78fdc9610e58a80e0dffb5bedfd1904e8c49`  
		Last Modified: Wed, 08 Jan 2025 18:05:21 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7432544a077dfea3275a8ac795a2209f350974ffac7c632739db8d2b65024a`  
		Last Modified: Wed, 08 Jan 2025 18:05:22 GMT  
		Size: 20.9 MB (20883346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a46140907ea62255a3d87a561360306baf97e4760d41959b6c8f850fca6ae0d`  
		Last Modified: Wed, 08 Jan 2025 18:05:22 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2ac29afbf19ab96f8ab2014492ad421acfdb892865288ceeb2d8011a57fb66`  
		Last Modified: Wed, 08 Jan 2025 18:05:22 GMT  
		Size: 20.0 KB (20030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-alpine` - unknown; unknown

```console
$ docker pull php@sha256:62c701558eef6385495b47f7e7ed878c009bc3e51543fc4b08294919722e112f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 KB (310676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180ed6bc366866f1eaf6052d85411cc4a7d897da22340208572a89e6d73ea72a`

```dockerfile
```

-	Layers:
	-	`sha256:36e7c5e7c15ead7e8a4d942139ba4f2168b2dfa89ca3d50ed72a2605b0856ef4`  
		Last Modified: Wed, 08 Jan 2025 18:05:21 GMT  
		Size: 270.4 KB (270353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2184b35ec99931384b690a38a94c92f75342543fea8f8508b90bef429d7058ed`  
		Last Modified: Wed, 08 Jan 2025 18:05:20 GMT  
		Size: 40.3 KB (40323 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-alpine` - linux; arm variant v6

```console
$ docker pull php@sha256:330a1b8003cd9d3ef16213b76482ce50ecf2cc6b5baf9aa49d0b4ac9e72b8d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39277128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed01f7bb5f94f7a00eddf8e7cfac9b2a6a67b6ff9eab8872cd2864115fa0509`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 19 Dec 2024 20:11:07 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 20:11:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 20:11:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_VERSION=8.4.2
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bef010c611114840926e80cb28932ac752a42db1830688c08b53e3b0479b57`  
		Last Modified: Tue, 07 Jan 2025 04:04:46 GMT  
		Size: 3.3 MB (3288904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6270f8fc8d436fea30c28e682f01c03d0fc9e3ad4d478dd522e49204e509af1`  
		Last Modified: Tue, 07 Jan 2025 04:04:45 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100d76c367f31c843767d908ec20d1f4689fd733c923fd9605738b522084ac5a`  
		Last Modified: Tue, 07 Jan 2025 04:04:45 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9cad72888d493461905bb35f7bcd71f1d25ebbe70a3393d0bb41f85530a877`  
		Last Modified: Tue, 07 Jan 2025 04:29:46 GMT  
		Size: 13.6 MB (13580273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8849cb375579fb474d82fcfccb4d4026673e3ef62e8af96b9e95161dbe194062`  
		Last Modified: Tue, 07 Jan 2025 04:29:45 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda8bc0d594b963b5ce6c152e340a574ef001847b995028acfcabdd276d860c4`  
		Last Modified: Tue, 07 Jan 2025 04:29:46 GMT  
		Size: 19.0 MB (19023259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e03bf22ff89a4c807e160d4707cb4c6fcf6dd93afadf3a26e42e6d47109f692`  
		Last Modified: Tue, 07 Jan 2025 04:29:45 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e845766e5d3215429f966fb3b7ce57639ba9ee6dce461165a277a8fe787ba06`  
		Last Modified: Tue, 07 Jan 2025 04:29:46 GMT  
		Size: 19.6 KB (19556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-alpine` - unknown; unknown

```console
$ docker pull php@sha256:3e2f82d8c935649c60c125b1eea484371de2567c4e0afa66dbc759085aa2c8a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 KB (40345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1b5b175bc64e6fec7d736eb9ebbbbbe12843e8fbf7cf2de24b8e3327489908`

```dockerfile
```

-	Layers:
	-	`sha256:69a3a8f363a472c3bba3ecdb2bc422c6b2c17de5246e173f9231151eb5c234ef`  
		Last Modified: Tue, 07 Jan 2025 04:29:45 GMT  
		Size: 40.3 KB (40345 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-alpine` - linux; arm variant v7

```console
$ docker pull php@sha256:bb13f56475af8ebc109250b1db58221ce232858c281d595af010482633f70d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37802360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dafab128d99dbe159e63e8ffad902de134fb813348ef42ec2c51c35316a094bb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 19 Dec 2024 20:11:07 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 20:11:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 20:11:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_VERSION=8.4.2
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Last Modified: Tue, 07 Jan 2025 02:55:27 GMT  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a46a05ef2f8f5dc8f91bb48ccb26f8769e182e5d38d1a1d557e82d060b4ec5`  
		Last Modified: Tue, 07 Jan 2025 03:49:17 GMT  
		Size: 3.1 MB (3097878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0ae4122e18dac51504a788ad60f49ca9ac0b06ecc7c0df42385e05efeb7e30`  
		Last Modified: Tue, 07 Jan 2025 03:49:17 GMT  
		Size: 940.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90539fb79bdae2b2ecda3212490766029854e00ebfa8dd5d8618634d5b8b789b`  
		Last Modified: Tue, 07 Jan 2025 03:49:16 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fa228f57449de6b88589b4c2706859fa129d7e5c39f9c7f5b984e02449b994`  
		Last Modified: Tue, 07 Jan 2025 04:15:20 GMT  
		Size: 13.6 MB (13580270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c94923f50c80609f0e270f7114f1117bbfa65ff38e55bacfb2f449b4471a43`  
		Last Modified: Tue, 07 Jan 2025 04:15:20 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02141d508e59de2ce4670bdd0708c65da88d220649ca809923f9abf12d0c97e9`  
		Last Modified: Tue, 07 Jan 2025 04:15:21 GMT  
		Size: 18.0 MB (18007306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d581f46b15dafa202888d672a3bca587e73807697e6067c69cdc9e56d3aa7d`  
		Last Modified: Tue, 07 Jan 2025 04:15:20 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e712c4594e8d2f4bec83693564893857a12a9d06e24665596ad929c393df894`  
		Last Modified: Tue, 07 Jan 2025 04:15:20 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-alpine` - unknown; unknown

```console
$ docker pull php@sha256:11d2e879c8b79284e049b4e4ffe91521b3da171fdf01cf5564b82c1d825d35f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 KB (302354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e0e6355a392ed98232ba6922d199181aef1c688d4dc4dc4bf83969671d298c`

```dockerfile
```

-	Layers:
	-	`sha256:963ef47a723be967f8e5cc8b84875609c72ab5de5dbddcfc52f4ab8a7cfdd7a1`  
		Last Modified: Tue, 07 Jan 2025 04:15:19 GMT  
		Size: 261.8 KB (261794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7009a5b0a28279cc6079a5baa277a7163d3729143035f10949202d3790ba19db`  
		Last Modified: Tue, 07 Jan 2025 04:15:19 GMT  
		Size: 40.6 KB (40560 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-alpine` - linux; arm64 variant v8

```console
$ docker pull php@sha256:1d0270d66cf99ed31819458235d754c0644771597ebc65b8bf3ee36650d819dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41335754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e880aabeed90bfecf9239a79d8179fea7f4b5eccd66df662b92857945b56cd2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 19 Dec 2024 20:11:07 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 20:11:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 20:11:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_VERSION=8.4.2
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d40162970ab5d274af508499ec972de793b17d5f14ffee01a11a8e5a5256724`  
		Last Modified: Tue, 07 Jan 2025 04:25:07 GMT  
		Size: 3.3 MB (3315021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee8949964140eb86d4055cf8d682a19190f4519a76a0135d9c0635b8e590a12`  
		Last Modified: Tue, 07 Jan 2025 04:25:07 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5dc0ab84d61c5b652f4966a78d4064b20a3ee74b683b2fff8a31bfa6695fd46`  
		Last Modified: Tue, 07 Jan 2025 04:25:07 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24cf57366dc62dc8b2953fc830b0a50b8e6988edf5bbd787b8e5fe45ba9631b`  
		Last Modified: Tue, 07 Jan 2025 04:48:21 GMT  
		Size: 13.6 MB (13580276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759709f7d19efeaccc06bf3d7e83484d695e4861a56c675795ead02b448b534d`  
		Last Modified: Tue, 07 Jan 2025 04:48:20 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2655a8396fd7583723e76c552839baa55e57ec2891818e53db3b2b19bdfa50`  
		Last Modified: Tue, 07 Jan 2025 04:48:21 GMT  
		Size: 20.4 MB (20433798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ca7a96ea8bcfefa0a03b11382e0940be5d188d5c425de4f3e776cf036808cd`  
		Last Modified: Tue, 07 Jan 2025 04:48:20 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993185eeadb1a369373e2ed390a3d9c15f29108d3e3e3c3ffaba1675fe9f37e6`  
		Last Modified: Tue, 07 Jan 2025 04:48:21 GMT  
		Size: 19.6 KB (19556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-alpine` - unknown; unknown

```console
$ docker pull php@sha256:394c1ca7dc9680756aa4a0f480d80168264b8018bc7980dc2cfbabce2ad9f8fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 KB (302508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f25eb006e70e0dbd9e2ba28e7365b35e3bb7fd1cccd1b7b5410d6e0acfa1d3`

```dockerfile
```

-	Layers:
	-	`sha256:f3167c4a9a19a84a1d07bcfb6c5abfded24cc4a43a1d6cdbc3664de4fe23995f`  
		Last Modified: Tue, 07 Jan 2025 04:48:20 GMT  
		Size: 261.9 KB (261862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9abbb2109b04c379dd124c26557c358ecf00b3f468b19ee8bd65d88ae2773556`  
		Last Modified: Tue, 07 Jan 2025 04:48:20 GMT  
		Size: 40.6 KB (40646 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-alpine` - linux; 386

```console
$ docker pull php@sha256:896a736614c0b841f1caf4bcc8b05c3c8152f0a37975df5295694c9a38e7815e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41839601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53fa332a12c4678db869f69b8d0caef2cd430c9b8d740d4680bede83cfcf717`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 19 Dec 2024 20:11:07 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 20:11:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 20:11:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_VERSION=8.4.2
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d797f910131616fc1fb7e27045672feb995ed293545650f3a9808c32ed8992`  
		Last Modified: Wed, 08 Jan 2025 18:05:12 GMT  
		Size: 3.4 MB (3373789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd586c255813e5d766b1178fe388f75675f7d946a9614f5e0675b6edfe258fc3`  
		Last Modified: Wed, 08 Jan 2025 18:05:12 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a99714ec2ca232529d49f5e3e7d8b66d9ffdcfe68324b0f100903c245c03458`  
		Last Modified: Wed, 08 Jan 2025 18:05:12 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c84abf21df92bb668c7f027c69b2f4a88330d30ab21ddd3590412c02423d9d`  
		Last Modified: Wed, 08 Jan 2025 18:05:12 GMT  
		Size: 13.6 MB (13580417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f95a32c1fc73d587995143d03a6e5603b86cd7c2419add0c6e1c379c24fb6b9d`  
		Last Modified: Wed, 08 Jan 2025 18:05:12 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c197ef0272bae3b53601596eee6f0b4e0830049f4f85515503be87fa704773c`  
		Last Modified: Wed, 08 Jan 2025 18:05:13 GMT  
		Size: 21.4 MB (21398148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fd8c0572b67c8d7c1cfe944b97468ff9628fa33c225fe9a67c5c816b918f08`  
		Last Modified: Wed, 08 Jan 2025 18:05:13 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed2cc3fa0926a752f59abceea5b67c56cc4f5852c95718c22b46974c53d732e`  
		Last Modified: Wed, 08 Jan 2025 18:05:13 GMT  
		Size: 20.0 KB (20025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-alpine` - unknown; unknown

```console
$ docker pull php@sha256:1a88e7857de2f66bfe8e60d5eb488313e458cdf1a547aa33a15e9de626da4b9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 KB (310488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece294a05c994d06e60a81f63604b4acc7347d3293a9136bf3ab598b3415e0de`

```dockerfile
```

-	Layers:
	-	`sha256:bdd09a43fff2661598451b0bb7b317c8b1c28e2cb99468c940a5dd1a8e6c1aa3`  
		Last Modified: Wed, 08 Jan 2025 18:05:12 GMT  
		Size: 270.3 KB (270268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eae06e95c2bb3f363cd51ff1db0a8c7bc66464b09b66734331c94206f20d16f`  
		Last Modified: Wed, 08 Jan 2025 18:05:12 GMT  
		Size: 40.2 KB (40220 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-alpine` - linux; ppc64le

```console
$ docker pull php@sha256:6a45ea57cf27086047116602e592ce50545a54391afed483494e23c2ad1a32c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42447816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20857ecb9dadee5c6ed325fa13412794c9b5d2e229d03739386ed4d4764cd185`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 19 Dec 2024 20:11:07 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 20:11:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 20:11:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_VERSION=8.4.2
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0531d7b7562af8543d49e87e3c65356ad3882b917d7cb80906077f366e663b8`  
		Last Modified: Wed, 08 Jan 2025 18:57:53 GMT  
		Size: 13.6 MB (13580468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0227c9f9f7d554f1cca300c56b87e0f5cc124d786dafe8a7338b615a2c2e8`  
		Last Modified: Wed, 08 Jan 2025 18:57:52 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e0a2669f50a049a76351a285c8204d720afe439b7e0b795863a39d93df34aa`  
		Last Modified: Wed, 08 Jan 2025 18:57:53 GMT  
		Size: 21.8 MB (21793458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9a94c095e30794added4a9db5fc7717277f7213a5322f2fab857d9314b1677`  
		Last Modified: Wed, 08 Jan 2025 18:57:52 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76252e4d5b0498d6bec3afc8d1cb775e7d3b0dd5397dc1949ec1d7efdea66e4a`  
		Last Modified: Wed, 08 Jan 2025 18:57:53 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-alpine` - unknown; unknown

```console
$ docker pull php@sha256:5033577d4b1b3c1e389290fd2489eb4673e17dab38f82c0ffa9d1c322272d0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 KB (306144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6336d3e97b9852536c0fd9d7c02d5d40c8ea455ed3e3d33681a4929dee06cc`

```dockerfile
```

-	Layers:
	-	`sha256:feebcb5541c65761a80ddb91e1eeb7c4e91c04b11bf1b736cc2d300ec55653a9`  
		Last Modified: Wed, 08 Jan 2025 18:57:52 GMT  
		Size: 265.7 KB (265695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cab8c8999d9d804a5bb0bd0a3845e1c1d72d5cfb669a1edbbb7e4ea0e3dbc25`  
		Last Modified: Wed, 08 Jan 2025 18:57:52 GMT  
		Size: 40.4 KB (40449 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-alpine` - linux; riscv64

```console
$ docker pull php@sha256:430c9e37a214cc169ff20a7bdea63f177553d00714a81758e93ea2fe1df6baf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40709998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2120cabfe521e8bd91d086be3b90b82f85db2ada0e438ac1cb24558270a110ac`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 19 Dec 2024 20:11:07 GMT
ADD alpine-minirootfs-3.21.1-riscv64.tar.gz / # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 20:11:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 20:11:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_VERSION=8.4.2
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:7ac47ecf3caf977bc5a9f6efe0249994a504165670ebb9b6fe2c478617c5482f`  
		Last Modified: Tue, 07 Jan 2025 02:32:47 GMT  
		Size: 3.3 MB (3345140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1808309f1628e40db606650e5c5d89efd711ded9a012d0cc7cb37b2e58f215`  
		Last Modified: Tue, 07 Jan 2025 08:38:05 GMT  
		Size: 3.4 MB (3445022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6d2be5bcbaa6c2bd88c84fa524a0d4903f7d71548a130f5bfb0a4d0fa29a05`  
		Last Modified: Tue, 07 Jan 2025 08:38:03 GMT  
		Size: 940.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b5c101ed392a3daeb68dbe617637bb496ec665565d6d57d81f63915d6ab310`  
		Last Modified: Tue, 07 Jan 2025 08:38:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bb8ca8cebb1600d2403a705d8a756bc63aaa5a943e79b872774d6a2021ae69`  
		Last Modified: Tue, 07 Jan 2025 14:18:45 GMT  
		Size: 13.6 MB (13580263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0695e16f214fbf505962f4706b074f99742aad4fa96c957296c0321993739e`  
		Last Modified: Tue, 07 Jan 2025 14:18:43 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c30a089c7655d8ca6b292e37b69368f232e11a0d5abd380bf3da235e9812dee`  
		Last Modified: Tue, 07 Jan 2025 14:18:46 GMT  
		Size: 20.3 MB (20315915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a914b26e508ee8c8a80c962837501037433f9800bfb1c882b4d00805b98deff2`  
		Last Modified: Tue, 07 Jan 2025 14:18:43 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f4aee7808ae7f8b6bce693b17562e84ed059ad6dd1af649708dcddc020ae78`  
		Last Modified: Tue, 07 Jan 2025 14:18:44 GMT  
		Size: 19.6 KB (19557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-alpine` - unknown; unknown

```console
$ docker pull php@sha256:c77ccc35b422206efdd2ce8e2c268e9b633d98fe2f667ab64eae5854822bb8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 KB (300262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef4bd17e27d00f0f20e4e3fda7b7fd5b8c4501f9da265e1c2ee7ac46e26c561`

```dockerfile
```

-	Layers:
	-	`sha256:cb70177d25579e1ab52fea468185fcf68d16b4a7273ad90b373dfb760f9a6b1a`  
		Last Modified: Tue, 07 Jan 2025 14:18:43 GMT  
		Size: 259.8 KB (259813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cebcc8c480c0ebb45c9168d71fe0f0f6d6eb2e8ee42821a9336ded4aa49d8da`  
		Last Modified: Tue, 07 Jan 2025 14:18:43 GMT  
		Size: 40.4 KB (40449 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-alpine` - linux; s390x

```console
$ docker pull php@sha256:6662eead6692fb6fd2686db59c4a816d549085af55dee0ae92de0ba6cd044938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41976585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd61c8ea8bdb606d34600cbe3b3e58e5c60ef6947b7aa43b4a6f9ea2221180de`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 19 Dec 2024 20:11:07 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 20:11:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 20:11:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_VERSION=8.4.2
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81298346f7998688090749dc4a0c5695063618d53944be66940589a7c4cec0f0`  
		Last Modified: Tue, 07 Jan 2025 03:52:54 GMT  
		Size: 3.5 MB (3546676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067ae0e9cd63cfedbc820ff5cce925cad38492ddd41b8ef4a7dafcfb8c8699fc`  
		Last Modified: Tue, 07 Jan 2025 03:52:54 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19010506c88f12a8f1bd5ca006528412ce5ffcb1745e840ef9578eb779ec3a4d`  
		Last Modified: Tue, 07 Jan 2025 03:52:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9a2aa090442c32bde97cc0433427651278f3469b660d2ecc2ce3d4a0d86802`  
		Last Modified: Tue, 07 Jan 2025 04:15:56 GMT  
		Size: 13.6 MB (13580268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7b1ac65cd419ea526b44e4e04bd8ede339b5f36bb02823f61f60fd1f52efab`  
		Last Modified: Tue, 07 Jan 2025 04:15:55 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acc6d740c96374f22521a0790ee9a0528331c682fd1240f7ffc40caca929f49`  
		Last Modified: Tue, 07 Jan 2025 04:15:56 GMT  
		Size: 21.4 MB (21366542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb25f22751a4cf399a59825eaef8c37645fd93ae289b4222a335a082ec795ff8`  
		Last Modified: Tue, 07 Jan 2025 04:15:55 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4351b5fe4398b8f4529aebae29deca58e74b874c500e527f23385b4e19dc1874`  
		Last Modified: Tue, 07 Jan 2025 04:15:56 GMT  
		Size: 19.6 KB (19554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-alpine` - unknown; unknown

```console
$ docker pull php@sha256:d16a033c4d3ec36ad8833b2ca25b1c932c3203d8137964a390cff71265a821df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.0 KB (300034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b6ee8e8469193707678e60cdf68c3c957908513fd0c566b34a3e1622d0033e`

```dockerfile
```

-	Layers:
	-	`sha256:2fe35cd4348ccf7f744c2959706a3b43bf490fa72c56903dc9fbc5f45de5379e`  
		Last Modified: Tue, 07 Jan 2025 04:15:55 GMT  
		Size: 259.7 KB (259711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56a60d2aeac7c3098d7103d83d80ec2a09c679d076029de1f5e7b3ba0273e1c4`  
		Last Modified: Tue, 07 Jan 2025 04:15:55 GMT  
		Size: 40.3 KB (40323 bytes)  
		MIME: application/vnd.in-toto+json
