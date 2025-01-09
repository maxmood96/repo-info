<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `composer`

-	[`composer:1`](#composer1)
-	[`composer:1.10`](#composer110)
-	[`composer:1.10.27`](#composer11027)
-	[`composer:2`](#composer2)
-	[`composer:2.2`](#composer22)
-	[`composer:2.2.25`](#composer2225)
-	[`composer:2.8`](#composer28)
-	[`composer:2.8.4`](#composer284)
-	[`composer:latest`](#composerlatest)
-	[`composer:lts`](#composerlts)

## `composer:1`

```console
$ docker pull composer@sha256:955962b2bad33bc86e82dfeffcfaf558ae65f977ce52139c5bd0fd49ed045549
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

### `composer:1` - linux; amd64

```console
$ docker pull composer@sha256:6b2f16390a7eadc1e9ca1ff139c2d12f6673514054c91752e513749cc47a597f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74095403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38a56acb18557cfb93f82b3c8f039460811b182ab8aa7f8584a6deacfa3b4c2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
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
	-	`sha256:e0baa056e21bcab81c2acc5425ed67c40a2988d923a3def22fa0d8050cadda8a`  
		Last Modified: Wed, 08 Jan 2025 18:23:23 GMT  
		Size: 31.9 MB (31896629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d559b6b0eff1bbb1c50a1df8bbe104b308b9e9e9b322cbadf11f5397753c46d`  
		Last Modified: Wed, 08 Jan 2025 18:23:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2476acf1da8f88db250c313c5274e7d11c4e7621977c094f8ffd6327244702`  
		Last Modified: Wed, 08 Jan 2025 18:23:23 GMT  
		Size: 734.8 KB (734786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b18feab52adf6434ad9b56755607fb54747e39e2cf3b420628d9f7db124f084`  
		Last Modified: Wed, 08 Jan 2025 18:23:22 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7697754ff51986cb09fd9446d5106596f8e01b2ec9416923e7ee18e0e2865986`  
		Last Modified: Wed, 08 Jan 2025 18:23:23 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:703fab1901cd1587c27f5cad46f45b8253432a2a2a8e63abdd64ba50a4b4f03e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42f044d0c6fbfb26beaf4f8e255146492781eb7dcdf971a3cca32f59e1403e6`

```dockerfile
```

-	Layers:
	-	`sha256:3346875877893e36b6f315ac8c0f4e15d4ecc9b8a789f397eb0a12d796826ec9`  
		Last Modified: Wed, 08 Jan 2025 18:23:22 GMT  
		Size: 2.2 MB (2157753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ff1b3d80a7aff76c866c1f87ae1074caeb4344ce72f8778870cb88cc1e09a83`  
		Last Modified: Wed, 08 Jan 2025 18:23:22 GMT  
		Size: 30.7 KB (30663 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v6

```console
$ docker pull composer@sha256:e862d9712e31257f7fc6b0b980e7e63a437adb19a619d4c429b6096ea5c2ff2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70653374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16265b47f88f65659362afafcb8514da9b4b5cb06dc469c86fa8a2e67b71862e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
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
	-	`sha256:8bfbe143528e86684282cbfd298570a16342fbf7feefa882f4ff4af7f9116796`  
		Last Modified: Tue, 07 Jan 2025 18:31:35 GMT  
		Size: 30.6 MB (30640654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a227f011e7035c2e61babbdbf90fea0a1845e1422312eda1608ae428cda1dead`  
		Last Modified: Tue, 07 Jan 2025 18:31:34 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e794bfae4b6705817b1018f3ca81ea2f56bfa199ee676d595cf1a135a47d5d0`  
		Last Modified: Tue, 07 Jan 2025 18:32:15 GMT  
		Size: 734.8 KB (734830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceec54fcb2477b469f9dca645219b218dc16b9abef7401105c9053f18e97c13`  
		Last Modified: Thu, 12 Dec 2024 01:10:16 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b9fe11112ee8e527e9750c126b17a445b7f96b96ca39555816b49fb880c4a7`  
		Last Modified: Tue, 07 Jan 2025 18:32:15 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:a73f943c964db89ee098463de693fd2ef7fc3f0467d4a318647ee20d11829d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16d64f6d0243b383baf127cb45a73e787149cd76f8be97cf95e246ccc60ba91`

```dockerfile
```

-	Layers:
	-	`sha256:25a3b59798e5b19e59e29303b48987fe7b05e9f15904a361d382a9f9687f1450`  
		Last Modified: Tue, 07 Jan 2025 18:32:14 GMT  
		Size: 30.5 KB (30541 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v7

```console
$ docker pull composer@sha256:98dbf9524d30acade32d329256d86f42c8ef4a898041b1dffa9e8d1361454ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68678837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6c82849fc925f422c74dc0cae3cb1ce94f3ce271c34194873654bd63545226`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
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
	-	`sha256:0a2bf4fd23a4343e4fa39d2a63004ae4de297973415bc8809c9c56b1097caf8a`  
		Last Modified: Tue, 07 Jan 2025 18:37:42 GMT  
		Size: 30.2 MB (30150038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89da730f1c4439581b1de7342d8be357e2ea326296a6c567ba8c4e6dad0fd87e`  
		Last Modified: Tue, 07 Jan 2025 18:37:41 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e635296b448d841a4671d8cba8976a8128548552385264454ab9363c9ea5b1`  
		Last Modified: Tue, 07 Jan 2025 18:38:34 GMT  
		Size: 725.7 KB (725678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42609dc32c914fa266df15de6a777f78e70ba6565db9de8ccf3788960989a45e`  
		Last Modified: Tue, 07 Jan 2025 18:38:34 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb892cf47a78581beb2f9109828a47244da7e79953754032b32cf3353d5edb9`  
		Last Modified: Tue, 07 Jan 2025 18:38:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:4d115aaf9c292ee9e922dfe0accc2d1654e5911ec97a5ff3429adc85c800d4fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2182949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1117521ea9037cc744887e42a96f3940948c3d4b8804cca3384b4bc0de08f7c6`

```dockerfile
```

-	Layers:
	-	`sha256:76a20245842c0898732e4fe8b4781f24f82feeb4a3baf97bc48aee6f6ab79d7f`  
		Last Modified: Tue, 07 Jan 2025 18:38:34 GMT  
		Size: 2.2 MB (2152191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e53dc510835790f52cecaf4bfcfa20d40bc06220dc45e1c76729bdc7f52cb73`  
		Last Modified: Tue, 07 Jan 2025 18:38:34 GMT  
		Size: 30.8 KB (30758 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:6c17e3feffa63f178fde61a8962c57757428ef1ce893462d0fb57f6ea63d44fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74075165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b41179c347f22789f6ca556c6d271fa5b0482d7309567157dce16f5ae9df4ba1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
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
	-	`sha256:a0c59331d5588d1a35cef8b8de8c57f9df896f2230d66caa4f7510c076bcf10b`  
		Last Modified: Tue, 07 Jan 2025 16:07:22 GMT  
		Size: 32.0 MB (32004107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bc1dca7afc6e7b778ae0cc6c16db02fce566edf2e75b273bdf7c721ed764f9`  
		Last Modified: Tue, 07 Jan 2025 16:07:20 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73986a30d8c09766a7922c25bbc7ecf4e9fbe9236e8a177ecc7bc34f12b2c577`  
		Last Modified: Tue, 07 Jan 2025 16:07:59 GMT  
		Size: 734.5 KB (734546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b657f47148d28cc496448194a0537772ae6ba155719457ab23cd19f00a675c`  
		Last Modified: Tue, 07 Jan 2025 16:07:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e547aa95059343e2a89f0aa9df7dda72b796b5828057dde958cd37af5291ce37`  
		Last Modified: Tue, 07 Jan 2025 16:07:58 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:ea27965f4a612512ec0c983f7c4a9ee37177e3ef6abe01047a11996050474d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2182801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aaf63528deebd516e3ccdc065c5f00b04f2a41d5e9c0f09ae8776f387311d31`

```dockerfile
```

-	Layers:
	-	`sha256:f6464ba994123331ff950dafad28b875c34598fac050ab5b1287cff1f5d9783a`  
		Last Modified: Tue, 07 Jan 2025 16:07:58 GMT  
		Size: 2.2 MB (2152015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84fa994e814a9e6d5060d472f23a08916ba7da4d4bfb0052acc17033519bd8f7`  
		Last Modified: Tue, 07 Jan 2025 16:07:58 GMT  
		Size: 30.8 KB (30786 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; 386

```console
$ docker pull composer@sha256:21bd26cea6439d7d1e9f9d9eafd260b1e5ba0f8b133c1b23f242183e3874e99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53971076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3e7783812b8f08d1fce659d96099165946ac152e98528d07ede8555894105b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
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
	-	`sha256:06a7c334e47b7bedcfbbab866ed1535be7a5bff71e9c2f65d0853b8917b54d5e`  
		Last Modified: Wed, 08 Jan 2025 18:23:10 GMT  
		Size: 11.4 MB (11421291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7325392e6f571d6d6c867ba9360a98dcc25489b73ee76ef7f4cc6be5d7ec8b54`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e4ea9b35249bd4e2ca2be15e09178a3864525fbf2852e7c0941286a8de8232`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 709.4 KB (709426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b841e07130960846a25b675f90a14ac2263456bfa82c476d0894d4416a4f7e23`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f05948628ca40470c501b71b53616ed24606f1134506db08b96b27478c89d57`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:ac39a03fc334d90fb28898ac7b6dce23bae8cfc912ff00df602a3ed3c76f6e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.0 KB (458044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873e26b1f404f1c2276cea45d18e466c9fdeb13dd267c8a4b60f71da5ed5ba5f`

```dockerfile
```

-	Layers:
	-	`sha256:9118a3e849753adb719a1c04c2289b4b00ff09363c8b63bbe938aba7b6accd0d`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 427.4 KB (427411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ea266899259dd9be18fa15f72de37b19d0b207219e4182233502d0e7c9b7611`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 30.6 KB (30633 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; ppc64le

```console
$ docker pull composer@sha256:034c9032402ba9d9d6113328f132e54402b915dc23160478e0aacb4065fda04a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76133572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e171201126e4e2e043a04fe7fe010b8dd0ab534acd0a4ee948e8c6617008766`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
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
	-	`sha256:26aa0c6396d98d67cdb7cff725afeddc08a54386e1d5e68f922a402f902d2924`  
		Last Modified: Thu, 09 Jan 2025 01:29:00 GMT  
		Size: 32.9 MB (32943089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ed0b4e6953a4bbe30d89c2f6151304b7cf0496993f171b508a19e501ebb706`  
		Last Modified: Thu, 09 Jan 2025 01:28:58 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aff28fa1c95218da070d5a31a93ad748ea433d6ab5ff5776f30abe3042ab76c`  
		Last Modified: Thu, 09 Jan 2025 01:29:51 GMT  
		Size: 741.9 KB (741907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862fe24a45e54982220822b5fc5f1276edf39ea248d7f2faa840536d9c59dbcd`  
		Last Modified: Thu, 09 Jan 2025 01:29:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6de68302ba03894226251cb89d18b55f6f4a00479bfefff88afa83c312d6396`  
		Last Modified: Thu, 09 Jan 2025 01:29:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:14a21f897f80deb748d02ce783bb7a9d1836e046bde73f8445b482fef7396171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9eaf39b885db4cc415e7cd5f9dfe941372d2f91596d9eea845bbec0c60dec7`

```dockerfile
```

-	Layers:
	-	`sha256:a65e9e9a573158545be8615b92246ba838ce73b2b03b30d190ae1bc00bac3973`  
		Last Modified: Thu, 09 Jan 2025 01:29:51 GMT  
		Size: 2.2 MB (2156310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a75a723e899f00acecc4fd3c1b3b978868bb538601e0dc91205884695a20790`  
		Last Modified: Thu, 09 Jan 2025 01:29:51 GMT  
		Size: 30.7 KB (30706 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; riscv64

```console
$ docker pull composer@sha256:20800139ab857e1ae32895e31dbcd06ca9bd5783439c31abb52e4fad8edf7114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73492700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7195f32a1fe5dfe205bf99e9e69fe8a8aa6de04a052aa9123429990ac8d82cc8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
		Size: 3.4 MB (3445761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9c93fa8ac38e6017fe5251627d738084239fbab425319ead8bdece897e493`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe2d3ee20829a994ce6548409e985a58c1c6ec2238583410057ae0e6dfe95a1`  
		Last Modified: Fri, 20 Dec 2024 22:27:49 GMT  
		Size: 13.6 MB (13580504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a67918c3771135e7a2b16f42498ea94d985dc8f6407db3a3ee60e1e3e9373b`  
		Last Modified: Fri, 20 Dec 2024 22:27:47 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e567d61ea86fdc5c63b8ce75eb88bcda35c75049600dcb0b112964a7da3ac42f`  
		Last Modified: Fri, 20 Dec 2024 22:27:50 GMT  
		Size: 20.8 MB (20797397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263bcc5a009f020e39d0e162f139f8f8433852481d7368c9cde637ffd9f841e5`  
		Last Modified: Fri, 20 Dec 2024 22:27:47 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9ec8a613ce316b270ee3a65ed2d2041d6579061f1f8b0d0725f55b6f9e84fc`  
		Last Modified: Fri, 20 Dec 2024 22:27:48 GMT  
		Size: 19.9 KB (19885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe21f96e7307414693b828f2173bcaa37df5cd8443ce028ad761b4e69270f7`  
		Last Modified: Sat, 21 Dec 2024 14:35:27 GMT  
		Size: 31.0 MB (31000197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4008aa8424d8743580595dbf0803a9aa275eb20020eb2e8e47ed5c19aeeee6bf`  
		Last Modified: Sat, 21 Dec 2024 14:35:22 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a14b849fe13061781f4997ff034beb7d7e7efc1906f682820d8670d267bcda`  
		Last Modified: Sat, 21 Dec 2024 14:40:34 GMT  
		Size: 1.3 MB (1290064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7315de22cb12057db543b8aa66851c16de951dcb7a67f300b3830603a6c9133a`  
		Last Modified: Sat, 21 Dec 2024 14:40:34 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae8a332fa05680425ba7da4e17c586392bf75e58b2669f7fb3d8baa5dacb38b`  
		Last Modified: Sat, 21 Dec 2024 14:40:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:ef8b2ce91749f276965645085bb4a7c42bece35e36e8527d772126590d52d058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dcb4c33b9179b7a3d87189a04786f5d83345fd1665a31467ed21df003d0cb2`

```dockerfile
```

-	Layers:
	-	`sha256:c42ea4c3452055a708038243c0d8b6e98c54ee7b2c20cbae799325a74c9e3ee0`  
		Last Modified: Sat, 21 Dec 2024 14:40:34 GMT  
		Size: 2.2 MB (2156552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3be44d5530fea8b3c03296e7a24cf32ee2b7078832d37cd59448c9daba90bc4d`  
		Last Modified: Sat, 21 Dec 2024 14:40:33 GMT  
		Size: 30.7 KB (30708 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; s390x

```console
$ docker pull composer@sha256:6229d42bde23b8768377fdf65985776abb7ffc8514042204f0ead18c87cdb3fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74389732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc272a3915f22a923288a3d45775e1fb995abe36c8438b41922d9d4f2dea1fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
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
	-	`sha256:3f63ed19a544e5e26e1152afe55e1e34f250a8fe3982b62ef0754513377c899c`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 31.7 MB (31674581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59aadc194319e2220294cf3ff3a08addb3a57ecf676d4fb858a0ff81e0bd6c8d`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c138d2282ae5aae067e693eb06174a49d9a826ebbf642ac7c6ec59d64d4ae21`  
		Last Modified: Tue, 07 Jan 2025 15:52:36 GMT  
		Size: 737.8 KB (737803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afc145711085542bc482d840451d9e52cb86ab586f834f7da2df3d9fc7d5124`  
		Last Modified: Tue, 07 Jan 2025 15:52:36 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4bd4a668d2a2ed5a09f3e68adae7505113fcfece0888af5d060b744b511b8b`  
		Last Modified: Tue, 07 Jan 2025 15:52:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:b93f96d27b951efd7038b3f071693e46761ad0775829516b9686f4f9736afa64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f8d25c5f017fce69ccec533ccae54e8a6273c3f52121d35eea6b87abc3a3b4`

```dockerfile
```

-	Layers:
	-	`sha256:49170b78fc956a02eb723b0e41be238e4f5b6c681b655f03fb9200630daf9a36`  
		Last Modified: Tue, 07 Jan 2025 15:52:35 GMT  
		Size: 2.1 MB (2149160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9180cd61e016631dbcb2c0ac3a81cf0dc9be3f5372b7bb0aaffa18110579735`  
		Last Modified: Tue, 07 Jan 2025 15:52:35 GMT  
		Size: 30.7 KB (30664 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10`

```console
$ docker pull composer@sha256:955962b2bad33bc86e82dfeffcfaf558ae65f977ce52139c5bd0fd49ed045549
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

### `composer:1.10` - linux; amd64

```console
$ docker pull composer@sha256:6b2f16390a7eadc1e9ca1ff139c2d12f6673514054c91752e513749cc47a597f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74095403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38a56acb18557cfb93f82b3c8f039460811b182ab8aa7f8584a6deacfa3b4c2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
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
	-	`sha256:e0baa056e21bcab81c2acc5425ed67c40a2988d923a3def22fa0d8050cadda8a`  
		Last Modified: Wed, 08 Jan 2025 18:23:23 GMT  
		Size: 31.9 MB (31896629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d559b6b0eff1bbb1c50a1df8bbe104b308b9e9e9b322cbadf11f5397753c46d`  
		Last Modified: Wed, 08 Jan 2025 18:23:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2476acf1da8f88db250c313c5274e7d11c4e7621977c094f8ffd6327244702`  
		Last Modified: Wed, 08 Jan 2025 18:23:23 GMT  
		Size: 734.8 KB (734786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b18feab52adf6434ad9b56755607fb54747e39e2cf3b420628d9f7db124f084`  
		Last Modified: Wed, 08 Jan 2025 18:23:22 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7697754ff51986cb09fd9446d5106596f8e01b2ec9416923e7ee18e0e2865986`  
		Last Modified: Wed, 08 Jan 2025 18:23:23 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:703fab1901cd1587c27f5cad46f45b8253432a2a2a8e63abdd64ba50a4b4f03e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42f044d0c6fbfb26beaf4f8e255146492781eb7dcdf971a3cca32f59e1403e6`

```dockerfile
```

-	Layers:
	-	`sha256:3346875877893e36b6f315ac8c0f4e15d4ecc9b8a789f397eb0a12d796826ec9`  
		Last Modified: Wed, 08 Jan 2025 18:23:22 GMT  
		Size: 2.2 MB (2157753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ff1b3d80a7aff76c866c1f87ae1074caeb4344ce72f8778870cb88cc1e09a83`  
		Last Modified: Wed, 08 Jan 2025 18:23:22 GMT  
		Size: 30.7 KB (30663 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v6

```console
$ docker pull composer@sha256:e862d9712e31257f7fc6b0b980e7e63a437adb19a619d4c429b6096ea5c2ff2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70653374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16265b47f88f65659362afafcb8514da9b4b5cb06dc469c86fa8a2e67b71862e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
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
	-	`sha256:8bfbe143528e86684282cbfd298570a16342fbf7feefa882f4ff4af7f9116796`  
		Last Modified: Tue, 07 Jan 2025 18:31:35 GMT  
		Size: 30.6 MB (30640654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a227f011e7035c2e61babbdbf90fea0a1845e1422312eda1608ae428cda1dead`  
		Last Modified: Tue, 07 Jan 2025 18:31:34 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e794bfae4b6705817b1018f3ca81ea2f56bfa199ee676d595cf1a135a47d5d0`  
		Last Modified: Tue, 07 Jan 2025 18:32:15 GMT  
		Size: 734.8 KB (734830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceec54fcb2477b469f9dca645219b218dc16b9abef7401105c9053f18e97c13`  
		Last Modified: Thu, 12 Dec 2024 01:10:16 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b9fe11112ee8e527e9750c126b17a445b7f96b96ca39555816b49fb880c4a7`  
		Last Modified: Tue, 07 Jan 2025 18:32:15 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:a73f943c964db89ee098463de693fd2ef7fc3f0467d4a318647ee20d11829d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16d64f6d0243b383baf127cb45a73e787149cd76f8be97cf95e246ccc60ba91`

```dockerfile
```

-	Layers:
	-	`sha256:25a3b59798e5b19e59e29303b48987fe7b05e9f15904a361d382a9f9687f1450`  
		Last Modified: Tue, 07 Jan 2025 18:32:14 GMT  
		Size: 30.5 KB (30541 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v7

```console
$ docker pull composer@sha256:98dbf9524d30acade32d329256d86f42c8ef4a898041b1dffa9e8d1361454ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68678837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6c82849fc925f422c74dc0cae3cb1ce94f3ce271c34194873654bd63545226`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
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
	-	`sha256:0a2bf4fd23a4343e4fa39d2a63004ae4de297973415bc8809c9c56b1097caf8a`  
		Last Modified: Tue, 07 Jan 2025 18:37:42 GMT  
		Size: 30.2 MB (30150038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89da730f1c4439581b1de7342d8be357e2ea326296a6c567ba8c4e6dad0fd87e`  
		Last Modified: Tue, 07 Jan 2025 18:37:41 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e635296b448d841a4671d8cba8976a8128548552385264454ab9363c9ea5b1`  
		Last Modified: Tue, 07 Jan 2025 18:38:34 GMT  
		Size: 725.7 KB (725678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42609dc32c914fa266df15de6a777f78e70ba6565db9de8ccf3788960989a45e`  
		Last Modified: Tue, 07 Jan 2025 18:38:34 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb892cf47a78581beb2f9109828a47244da7e79953754032b32cf3353d5edb9`  
		Last Modified: Tue, 07 Jan 2025 18:38:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:4d115aaf9c292ee9e922dfe0accc2d1654e5911ec97a5ff3429adc85c800d4fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2182949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1117521ea9037cc744887e42a96f3940948c3d4b8804cca3384b4bc0de08f7c6`

```dockerfile
```

-	Layers:
	-	`sha256:76a20245842c0898732e4fe8b4781f24f82feeb4a3baf97bc48aee6f6ab79d7f`  
		Last Modified: Tue, 07 Jan 2025 18:38:34 GMT  
		Size: 2.2 MB (2152191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e53dc510835790f52cecaf4bfcfa20d40bc06220dc45e1c76729bdc7f52cb73`  
		Last Modified: Tue, 07 Jan 2025 18:38:34 GMT  
		Size: 30.8 KB (30758 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:6c17e3feffa63f178fde61a8962c57757428ef1ce893462d0fb57f6ea63d44fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74075165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b41179c347f22789f6ca556c6d271fa5b0482d7309567157dce16f5ae9df4ba1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
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
	-	`sha256:a0c59331d5588d1a35cef8b8de8c57f9df896f2230d66caa4f7510c076bcf10b`  
		Last Modified: Tue, 07 Jan 2025 16:07:22 GMT  
		Size: 32.0 MB (32004107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bc1dca7afc6e7b778ae0cc6c16db02fce566edf2e75b273bdf7c721ed764f9`  
		Last Modified: Tue, 07 Jan 2025 16:07:20 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73986a30d8c09766a7922c25bbc7ecf4e9fbe9236e8a177ecc7bc34f12b2c577`  
		Last Modified: Tue, 07 Jan 2025 16:07:59 GMT  
		Size: 734.5 KB (734546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b657f47148d28cc496448194a0537772ae6ba155719457ab23cd19f00a675c`  
		Last Modified: Tue, 07 Jan 2025 16:07:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e547aa95059343e2a89f0aa9df7dda72b796b5828057dde958cd37af5291ce37`  
		Last Modified: Tue, 07 Jan 2025 16:07:58 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:ea27965f4a612512ec0c983f7c4a9ee37177e3ef6abe01047a11996050474d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2182801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aaf63528deebd516e3ccdc065c5f00b04f2a41d5e9c0f09ae8776f387311d31`

```dockerfile
```

-	Layers:
	-	`sha256:f6464ba994123331ff950dafad28b875c34598fac050ab5b1287cff1f5d9783a`  
		Last Modified: Tue, 07 Jan 2025 16:07:58 GMT  
		Size: 2.2 MB (2152015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84fa994e814a9e6d5060d472f23a08916ba7da4d4bfb0052acc17033519bd8f7`  
		Last Modified: Tue, 07 Jan 2025 16:07:58 GMT  
		Size: 30.8 KB (30786 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; 386

```console
$ docker pull composer@sha256:21bd26cea6439d7d1e9f9d9eafd260b1e5ba0f8b133c1b23f242183e3874e99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53971076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3e7783812b8f08d1fce659d96099165946ac152e98528d07ede8555894105b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
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
	-	`sha256:06a7c334e47b7bedcfbbab866ed1535be7a5bff71e9c2f65d0853b8917b54d5e`  
		Last Modified: Wed, 08 Jan 2025 18:23:10 GMT  
		Size: 11.4 MB (11421291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7325392e6f571d6d6c867ba9360a98dcc25489b73ee76ef7f4cc6be5d7ec8b54`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e4ea9b35249bd4e2ca2be15e09178a3864525fbf2852e7c0941286a8de8232`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 709.4 KB (709426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b841e07130960846a25b675f90a14ac2263456bfa82c476d0894d4416a4f7e23`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f05948628ca40470c501b71b53616ed24606f1134506db08b96b27478c89d57`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:ac39a03fc334d90fb28898ac7b6dce23bae8cfc912ff00df602a3ed3c76f6e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.0 KB (458044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873e26b1f404f1c2276cea45d18e466c9fdeb13dd267c8a4b60f71da5ed5ba5f`

```dockerfile
```

-	Layers:
	-	`sha256:9118a3e849753adb719a1c04c2289b4b00ff09363c8b63bbe938aba7b6accd0d`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 427.4 KB (427411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ea266899259dd9be18fa15f72de37b19d0b207219e4182233502d0e7c9b7611`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 30.6 KB (30633 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; ppc64le

```console
$ docker pull composer@sha256:034c9032402ba9d9d6113328f132e54402b915dc23160478e0aacb4065fda04a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76133572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e171201126e4e2e043a04fe7fe010b8dd0ab534acd0a4ee948e8c6617008766`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
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
	-	`sha256:26aa0c6396d98d67cdb7cff725afeddc08a54386e1d5e68f922a402f902d2924`  
		Last Modified: Thu, 09 Jan 2025 01:29:00 GMT  
		Size: 32.9 MB (32943089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ed0b4e6953a4bbe30d89c2f6151304b7cf0496993f171b508a19e501ebb706`  
		Last Modified: Thu, 09 Jan 2025 01:28:58 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aff28fa1c95218da070d5a31a93ad748ea433d6ab5ff5776f30abe3042ab76c`  
		Last Modified: Thu, 09 Jan 2025 01:29:51 GMT  
		Size: 741.9 KB (741907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862fe24a45e54982220822b5fc5f1276edf39ea248d7f2faa840536d9c59dbcd`  
		Last Modified: Thu, 09 Jan 2025 01:29:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6de68302ba03894226251cb89d18b55f6f4a00479bfefff88afa83c312d6396`  
		Last Modified: Thu, 09 Jan 2025 01:29:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:14a21f897f80deb748d02ce783bb7a9d1836e046bde73f8445b482fef7396171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9eaf39b885db4cc415e7cd5f9dfe941372d2f91596d9eea845bbec0c60dec7`

```dockerfile
```

-	Layers:
	-	`sha256:a65e9e9a573158545be8615b92246ba838ce73b2b03b30d190ae1bc00bac3973`  
		Last Modified: Thu, 09 Jan 2025 01:29:51 GMT  
		Size: 2.2 MB (2156310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a75a723e899f00acecc4fd3c1b3b978868bb538601e0dc91205884695a20790`  
		Last Modified: Thu, 09 Jan 2025 01:29:51 GMT  
		Size: 30.7 KB (30706 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; riscv64

```console
$ docker pull composer@sha256:20800139ab857e1ae32895e31dbcd06ca9bd5783439c31abb52e4fad8edf7114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73492700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7195f32a1fe5dfe205bf99e9e69fe8a8aa6de04a052aa9123429990ac8d82cc8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
		Size: 3.4 MB (3445761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9c93fa8ac38e6017fe5251627d738084239fbab425319ead8bdece897e493`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe2d3ee20829a994ce6548409e985a58c1c6ec2238583410057ae0e6dfe95a1`  
		Last Modified: Fri, 20 Dec 2024 22:27:49 GMT  
		Size: 13.6 MB (13580504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a67918c3771135e7a2b16f42498ea94d985dc8f6407db3a3ee60e1e3e9373b`  
		Last Modified: Fri, 20 Dec 2024 22:27:47 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e567d61ea86fdc5c63b8ce75eb88bcda35c75049600dcb0b112964a7da3ac42f`  
		Last Modified: Fri, 20 Dec 2024 22:27:50 GMT  
		Size: 20.8 MB (20797397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263bcc5a009f020e39d0e162f139f8f8433852481d7368c9cde637ffd9f841e5`  
		Last Modified: Fri, 20 Dec 2024 22:27:47 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9ec8a613ce316b270ee3a65ed2d2041d6579061f1f8b0d0725f55b6f9e84fc`  
		Last Modified: Fri, 20 Dec 2024 22:27:48 GMT  
		Size: 19.9 KB (19885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe21f96e7307414693b828f2173bcaa37df5cd8443ce028ad761b4e69270f7`  
		Last Modified: Sat, 21 Dec 2024 14:35:27 GMT  
		Size: 31.0 MB (31000197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4008aa8424d8743580595dbf0803a9aa275eb20020eb2e8e47ed5c19aeeee6bf`  
		Last Modified: Sat, 21 Dec 2024 14:35:22 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a14b849fe13061781f4997ff034beb7d7e7efc1906f682820d8670d267bcda`  
		Last Modified: Sat, 21 Dec 2024 14:40:34 GMT  
		Size: 1.3 MB (1290064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7315de22cb12057db543b8aa66851c16de951dcb7a67f300b3830603a6c9133a`  
		Last Modified: Sat, 21 Dec 2024 14:40:34 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae8a332fa05680425ba7da4e17c586392bf75e58b2669f7fb3d8baa5dacb38b`  
		Last Modified: Sat, 21 Dec 2024 14:40:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:ef8b2ce91749f276965645085bb4a7c42bece35e36e8527d772126590d52d058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dcb4c33b9179b7a3d87189a04786f5d83345fd1665a31467ed21df003d0cb2`

```dockerfile
```

-	Layers:
	-	`sha256:c42ea4c3452055a708038243c0d8b6e98c54ee7b2c20cbae799325a74c9e3ee0`  
		Last Modified: Sat, 21 Dec 2024 14:40:34 GMT  
		Size: 2.2 MB (2156552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3be44d5530fea8b3c03296e7a24cf32ee2b7078832d37cd59448c9daba90bc4d`  
		Last Modified: Sat, 21 Dec 2024 14:40:33 GMT  
		Size: 30.7 KB (30708 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; s390x

```console
$ docker pull composer@sha256:6229d42bde23b8768377fdf65985776abb7ffc8514042204f0ead18c87cdb3fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74389732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc272a3915f22a923288a3d45775e1fb995abe36c8438b41922d9d4f2dea1fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
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
	-	`sha256:3f63ed19a544e5e26e1152afe55e1e34f250a8fe3982b62ef0754513377c899c`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 31.7 MB (31674581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59aadc194319e2220294cf3ff3a08addb3a57ecf676d4fb858a0ff81e0bd6c8d`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c138d2282ae5aae067e693eb06174a49d9a826ebbf642ac7c6ec59d64d4ae21`  
		Last Modified: Tue, 07 Jan 2025 15:52:36 GMT  
		Size: 737.8 KB (737803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afc145711085542bc482d840451d9e52cb86ab586f834f7da2df3d9fc7d5124`  
		Last Modified: Tue, 07 Jan 2025 15:52:36 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4bd4a668d2a2ed5a09f3e68adae7505113fcfece0888af5d060b744b511b8b`  
		Last Modified: Tue, 07 Jan 2025 15:52:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:b93f96d27b951efd7038b3f071693e46761ad0775829516b9686f4f9736afa64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f8d25c5f017fce69ccec533ccae54e8a6273c3f52121d35eea6b87abc3a3b4`

```dockerfile
```

-	Layers:
	-	`sha256:49170b78fc956a02eb723b0e41be238e4f5b6c681b655f03fb9200630daf9a36`  
		Last Modified: Tue, 07 Jan 2025 15:52:35 GMT  
		Size: 2.1 MB (2149160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9180cd61e016631dbcb2c0ac3a81cf0dc9be3f5372b7bb0aaffa18110579735`  
		Last Modified: Tue, 07 Jan 2025 15:52:35 GMT  
		Size: 30.7 KB (30664 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10.27`

```console
$ docker pull composer@sha256:955962b2bad33bc86e82dfeffcfaf558ae65f977ce52139c5bd0fd49ed045549
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

### `composer:1.10.27` - linux; amd64

```console
$ docker pull composer@sha256:6b2f16390a7eadc1e9ca1ff139c2d12f6673514054c91752e513749cc47a597f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74095403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38a56acb18557cfb93f82b3c8f039460811b182ab8aa7f8584a6deacfa3b4c2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
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
	-	`sha256:e0baa056e21bcab81c2acc5425ed67c40a2988d923a3def22fa0d8050cadda8a`  
		Last Modified: Wed, 08 Jan 2025 18:23:23 GMT  
		Size: 31.9 MB (31896629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d559b6b0eff1bbb1c50a1df8bbe104b308b9e9e9b322cbadf11f5397753c46d`  
		Last Modified: Wed, 08 Jan 2025 18:23:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2476acf1da8f88db250c313c5274e7d11c4e7621977c094f8ffd6327244702`  
		Last Modified: Wed, 08 Jan 2025 18:23:23 GMT  
		Size: 734.8 KB (734786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b18feab52adf6434ad9b56755607fb54747e39e2cf3b420628d9f7db124f084`  
		Last Modified: Wed, 08 Jan 2025 18:23:22 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7697754ff51986cb09fd9446d5106596f8e01b2ec9416923e7ee18e0e2865986`  
		Last Modified: Wed, 08 Jan 2025 18:23:23 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:703fab1901cd1587c27f5cad46f45b8253432a2a2a8e63abdd64ba50a4b4f03e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42f044d0c6fbfb26beaf4f8e255146492781eb7dcdf971a3cca32f59e1403e6`

```dockerfile
```

-	Layers:
	-	`sha256:3346875877893e36b6f315ac8c0f4e15d4ecc9b8a789f397eb0a12d796826ec9`  
		Last Modified: Wed, 08 Jan 2025 18:23:22 GMT  
		Size: 2.2 MB (2157753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ff1b3d80a7aff76c866c1f87ae1074caeb4344ce72f8778870cb88cc1e09a83`  
		Last Modified: Wed, 08 Jan 2025 18:23:22 GMT  
		Size: 30.7 KB (30663 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v6

```console
$ docker pull composer@sha256:e862d9712e31257f7fc6b0b980e7e63a437adb19a619d4c429b6096ea5c2ff2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70653374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16265b47f88f65659362afafcb8514da9b4b5cb06dc469c86fa8a2e67b71862e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
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
	-	`sha256:8bfbe143528e86684282cbfd298570a16342fbf7feefa882f4ff4af7f9116796`  
		Last Modified: Tue, 07 Jan 2025 18:31:35 GMT  
		Size: 30.6 MB (30640654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a227f011e7035c2e61babbdbf90fea0a1845e1422312eda1608ae428cda1dead`  
		Last Modified: Tue, 07 Jan 2025 18:31:34 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e794bfae4b6705817b1018f3ca81ea2f56bfa199ee676d595cf1a135a47d5d0`  
		Last Modified: Tue, 07 Jan 2025 18:32:15 GMT  
		Size: 734.8 KB (734830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceec54fcb2477b469f9dca645219b218dc16b9abef7401105c9053f18e97c13`  
		Last Modified: Thu, 12 Dec 2024 01:10:16 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b9fe11112ee8e527e9750c126b17a445b7f96b96ca39555816b49fb880c4a7`  
		Last Modified: Tue, 07 Jan 2025 18:32:15 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:a73f943c964db89ee098463de693fd2ef7fc3f0467d4a318647ee20d11829d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16d64f6d0243b383baf127cb45a73e787149cd76f8be97cf95e246ccc60ba91`

```dockerfile
```

-	Layers:
	-	`sha256:25a3b59798e5b19e59e29303b48987fe7b05e9f15904a361d382a9f9687f1450`  
		Last Modified: Tue, 07 Jan 2025 18:32:14 GMT  
		Size: 30.5 KB (30541 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v7

```console
$ docker pull composer@sha256:98dbf9524d30acade32d329256d86f42c8ef4a898041b1dffa9e8d1361454ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68678837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6c82849fc925f422c74dc0cae3cb1ce94f3ce271c34194873654bd63545226`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
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
	-	`sha256:0a2bf4fd23a4343e4fa39d2a63004ae4de297973415bc8809c9c56b1097caf8a`  
		Last Modified: Tue, 07 Jan 2025 18:37:42 GMT  
		Size: 30.2 MB (30150038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89da730f1c4439581b1de7342d8be357e2ea326296a6c567ba8c4e6dad0fd87e`  
		Last Modified: Tue, 07 Jan 2025 18:37:41 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e635296b448d841a4671d8cba8976a8128548552385264454ab9363c9ea5b1`  
		Last Modified: Tue, 07 Jan 2025 18:38:34 GMT  
		Size: 725.7 KB (725678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42609dc32c914fa266df15de6a777f78e70ba6565db9de8ccf3788960989a45e`  
		Last Modified: Tue, 07 Jan 2025 18:38:34 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb892cf47a78581beb2f9109828a47244da7e79953754032b32cf3353d5edb9`  
		Last Modified: Tue, 07 Jan 2025 18:38:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:4d115aaf9c292ee9e922dfe0accc2d1654e5911ec97a5ff3429adc85c800d4fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2182949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1117521ea9037cc744887e42a96f3940948c3d4b8804cca3384b4bc0de08f7c6`

```dockerfile
```

-	Layers:
	-	`sha256:76a20245842c0898732e4fe8b4781f24f82feeb4a3baf97bc48aee6f6ab79d7f`  
		Last Modified: Tue, 07 Jan 2025 18:38:34 GMT  
		Size: 2.2 MB (2152191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e53dc510835790f52cecaf4bfcfa20d40bc06220dc45e1c76729bdc7f52cb73`  
		Last Modified: Tue, 07 Jan 2025 18:38:34 GMT  
		Size: 30.8 KB (30758 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:6c17e3feffa63f178fde61a8962c57757428ef1ce893462d0fb57f6ea63d44fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74075165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b41179c347f22789f6ca556c6d271fa5b0482d7309567157dce16f5ae9df4ba1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
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
	-	`sha256:a0c59331d5588d1a35cef8b8de8c57f9df896f2230d66caa4f7510c076bcf10b`  
		Last Modified: Tue, 07 Jan 2025 16:07:22 GMT  
		Size: 32.0 MB (32004107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bc1dca7afc6e7b778ae0cc6c16db02fce566edf2e75b273bdf7c721ed764f9`  
		Last Modified: Tue, 07 Jan 2025 16:07:20 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73986a30d8c09766a7922c25bbc7ecf4e9fbe9236e8a177ecc7bc34f12b2c577`  
		Last Modified: Tue, 07 Jan 2025 16:07:59 GMT  
		Size: 734.5 KB (734546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b657f47148d28cc496448194a0537772ae6ba155719457ab23cd19f00a675c`  
		Last Modified: Tue, 07 Jan 2025 16:07:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e547aa95059343e2a89f0aa9df7dda72b796b5828057dde958cd37af5291ce37`  
		Last Modified: Tue, 07 Jan 2025 16:07:58 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:ea27965f4a612512ec0c983f7c4a9ee37177e3ef6abe01047a11996050474d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2182801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aaf63528deebd516e3ccdc065c5f00b04f2a41d5e9c0f09ae8776f387311d31`

```dockerfile
```

-	Layers:
	-	`sha256:f6464ba994123331ff950dafad28b875c34598fac050ab5b1287cff1f5d9783a`  
		Last Modified: Tue, 07 Jan 2025 16:07:58 GMT  
		Size: 2.2 MB (2152015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84fa994e814a9e6d5060d472f23a08916ba7da4d4bfb0052acc17033519bd8f7`  
		Last Modified: Tue, 07 Jan 2025 16:07:58 GMT  
		Size: 30.8 KB (30786 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; 386

```console
$ docker pull composer@sha256:21bd26cea6439d7d1e9f9d9eafd260b1e5ba0f8b133c1b23f242183e3874e99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53971076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3e7783812b8f08d1fce659d96099165946ac152e98528d07ede8555894105b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
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
	-	`sha256:06a7c334e47b7bedcfbbab866ed1535be7a5bff71e9c2f65d0853b8917b54d5e`  
		Last Modified: Wed, 08 Jan 2025 18:23:10 GMT  
		Size: 11.4 MB (11421291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7325392e6f571d6d6c867ba9360a98dcc25489b73ee76ef7f4cc6be5d7ec8b54`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e4ea9b35249bd4e2ca2be15e09178a3864525fbf2852e7c0941286a8de8232`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 709.4 KB (709426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b841e07130960846a25b675f90a14ac2263456bfa82c476d0894d4416a4f7e23`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f05948628ca40470c501b71b53616ed24606f1134506db08b96b27478c89d57`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:ac39a03fc334d90fb28898ac7b6dce23bae8cfc912ff00df602a3ed3c76f6e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.0 KB (458044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873e26b1f404f1c2276cea45d18e466c9fdeb13dd267c8a4b60f71da5ed5ba5f`

```dockerfile
```

-	Layers:
	-	`sha256:9118a3e849753adb719a1c04c2289b4b00ff09363c8b63bbe938aba7b6accd0d`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 427.4 KB (427411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ea266899259dd9be18fa15f72de37b19d0b207219e4182233502d0e7c9b7611`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 30.6 KB (30633 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; ppc64le

```console
$ docker pull composer@sha256:034c9032402ba9d9d6113328f132e54402b915dc23160478e0aacb4065fda04a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76133572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e171201126e4e2e043a04fe7fe010b8dd0ab534acd0a4ee948e8c6617008766`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
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
	-	`sha256:26aa0c6396d98d67cdb7cff725afeddc08a54386e1d5e68f922a402f902d2924`  
		Last Modified: Thu, 09 Jan 2025 01:29:00 GMT  
		Size: 32.9 MB (32943089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ed0b4e6953a4bbe30d89c2f6151304b7cf0496993f171b508a19e501ebb706`  
		Last Modified: Thu, 09 Jan 2025 01:28:58 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aff28fa1c95218da070d5a31a93ad748ea433d6ab5ff5776f30abe3042ab76c`  
		Last Modified: Thu, 09 Jan 2025 01:29:51 GMT  
		Size: 741.9 KB (741907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862fe24a45e54982220822b5fc5f1276edf39ea248d7f2faa840536d9c59dbcd`  
		Last Modified: Thu, 09 Jan 2025 01:29:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6de68302ba03894226251cb89d18b55f6f4a00479bfefff88afa83c312d6396`  
		Last Modified: Thu, 09 Jan 2025 01:29:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:14a21f897f80deb748d02ce783bb7a9d1836e046bde73f8445b482fef7396171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9eaf39b885db4cc415e7cd5f9dfe941372d2f91596d9eea845bbec0c60dec7`

```dockerfile
```

-	Layers:
	-	`sha256:a65e9e9a573158545be8615b92246ba838ce73b2b03b30d190ae1bc00bac3973`  
		Last Modified: Thu, 09 Jan 2025 01:29:51 GMT  
		Size: 2.2 MB (2156310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a75a723e899f00acecc4fd3c1b3b978868bb538601e0dc91205884695a20790`  
		Last Modified: Thu, 09 Jan 2025 01:29:51 GMT  
		Size: 30.7 KB (30706 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; riscv64

```console
$ docker pull composer@sha256:20800139ab857e1ae32895e31dbcd06ca9bd5783439c31abb52e4fad8edf7114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73492700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7195f32a1fe5dfe205bf99e9e69fe8a8aa6de04a052aa9123429990ac8d82cc8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
		Size: 3.4 MB (3445761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9c93fa8ac38e6017fe5251627d738084239fbab425319ead8bdece897e493`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe2d3ee20829a994ce6548409e985a58c1c6ec2238583410057ae0e6dfe95a1`  
		Last Modified: Fri, 20 Dec 2024 22:27:49 GMT  
		Size: 13.6 MB (13580504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a67918c3771135e7a2b16f42498ea94d985dc8f6407db3a3ee60e1e3e9373b`  
		Last Modified: Fri, 20 Dec 2024 22:27:47 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e567d61ea86fdc5c63b8ce75eb88bcda35c75049600dcb0b112964a7da3ac42f`  
		Last Modified: Fri, 20 Dec 2024 22:27:50 GMT  
		Size: 20.8 MB (20797397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263bcc5a009f020e39d0e162f139f8f8433852481d7368c9cde637ffd9f841e5`  
		Last Modified: Fri, 20 Dec 2024 22:27:47 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9ec8a613ce316b270ee3a65ed2d2041d6579061f1f8b0d0725f55b6f9e84fc`  
		Last Modified: Fri, 20 Dec 2024 22:27:48 GMT  
		Size: 19.9 KB (19885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe21f96e7307414693b828f2173bcaa37df5cd8443ce028ad761b4e69270f7`  
		Last Modified: Sat, 21 Dec 2024 14:35:27 GMT  
		Size: 31.0 MB (31000197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4008aa8424d8743580595dbf0803a9aa275eb20020eb2e8e47ed5c19aeeee6bf`  
		Last Modified: Sat, 21 Dec 2024 14:35:22 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a14b849fe13061781f4997ff034beb7d7e7efc1906f682820d8670d267bcda`  
		Last Modified: Sat, 21 Dec 2024 14:40:34 GMT  
		Size: 1.3 MB (1290064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7315de22cb12057db543b8aa66851c16de951dcb7a67f300b3830603a6c9133a`  
		Last Modified: Sat, 21 Dec 2024 14:40:34 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae8a332fa05680425ba7da4e17c586392bf75e58b2669f7fb3d8baa5dacb38b`  
		Last Modified: Sat, 21 Dec 2024 14:40:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:ef8b2ce91749f276965645085bb4a7c42bece35e36e8527d772126590d52d058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dcb4c33b9179b7a3d87189a04786f5d83345fd1665a31467ed21df003d0cb2`

```dockerfile
```

-	Layers:
	-	`sha256:c42ea4c3452055a708038243c0d8b6e98c54ee7b2c20cbae799325a74c9e3ee0`  
		Last Modified: Sat, 21 Dec 2024 14:40:34 GMT  
		Size: 2.2 MB (2156552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3be44d5530fea8b3c03296e7a24cf32ee2b7078832d37cd59448c9daba90bc4d`  
		Last Modified: Sat, 21 Dec 2024 14:40:33 GMT  
		Size: 30.7 KB (30708 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; s390x

```console
$ docker pull composer@sha256:6229d42bde23b8768377fdf65985776abb7ffc8514042204f0ead18c87cdb3fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74389732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc272a3915f22a923288a3d45775e1fb995abe36c8438b41922d9d4f2dea1fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
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
	-	`sha256:3f63ed19a544e5e26e1152afe55e1e34f250a8fe3982b62ef0754513377c899c`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 31.7 MB (31674581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59aadc194319e2220294cf3ff3a08addb3a57ecf676d4fb858a0ff81e0bd6c8d`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c138d2282ae5aae067e693eb06174a49d9a826ebbf642ac7c6ec59d64d4ae21`  
		Last Modified: Tue, 07 Jan 2025 15:52:36 GMT  
		Size: 737.8 KB (737803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afc145711085542bc482d840451d9e52cb86ab586f834f7da2df3d9fc7d5124`  
		Last Modified: Tue, 07 Jan 2025 15:52:36 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4bd4a668d2a2ed5a09f3e68adae7505113fcfece0888af5d060b744b511b8b`  
		Last Modified: Tue, 07 Jan 2025 15:52:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:b93f96d27b951efd7038b3f071693e46761ad0775829516b9686f4f9736afa64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f8d25c5f017fce69ccec533ccae54e8a6273c3f52121d35eea6b87abc3a3b4`

```dockerfile
```

-	Layers:
	-	`sha256:49170b78fc956a02eb723b0e41be238e4f5b6c681b655f03fb9200630daf9a36`  
		Last Modified: Tue, 07 Jan 2025 15:52:35 GMT  
		Size: 2.1 MB (2149160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9180cd61e016631dbcb2c0ac3a81cf0dc9be3f5372b7bb0aaffa18110579735`  
		Last Modified: Tue, 07 Jan 2025 15:52:35 GMT  
		Size: 30.7 KB (30664 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2`

```console
$ docker pull composer@sha256:5343ca2d163000fc433898aba00818152bece4bf10d46745102378ace3964eed
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

### `composer:2` - linux; amd64

```console
$ docker pull composer@sha256:005298f3a8e453451ef3bf7b15bea492d29101a86bfa8407341d0b12038767ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74326216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53abc0a37f7ee2356900dd8be0983112aca615687e2fdcff5cd9232b69ca7b09`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:978a5b5b12769c41e9b5454d72092585972d47afc882215a4e67bfc88f493d5b`  
		Last Modified: Wed, 08 Jan 2025 18:23:13 GMT  
		Size: 31.9 MB (31896574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd30bbc7a30aecea7ad4e5f034902fbe2aea4b830d50751110bf328769b935d`  
		Last Modified: Wed, 08 Jan 2025 18:23:13 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f715b47c3e106a8a84813784dd5a6789a75cf4f1a2b83348b02dddae9efe6cd5`  
		Last Modified: Wed, 08 Jan 2025 18:23:13 GMT  
		Size: 965.6 KB (965645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db0149e0574a30416bd1757e8aa3fa032d928877beb21c19e749444aef6f6c4`  
		Last Modified: Wed, 08 Jan 2025 18:23:13 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afbc72cb26a761175852095f9aa309ccc07b9fa82ed03ddca84e352eb95eec8`  
		Last Modified: Wed, 08 Jan 2025 18:23:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:9d3e14b7d9b12b6593806213c69f200adb4eb03853681321f6a129b4917a7f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94fce35936248103dff28c70c7980eb4751a8a0d2137edda229bf8153dd787b9`

```dockerfile
```

-	Layers:
	-	`sha256:bccd273f9b6cb004932051c1a84a4c3b9c7085addbebadb6b0509df3ccbaf03b`  
		Last Modified: Wed, 08 Jan 2025 18:23:13 GMT  
		Size: 2.2 MB (2159247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5c182f2e98dc5d74159bb452b1e911f95f67e01096d4e4db9f66fac94095d3e`  
		Last Modified: Wed, 08 Jan 2025 18:23:13 GMT  
		Size: 31.0 KB (30958 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v6

```console
$ docker pull composer@sha256:33037a2771fa573b556f6f6f9b34a624d607f2e5ad17400931d72e522e7e0b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70883858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2742f0de5a004bc434bb7a5cdeeff99f5cb1e8cc1657ac03bdd12766e61d221b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:8bfbe143528e86684282cbfd298570a16342fbf7feefa882f4ff4af7f9116796`  
		Last Modified: Tue, 07 Jan 2025 18:31:35 GMT  
		Size: 30.6 MB (30640654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a227f011e7035c2e61babbdbf90fea0a1845e1422312eda1608ae428cda1dead`  
		Last Modified: Tue, 07 Jan 2025 18:31:34 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb4d70fa8e2e9e943104bb6ab3e28f71390a553840cdba5cbd7d8b618fa243b`  
		Last Modified: Tue, 07 Jan 2025 18:32:59 GMT  
		Size: 965.3 KB (965306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3826a6b574a6d595615f31b1ef9fae34a30dd1e418f79cee3bc7ab6a295e46ee`  
		Last Modified: Thu, 12 Dec 2024 19:28:04 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a40b7b2051e2d3ecb4c9cc96ce48f3cf1110f183d98c8e8df9222924c2c99b`  
		Last Modified: Tue, 07 Jan 2025 18:32:58 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:2f1c770454c1f9a39dc50afb470a9b303fbe20cec59ff4f1ea52a5865418d5c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180abf7fdf1d40f88a8ff64fb696c6dc3fe366f009e811e2a5fb3a979399e388`

```dockerfile
```

-	Layers:
	-	`sha256:cb72041883c9070c4153b3ab41d1755dcab7079e741903798832e7f29382bdb3`  
		Last Modified: Tue, 07 Jan 2025 18:32:58 GMT  
		Size: 30.8 KB (30844 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v7

```console
$ docker pull composer@sha256:594f53ed686765023ab6d53e4af003b79d54804802b89d575f23947c8360d70f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68909642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa3aff9d167a0aafd70dbccf29d249d860926dda0e4dc2f690134b0481ffebf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:0a2bf4fd23a4343e4fa39d2a63004ae4de297973415bc8809c9c56b1097caf8a`  
		Last Modified: Tue, 07 Jan 2025 18:37:42 GMT  
		Size: 30.2 MB (30150038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89da730f1c4439581b1de7342d8be357e2ea326296a6c567ba8c4e6dad0fd87e`  
		Last Modified: Tue, 07 Jan 2025 18:37:41 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6a1bad3eb85e0825e2a02155cda0ee2fe950d9e630efe3af93ce9a7886e632`  
		Last Modified: Tue, 07 Jan 2025 18:39:18 GMT  
		Size: 956.5 KB (956472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de4418b34011a326f53b6ef2ec2a18d2d74182277c0113bf6ddfb50428af1cc`  
		Last Modified: Tue, 07 Jan 2025 18:39:18 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4faa8b49ea62821ab26a87a3077ae98e271392d81fb83435adb091d96b34cff`  
		Last Modified: Tue, 07 Jan 2025 18:39:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:68947fc357f316533e66560925f64ac5c9bb0afd25a3aa7476e5f1ab0906c76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2184753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b0c05709ce6b958c6e8499802fc327c393298d2aaccbf1e9c73d062398ea6c`

```dockerfile
```

-	Layers:
	-	`sha256:8b8b8d795164c1e481dd469dee447f8c307553b607c9172fb3b7152cc5faac97`  
		Last Modified: Tue, 07 Jan 2025 18:39:18 GMT  
		Size: 2.2 MB (2153693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1807ecf10b7f0743c949836b691547a273d14ce37eca27b9bedc46ef878adfb9`  
		Last Modified: Tue, 07 Jan 2025 18:39:17 GMT  
		Size: 31.1 KB (31060 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:df5c4f311d7e77e252ad95f8f7ea66b3aa98394396e14cc9c7ea3ebb5b792b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74306091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7234ed006eb005ba5fba955cd5fba1a60de1a7af6badef61aa432ed5e52d0fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:a0c59331d5588d1a35cef8b8de8c57f9df896f2230d66caa4f7510c076bcf10b`  
		Last Modified: Tue, 07 Jan 2025 16:07:22 GMT  
		Size: 32.0 MB (32004107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bc1dca7afc6e7b778ae0cc6c16db02fce566edf2e75b273bdf7c721ed764f9`  
		Last Modified: Tue, 07 Jan 2025 16:07:20 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b939a8afce976fe45002973da6930697f18eae7fa27e8ce49dd2c17f65d1e5`  
		Last Modified: Tue, 07 Jan 2025 16:08:40 GMT  
		Size: 965.5 KB (965463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d8fee934fea50432c31925b35c4f56fde5213f691658f7dadc905edb60c69b`  
		Last Modified: Tue, 07 Jan 2025 16:08:40 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bdaaa2c66e9b7e2e40087cc900107f729d95917438796593acc5d49d16a25b`  
		Last Modified: Tue, 07 Jan 2025 16:08:40 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:5b3109cf34a8a6a9015cd8e20d5b60c4266fb5e5472d93092d79a788e22a1660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2184613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69df30c47d82fc2af4aba3ceca927f09a66f7144746a1ef19ab80acf5aa9f172`

```dockerfile
```

-	Layers:
	-	`sha256:cc0b071dfc1da5169488f1763875f769e28e8e5d06cba6d51427f582356b8d82`  
		Last Modified: Tue, 07 Jan 2025 16:08:40 GMT  
		Size: 2.2 MB (2153521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3593f9cd7e2f2a95a36b9cc0e63c452c488712bf7dc7f1a117dd35912fb9b537`  
		Last Modified: Tue, 07 Jan 2025 16:08:40 GMT  
		Size: 31.1 KB (31092 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; 386

```console
$ docker pull composer@sha256:c31ead984e1ee2d8efec17df384d63f4e1c5d854b428c40c215228a5ece6636b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54202544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a87b5519f7dbb8909d8ada69772bedef00855c1778fdb78caa889240def67d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:9057d2e3075e68379daa14741eee46f10348413e4debd93c3164c6d9281ff2ce`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 11.4 MB (11421295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9c3281d500418c6584ec3d0940fad88e375e39cbcb6f7b1f1f1605654ff468`  
		Last Modified: Wed, 08 Jan 2025 18:23:08 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7282b8d7cb806abb76d8b38dcb1f442799b33e340ddb3fb87aa3c65fe781f850`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 940.9 KB (940882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5cba85e675197ad1c4e50d53e4e0729a14dc95038bda054e5abd51eb1af7f2`  
		Last Modified: Wed, 08 Jan 2025 18:23:08 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f05948628ca40470c501b71b53616ed24606f1134506db08b96b27478c89d57`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:b3f96e58c405edfc5b23834bcd9683db84046ee1fa81b8d46f155e9fed60f03a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.8 KB (459822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1529a78ef0f77904d171c12f07aa6b11918c33f3b928126ca142a4367ec504ed`

```dockerfile
```

-	Layers:
	-	`sha256:c9238aa73cb4939daf0b36f8780096b38dffd6ec4dc7652dfc9f0af2bde3c4af`  
		Last Modified: Wed, 08 Jan 2025 18:23:08 GMT  
		Size: 428.9 KB (428900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c908b98f3fbcad032d5c687df01d8b71bdca05c3d5d9ede3de79959a5952e43`  
		Last Modified: Wed, 08 Jan 2025 18:23:08 GMT  
		Size: 30.9 KB (30922 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; ppc64le

```console
$ docker pull composer@sha256:97d2f5c73782a176aa8eeb4a6fb89685e3a6d796f569677b6f72f969cf9934f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76363875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf75369f387c182b0ae224de9bda281b6a897383b3ab57c201fcc90604499a3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:26aa0c6396d98d67cdb7cff725afeddc08a54386e1d5e68f922a402f902d2924`  
		Last Modified: Thu, 09 Jan 2025 01:29:00 GMT  
		Size: 32.9 MB (32943089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ed0b4e6953a4bbe30d89c2f6151304b7cf0496993f171b508a19e501ebb706`  
		Last Modified: Thu, 09 Jan 2025 01:28:58 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44629d85a30e074812821013cc532460d1a718009c13171f14849c0d657818a4`  
		Last Modified: Thu, 09 Jan 2025 01:30:41 GMT  
		Size: 972.2 KB (972200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae0870d155edbd5d8f44620e8fd1417a0014da3dfe8abbbbca1c3d61219eb81`  
		Last Modified: Thu, 09 Jan 2025 01:30:41 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02e4c72de67abe0992326a86fdd96d036c896006eefc4ebc2e4c8e8d2585b5c`  
		Last Modified: Thu, 09 Jan 2025 01:30:41 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:fa6b1fc46b576c78c7a115d62747e15d639dbd1203fe43c6bc77acf5aa1a232b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a72a373632f2591e90cab7db68d37ee6482a4c2edb1d976f21cf62c54c5e1c`

```dockerfile
```

-	Layers:
	-	`sha256:efae3b02ff4c673696f9f89debaabbaab703435f95f36e7e6c432283c9def1b9`  
		Last Modified: Thu, 09 Jan 2025 01:30:41 GMT  
		Size: 2.2 MB (2157810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b48f891f351b49b85f862d539710519a715d6ec7d72820a70c1457ed976bf76c`  
		Last Modified: Thu, 09 Jan 2025 01:30:41 GMT  
		Size: 31.0 KB (31006 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; riscv64

```console
$ docker pull composer@sha256:3e462cf88e80da773ee73a33af30f6d3d26181850646602bdd129b9e6b83e354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73723546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574b603af8bd97b8da7d159df81aadf76084e5f3c79ea67b42293b551a37a8e9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
		Size: 3.4 MB (3445761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9c93fa8ac38e6017fe5251627d738084239fbab425319ead8bdece897e493`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe2d3ee20829a994ce6548409e985a58c1c6ec2238583410057ae0e6dfe95a1`  
		Last Modified: Fri, 20 Dec 2024 22:27:49 GMT  
		Size: 13.6 MB (13580504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a67918c3771135e7a2b16f42498ea94d985dc8f6407db3a3ee60e1e3e9373b`  
		Last Modified: Fri, 20 Dec 2024 22:27:47 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e567d61ea86fdc5c63b8ce75eb88bcda35c75049600dcb0b112964a7da3ac42f`  
		Last Modified: Fri, 20 Dec 2024 22:27:50 GMT  
		Size: 20.8 MB (20797397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263bcc5a009f020e39d0e162f139f8f8433852481d7368c9cde637ffd9f841e5`  
		Last Modified: Fri, 20 Dec 2024 22:27:47 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9ec8a613ce316b270ee3a65ed2d2041d6579061f1f8b0d0725f55b6f9e84fc`  
		Last Modified: Fri, 20 Dec 2024 22:27:48 GMT  
		Size: 19.9 KB (19885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe21f96e7307414693b828f2173bcaa37df5cd8443ce028ad761b4e69270f7`  
		Last Modified: Sat, 21 Dec 2024 14:35:27 GMT  
		Size: 31.0 MB (31000197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4008aa8424d8743580595dbf0803a9aa275eb20020eb2e8e47ed5c19aeeee6bf`  
		Last Modified: Sat, 21 Dec 2024 14:35:22 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5e822a66d5151001774d542d9094b01daf100ed2157872f9877d906d3c58a9`  
		Last Modified: Sat, 21 Dec 2024 14:45:40 GMT  
		Size: 1.5 MB (1520901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d77b818da6a47633d65ab0ff8e7daaed7befa104f5c9fa09f8e82e8de6c9d7`  
		Last Modified: Sat, 21 Dec 2024 14:45:40 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9571248a3d79f630c65eb387c628804b009f25caf903c98b8310385c46a5a5bd`  
		Last Modified: Sat, 21 Dec 2024 14:45:40 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:74b44e5f1a6c0f35773105a798bc63b173bf7cb75c4af4fff3ed81bacc21ff2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50e5ce06ed6611b3c5d9bdf45873ac77f16e159372983bec4c7a1b140cc719b`

```dockerfile
```

-	Layers:
	-	`sha256:398b33f39dac14afa5780baf352eea65f1df765dec833491135a12f9ba4832c3`  
		Last Modified: Sat, 21 Dec 2024 14:45:40 GMT  
		Size: 2.2 MB (2158052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4e925469f2c58d80e4fb70d7fbe2424ee1f9a79db882fb4c3076c60ee921b42`  
		Last Modified: Sat, 21 Dec 2024 14:45:39 GMT  
		Size: 31.0 KB (31009 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; s390x

```console
$ docker pull composer@sha256:08f3eeed2a12f83f65d960fac5be4e0480c8734b7238bf20cf349178db442c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74620254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3785283d6b78dee3e29f5436fad47897fe6bbbf6ceefda0279058cc184d8e1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:3f63ed19a544e5e26e1152afe55e1e34f250a8fe3982b62ef0754513377c899c`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 31.7 MB (31674581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59aadc194319e2220294cf3ff3a08addb3a57ecf676d4fb858a0ff81e0bd6c8d`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b198938ddcda767ec453fd4c4438c1abaf40aedd368a78f6db8d56a6bd554a0`  
		Last Modified: Tue, 07 Jan 2025 15:53:31 GMT  
		Size: 968.3 KB (968314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0861e10c690483650a5c5b80a34f8062cf1c4991e5345d85cd0d17d56bb1ff`  
		Last Modified: Tue, 07 Jan 2025 15:53:31 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af048d98bf3c8a90c18d2c3115fa12f26188777034752c35b1c625281aa269c`  
		Last Modified: Tue, 07 Jan 2025 15:53:31 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:05f1fd51a10262cb513a2306d8841324bbae54348258bc3f43dc9b5b74169b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2181612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db7690f86ec1f52b5f920e134a8d3e09182d744d83472f8a9b493fe2b6b199b`

```dockerfile
```

-	Layers:
	-	`sha256:c5501f10e797650932c9d815eb6f1a7b7f7dd5eb6ccf761df1bdcb2feca404f7`  
		Last Modified: Tue, 07 Jan 2025 15:53:31 GMT  
		Size: 2.2 MB (2150654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a21f1b92bdd5f3c0b884d4d21f5cd59fe82cc515164be3abafa0e6508e82ae3`  
		Last Modified: Tue, 07 Jan 2025 15:53:30 GMT  
		Size: 31.0 KB (30958 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2`

```console
$ docker pull composer@sha256:2f5608ca4dea71332fc362322d8fd9faf8af679f884cd8c0809b57e783bb55fb
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

### `composer:2.2` - linux; amd64

```console
$ docker pull composer@sha256:d89f1b39885bc5fd7230772d2ba753b001ef77858206d86fe7653a5680d977d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74179967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064c853712449649329197128dea85b249dbfa8e337bdc0f28f7a46a70915f3c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
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
	-	`sha256:885cabab622328790c1b0fe029609594a60d1dde6f69dcb4cea95adfd92d8126`  
		Last Modified: Wed, 08 Jan 2025 18:23:12 GMT  
		Size: 31.9 MB (31896321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414b7b71fdb41abcb4ae1fc4672f9a1c2e0378ffde03fd52bb6bab21e8fc0792`  
		Last Modified: Wed, 08 Jan 2025 18:23:11 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c787e639b4347e933e17af93685e9678f55ff58887a31392ccd4a7b6c4a04fd`  
		Last Modified: Wed, 08 Jan 2025 18:23:12 GMT  
		Size: 819.6 KB (819649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5cba85e675197ad1c4e50d53e4e0729a14dc95038bda054e5abd51eb1af7f2`  
		Last Modified: Wed, 08 Jan 2025 18:23:08 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f05948628ca40470c501b71b53616ed24606f1134506db08b96b27478c89d57`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:e45b9734520af4d27ebe5f162005179af56ea71821d5ec27960ba2d08c1e90c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb109ab9b1f9daa010442645eef215da3ca8046f484ec0f4c357aa364ee6301`

```dockerfile
```

-	Layers:
	-	`sha256:70d3ef1a5d9e813dea628ac0de8bccdbd4c7beaaf5646fbbfcc90e33ffe4a213`  
		Last Modified: Wed, 08 Jan 2025 18:23:12 GMT  
		Size: 2.2 MB (2158953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e154f1263271bc00c1114370b3fea24edcdfb2143040971529c027ea928cde8f`  
		Last Modified: Wed, 08 Jan 2025 18:23:11 GMT  
		Size: 30.7 KB (30654 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v6

```console
$ docker pull composer@sha256:62780dfe0305b97d5c117da225f07089b5f049f9e28e63e77dace73ce3be1059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70737552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5123431ad90ce368101720cec24a22a396bc0b32e9dad29788f08e0848902788`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
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
	-	`sha256:8bfbe143528e86684282cbfd298570a16342fbf7feefa882f4ff4af7f9116796`  
		Last Modified: Tue, 07 Jan 2025 18:31:35 GMT  
		Size: 30.6 MB (30640654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a227f011e7035c2e61babbdbf90fea0a1845e1422312eda1608ae428cda1dead`  
		Last Modified: Tue, 07 Jan 2025 18:31:34 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a7f50a6a0b2d3bba683179b2ca8b3a6f06bfd4c4cd4cf9d7d8019fa8fdc3ed`  
		Last Modified: Tue, 07 Jan 2025 18:31:34 GMT  
		Size: 819.0 KB (819000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386d76b9a3e1f7c21e5a182c9d58502bc43af53578e67a16921add85659a9209`  
		Last Modified: Thu, 12 Dec 2024 19:27:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ff64dd899232449206800cffdc8869754b2909076233d33db06ddad1cdf3ab`  
		Last Modified: Tue, 07 Jan 2025 18:31:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:aca531ab11f0ec9cd82cb1561c71c8fd21045677fc332e31a991ebb62624fbb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84182bcd4d0972d594520d297fcd46e7f9820bc7b675b07ec118cd18508497c3`

```dockerfile
```

-	Layers:
	-	`sha256:7c740e78fe3d45b7ccc1292fa27e081e2817856eec1830607b76f5dd8f647675`  
		Last Modified: Tue, 07 Jan 2025 18:31:34 GMT  
		Size: 30.5 KB (30533 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v7

```console
$ docker pull composer@sha256:fe2e86e7783ca0794c0e26052f87bea5460a351e4a0a71f6c97dc848bab0f1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68763325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f539003ccc43375331a561f2fbddb2a1c4347d8a4e39b08b7e306c26e9374198`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
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
	-	`sha256:0a2bf4fd23a4343e4fa39d2a63004ae4de297973415bc8809c9c56b1097caf8a`  
		Last Modified: Tue, 07 Jan 2025 18:37:42 GMT  
		Size: 30.2 MB (30150038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89da730f1c4439581b1de7342d8be357e2ea326296a6c567ba8c4e6dad0fd87e`  
		Last Modified: Tue, 07 Jan 2025 18:37:41 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2866b818ce1acc063a90c52ca34e07472abd17b06d97f5cb4c3b576311e570d`  
		Last Modified: Tue, 07 Jan 2025 18:37:41 GMT  
		Size: 810.2 KB (810155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337e1d50532e32becc0231c4249de3f6ef29b28253de129ee5a78b1a3fc79e81`  
		Last Modified: Tue, 07 Jan 2025 18:37:41 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee87b2232654b3eb1c36caa684f8ccff56b1e37b1330e3f3c15eaa721a6e05f`  
		Last Modified: Tue, 07 Jan 2025 18:37:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:21398388870c6e26950eafb43b83ba774b8b8576a75dfaf38e50299d51adeb55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2184139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf47be48517aeedaf551be239ec81ba466518ad613e69ee63afb0609f455f15e`

```dockerfile
```

-	Layers:
	-	`sha256:517cce97251c609db3e3991630f2a5bc39f4422390d90007aea3d5ed3ad5fec6`  
		Last Modified: Tue, 07 Jan 2025 18:37:41 GMT  
		Size: 2.2 MB (2153391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10cd029e98742e609faaefa58d1cc5b64bc0ad33f0885eef827514a44f223b6a`  
		Last Modified: Tue, 07 Jan 2025 18:37:40 GMT  
		Size: 30.7 KB (30748 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:c54955436e867221e15e7b0b6889f5ad546095abfc856d42fc9ea083c93f4902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74159791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eeca8fe0441bd3d71568d6b9999e2f1547544b1965debcddb86d0e4c5ec555d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
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
	-	`sha256:a0c59331d5588d1a35cef8b8de8c57f9df896f2230d66caa4f7510c076bcf10b`  
		Last Modified: Tue, 07 Jan 2025 16:07:22 GMT  
		Size: 32.0 MB (32004107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bc1dca7afc6e7b778ae0cc6c16db02fce566edf2e75b273bdf7c721ed764f9`  
		Last Modified: Tue, 07 Jan 2025 16:07:20 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22f76f0fb079af01086f273a0c5a2c90c6164c8dbc6e94f26d29d86d625562a`  
		Last Modified: Tue, 07 Jan 2025 16:07:20 GMT  
		Size: 819.2 KB (819160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57850e2434c721ad60730949863bf3ad1b08b34367f7a9fdb22370cf20bdd38e`  
		Last Modified: Tue, 07 Jan 2025 16:07:20 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c75b7341e5165a5268e0c27fa486773dd4d578f8919cfa4c33ee9c14d9497c8`  
		Last Modified: Tue, 07 Jan 2025 16:07:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:f8584b8f4d9369dc4f295402f8bda2017d3d8ab6343c5e4c15fa5f4f08a4e026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2183990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e713c1a2820caba98c9259e6a458d567f77191e4c6f01048a3990b203ea3f25a`

```dockerfile
```

-	Layers:
	-	`sha256:970567e858d48b4a4723956c594efaf4f894e54a2b7405a843923594a74cb803`  
		Last Modified: Tue, 07 Jan 2025 16:07:20 GMT  
		Size: 2.2 MB (2153215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c32f616e654e513df779676341c65f0f8ac0b9e2d8294c69943a2bac10c00ec1`  
		Last Modified: Tue, 07 Jan 2025 16:07:20 GMT  
		Size: 30.8 KB (30775 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; 386

```console
$ docker pull composer@sha256:d867c413160a359efb52c69460a4144a03ed8da734699116540299d612e7d018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54060154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af7e0c10eb7fb91b52fac4ece18f3eb62e4fa7689fed39c9599452fa129c511`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
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
	-	`sha256:8fbd829e35763ceb6dccaeefd114a90e3d353e0f2279bccdbc61d7043db2f3e0`  
		Last Modified: Wed, 08 Jan 2025 18:23:10 GMT  
		Size: 11.4 MB (11421298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7325392e6f571d6d6c867ba9360a98dcc25489b73ee76ef7f4cc6be5d7ec8b54`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a0ea9fde932ff4d6706282639ee6dcdc1ae58fb69c70f200d3eee65b8b57de`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 798.5 KB (798487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7ec707154224ea90d37a709253436de0e37251a0637392c70bf27f2cb93575`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f05948628ca40470c501b71b53616ed24606f1134506db08b96b27478c89d57`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:823a8609ebdc375e23fb68610b629e4d12c9313888f35a65ff975e30357de379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.2 KB (459234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d52cd67e2526878d1fcb3f39879549b565d84f150023a1c5a1bd68b5d13895e`

```dockerfile
```

-	Layers:
	-	`sha256:82ddaf0eaae76863fc7e561ba10ace7088adc1d9708f67a614019ef59ed65e5e`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 428.6 KB (428611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a65dfea9228e3d77283a647e8033aacefe3c50b6e536857822aa4f78535aef91`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 30.6 KB (30623 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; ppc64le

```console
$ docker pull composer@sha256:c681ce6660052c5b5706c1ce94de91ea805ffbf6198a9ba4320ef50e6207ee1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76217995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da8839e93bd725eaa611e5287b8bd89ee9893ad4d64f8d23856437c058fb27b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
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
	-	`sha256:26aa0c6396d98d67cdb7cff725afeddc08a54386e1d5e68f922a402f902d2924`  
		Last Modified: Thu, 09 Jan 2025 01:29:00 GMT  
		Size: 32.9 MB (32943089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ed0b4e6953a4bbe30d89c2f6151304b7cf0496993f171b508a19e501ebb706`  
		Last Modified: Thu, 09 Jan 2025 01:28:58 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aecade86a1d865576697d59d99d03142a53200eb9c65045733a02e9b371744a`  
		Last Modified: Thu, 09 Jan 2025 01:28:59 GMT  
		Size: 826.3 KB (826320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067fa511713f9b64b2eac2a775759f1e7b8a632164010b713826377a5acfdf6d`  
		Last Modified: Thu, 09 Jan 2025 01:28:58 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77067613a67569ad413a6087f23c33cefaa8aa92e74697b79800bc235fdf47ee`  
		Last Modified: Thu, 09 Jan 2025 01:28:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:a71bca1eab6c6d29e8714a2d1acc82c79ba777a3230a2f23b64b5c624c0ddb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b08a6c05ed8f0e3db87d40776586c32e466c4025c5f194ebd53603ad5de5cd`

```dockerfile
```

-	Layers:
	-	`sha256:a1e946c2ab4d20f8dc014e4a54b3a6e9a94a86970d63c6b3775d03e328ed6da7`  
		Last Modified: Thu, 09 Jan 2025 01:28:58 GMT  
		Size: 2.2 MB (2157510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e080193b6d487618c1b09ea228820916ecde56ee3afde851edf6def943baa7d`  
		Last Modified: Thu, 09 Jan 2025 01:28:58 GMT  
		Size: 30.7 KB (30696 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; riscv64

```console
$ docker pull composer@sha256:5d855d116a11db35f6a8ad2be607bd8e5624eeb94475fe41679a24f4c4ffb032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73581176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebda7e74b0a3215d8eff4cfa7e70191f9eb54e0c56c6fffe7736ce1a76bff18`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
		Size: 3.4 MB (3445761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9c93fa8ac38e6017fe5251627d738084239fbab425319ead8bdece897e493`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe2d3ee20829a994ce6548409e985a58c1c6ec2238583410057ae0e6dfe95a1`  
		Last Modified: Fri, 20 Dec 2024 22:27:49 GMT  
		Size: 13.6 MB (13580504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a67918c3771135e7a2b16f42498ea94d985dc8f6407db3a3ee60e1e3e9373b`  
		Last Modified: Fri, 20 Dec 2024 22:27:47 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e567d61ea86fdc5c63b8ce75eb88bcda35c75049600dcb0b112964a7da3ac42f`  
		Last Modified: Fri, 20 Dec 2024 22:27:50 GMT  
		Size: 20.8 MB (20797397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263bcc5a009f020e39d0e162f139f8f8433852481d7368c9cde637ffd9f841e5`  
		Last Modified: Fri, 20 Dec 2024 22:27:47 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9ec8a613ce316b270ee3a65ed2d2041d6579061f1f8b0d0725f55b6f9e84fc`  
		Last Modified: Fri, 20 Dec 2024 22:27:48 GMT  
		Size: 19.9 KB (19885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe21f96e7307414693b828f2173bcaa37df5cd8443ce028ad761b4e69270f7`  
		Last Modified: Sat, 21 Dec 2024 14:35:27 GMT  
		Size: 31.0 MB (31000197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4008aa8424d8743580595dbf0803a9aa275eb20020eb2e8e47ed5c19aeeee6bf`  
		Last Modified: Sat, 21 Dec 2024 14:35:22 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57af59a23156600be33dba882bdf1a5e0021aa8a1a596a9177787f956d9b64a`  
		Last Modified: Sat, 21 Dec 2024 14:35:22 GMT  
		Size: 1.4 MB (1378532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081edbee53f3a9cf4b66b37a4a382dd412be359ae83d996f3486c00c340e622a`  
		Last Modified: Sat, 21 Dec 2024 14:35:22 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e210a352cd82457991648bd5510e28668c55ff115eda1b4507fe4a714e7923f0`  
		Last Modified: Sat, 21 Dec 2024 14:35:23 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:a2c7dca9aa5fcbd3871b7007b05cf47f7f2d2b368637d8b079f0f646f5bfd5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c674cd3c5293d3d1f3dd5b6b93134ecbce04724ce045e1deed00622bf30caee`

```dockerfile
```

-	Layers:
	-	`sha256:242ae2fc62a46e8658c8d4da70cdfd90b2baddb6395de29095bf372fb27560a9`  
		Last Modified: Sat, 21 Dec 2024 14:35:22 GMT  
		Size: 2.2 MB (2157752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec0097a6dfb339beb94a49db7f8925afc8a4499c4aa2a06fb1902165559b3486`  
		Last Modified: Sat, 21 Dec 2024 14:35:21 GMT  
		Size: 30.7 KB (30699 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; s390x

```console
$ docker pull composer@sha256:d02c93f2bed1ac62f9a10175194a7d1c3ff57a7ab1da35b5d838c9ce8f57dc8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74474247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9396e94046532c68a1e2079f216151ef6b76b0c87971d41b90a863dcf11e38`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
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
	-	`sha256:3f63ed19a544e5e26e1152afe55e1e34f250a8fe3982b62ef0754513377c899c`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 31.7 MB (31674581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59aadc194319e2220294cf3ff3a08addb3a57ecf676d4fb858a0ff81e0bd6c8d`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeeba213ea4c8637e0fc7148dff1096de416af696a8f3d82c2d9a49ce3c7cc28`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 822.3 KB (822308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7854c8ea0ad3ff17f9fe195d3544e9cbd21ff3acba3640292dfe831f78d84`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b983b49b572dbb392ac1688ac9013e00106127d063358984a7bb4cbfa8b94f`  
		Last Modified: Tue, 07 Jan 2025 15:51:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:6200dcf316dc362bab148966c3916a70a89158c498ad90838c65184d3c53df57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2181014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39799757773592a16da8bcbdb6995319725643d812b9d58541e8f5b510740554`

```dockerfile
```

-	Layers:
	-	`sha256:7a722c2780e1984cf94a58e3060e8f419a5e9faca1e4ba334aee11586a18bcaf`  
		Last Modified: Tue, 07 Jan 2025 15:51:40 GMT  
		Size: 2.2 MB (2150360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee0ca95466511e3dc9b15d260a86ebe0dc6036ed10cdb8212e7ac94f0614e79`  
		Last Modified: Tue, 07 Jan 2025 15:51:40 GMT  
		Size: 30.7 KB (30654 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2.25`

```console
$ docker pull composer@sha256:2f5608ca4dea71332fc362322d8fd9faf8af679f884cd8c0809b57e783bb55fb
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

### `composer:2.2.25` - linux; amd64

```console
$ docker pull composer@sha256:d89f1b39885bc5fd7230772d2ba753b001ef77858206d86fe7653a5680d977d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74179967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064c853712449649329197128dea85b249dbfa8e337bdc0f28f7a46a70915f3c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
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
	-	`sha256:885cabab622328790c1b0fe029609594a60d1dde6f69dcb4cea95adfd92d8126`  
		Last Modified: Wed, 08 Jan 2025 18:23:12 GMT  
		Size: 31.9 MB (31896321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414b7b71fdb41abcb4ae1fc4672f9a1c2e0378ffde03fd52bb6bab21e8fc0792`  
		Last Modified: Wed, 08 Jan 2025 18:23:11 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c787e639b4347e933e17af93685e9678f55ff58887a31392ccd4a7b6c4a04fd`  
		Last Modified: Wed, 08 Jan 2025 18:23:12 GMT  
		Size: 819.6 KB (819649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5cba85e675197ad1c4e50d53e4e0729a14dc95038bda054e5abd51eb1af7f2`  
		Last Modified: Wed, 08 Jan 2025 18:23:08 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f05948628ca40470c501b71b53616ed24606f1134506db08b96b27478c89d57`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:e45b9734520af4d27ebe5f162005179af56ea71821d5ec27960ba2d08c1e90c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb109ab9b1f9daa010442645eef215da3ca8046f484ec0f4c357aa364ee6301`

```dockerfile
```

-	Layers:
	-	`sha256:70d3ef1a5d9e813dea628ac0de8bccdbd4c7beaaf5646fbbfcc90e33ffe4a213`  
		Last Modified: Wed, 08 Jan 2025 18:23:12 GMT  
		Size: 2.2 MB (2158953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e154f1263271bc00c1114370b3fea24edcdfb2143040971529c027ea928cde8f`  
		Last Modified: Wed, 08 Jan 2025 18:23:11 GMT  
		Size: 30.7 KB (30654 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm variant v6

```console
$ docker pull composer@sha256:62780dfe0305b97d5c117da225f07089b5f049f9e28e63e77dace73ce3be1059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70737552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5123431ad90ce368101720cec24a22a396bc0b32e9dad29788f08e0848902788`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
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
	-	`sha256:8bfbe143528e86684282cbfd298570a16342fbf7feefa882f4ff4af7f9116796`  
		Last Modified: Tue, 07 Jan 2025 18:31:35 GMT  
		Size: 30.6 MB (30640654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a227f011e7035c2e61babbdbf90fea0a1845e1422312eda1608ae428cda1dead`  
		Last Modified: Tue, 07 Jan 2025 18:31:34 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a7f50a6a0b2d3bba683179b2ca8b3a6f06bfd4c4cd4cf9d7d8019fa8fdc3ed`  
		Last Modified: Tue, 07 Jan 2025 18:31:34 GMT  
		Size: 819.0 KB (819000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386d76b9a3e1f7c21e5a182c9d58502bc43af53578e67a16921add85659a9209`  
		Last Modified: Thu, 12 Dec 2024 19:27:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ff64dd899232449206800cffdc8869754b2909076233d33db06ddad1cdf3ab`  
		Last Modified: Tue, 07 Jan 2025 18:31:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:aca531ab11f0ec9cd82cb1561c71c8fd21045677fc332e31a991ebb62624fbb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84182bcd4d0972d594520d297fcd46e7f9820bc7b675b07ec118cd18508497c3`

```dockerfile
```

-	Layers:
	-	`sha256:7c740e78fe3d45b7ccc1292fa27e081e2817856eec1830607b76f5dd8f647675`  
		Last Modified: Tue, 07 Jan 2025 18:31:34 GMT  
		Size: 30.5 KB (30533 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm variant v7

```console
$ docker pull composer@sha256:fe2e86e7783ca0794c0e26052f87bea5460a351e4a0a71f6c97dc848bab0f1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68763325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f539003ccc43375331a561f2fbddb2a1c4347d8a4e39b08b7e306c26e9374198`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
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
	-	`sha256:0a2bf4fd23a4343e4fa39d2a63004ae4de297973415bc8809c9c56b1097caf8a`  
		Last Modified: Tue, 07 Jan 2025 18:37:42 GMT  
		Size: 30.2 MB (30150038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89da730f1c4439581b1de7342d8be357e2ea326296a6c567ba8c4e6dad0fd87e`  
		Last Modified: Tue, 07 Jan 2025 18:37:41 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2866b818ce1acc063a90c52ca34e07472abd17b06d97f5cb4c3b576311e570d`  
		Last Modified: Tue, 07 Jan 2025 18:37:41 GMT  
		Size: 810.2 KB (810155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337e1d50532e32becc0231c4249de3f6ef29b28253de129ee5a78b1a3fc79e81`  
		Last Modified: Tue, 07 Jan 2025 18:37:41 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee87b2232654b3eb1c36caa684f8ccff56b1e37b1330e3f3c15eaa721a6e05f`  
		Last Modified: Tue, 07 Jan 2025 18:37:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:21398388870c6e26950eafb43b83ba774b8b8576a75dfaf38e50299d51adeb55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2184139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf47be48517aeedaf551be239ec81ba466518ad613e69ee63afb0609f455f15e`

```dockerfile
```

-	Layers:
	-	`sha256:517cce97251c609db3e3991630f2a5bc39f4422390d90007aea3d5ed3ad5fec6`  
		Last Modified: Tue, 07 Jan 2025 18:37:41 GMT  
		Size: 2.2 MB (2153391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10cd029e98742e609faaefa58d1cc5b64bc0ad33f0885eef827514a44f223b6a`  
		Last Modified: Tue, 07 Jan 2025 18:37:40 GMT  
		Size: 30.7 KB (30748 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:c54955436e867221e15e7b0b6889f5ad546095abfc856d42fc9ea083c93f4902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74159791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eeca8fe0441bd3d71568d6b9999e2f1547544b1965debcddb86d0e4c5ec555d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
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
	-	`sha256:a0c59331d5588d1a35cef8b8de8c57f9df896f2230d66caa4f7510c076bcf10b`  
		Last Modified: Tue, 07 Jan 2025 16:07:22 GMT  
		Size: 32.0 MB (32004107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bc1dca7afc6e7b778ae0cc6c16db02fce566edf2e75b273bdf7c721ed764f9`  
		Last Modified: Tue, 07 Jan 2025 16:07:20 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22f76f0fb079af01086f273a0c5a2c90c6164c8dbc6e94f26d29d86d625562a`  
		Last Modified: Tue, 07 Jan 2025 16:07:20 GMT  
		Size: 819.2 KB (819160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57850e2434c721ad60730949863bf3ad1b08b34367f7a9fdb22370cf20bdd38e`  
		Last Modified: Tue, 07 Jan 2025 16:07:20 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c75b7341e5165a5268e0c27fa486773dd4d578f8919cfa4c33ee9c14d9497c8`  
		Last Modified: Tue, 07 Jan 2025 16:07:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:f8584b8f4d9369dc4f295402f8bda2017d3d8ab6343c5e4c15fa5f4f08a4e026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2183990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e713c1a2820caba98c9259e6a458d567f77191e4c6f01048a3990b203ea3f25a`

```dockerfile
```

-	Layers:
	-	`sha256:970567e858d48b4a4723956c594efaf4f894e54a2b7405a843923594a74cb803`  
		Last Modified: Tue, 07 Jan 2025 16:07:20 GMT  
		Size: 2.2 MB (2153215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c32f616e654e513df779676341c65f0f8ac0b9e2d8294c69943a2bac10c00ec1`  
		Last Modified: Tue, 07 Jan 2025 16:07:20 GMT  
		Size: 30.8 KB (30775 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; 386

```console
$ docker pull composer@sha256:d867c413160a359efb52c69460a4144a03ed8da734699116540299d612e7d018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54060154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af7e0c10eb7fb91b52fac4ece18f3eb62e4fa7689fed39c9599452fa129c511`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
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
	-	`sha256:8fbd829e35763ceb6dccaeefd114a90e3d353e0f2279bccdbc61d7043db2f3e0`  
		Last Modified: Wed, 08 Jan 2025 18:23:10 GMT  
		Size: 11.4 MB (11421298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7325392e6f571d6d6c867ba9360a98dcc25489b73ee76ef7f4cc6be5d7ec8b54`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a0ea9fde932ff4d6706282639ee6dcdc1ae58fb69c70f200d3eee65b8b57de`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 798.5 KB (798487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7ec707154224ea90d37a709253436de0e37251a0637392c70bf27f2cb93575`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f05948628ca40470c501b71b53616ed24606f1134506db08b96b27478c89d57`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:823a8609ebdc375e23fb68610b629e4d12c9313888f35a65ff975e30357de379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.2 KB (459234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d52cd67e2526878d1fcb3f39879549b565d84f150023a1c5a1bd68b5d13895e`

```dockerfile
```

-	Layers:
	-	`sha256:82ddaf0eaae76863fc7e561ba10ace7088adc1d9708f67a614019ef59ed65e5e`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 428.6 KB (428611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a65dfea9228e3d77283a647e8033aacefe3c50b6e536857822aa4f78535aef91`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 30.6 KB (30623 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; ppc64le

```console
$ docker pull composer@sha256:c681ce6660052c5b5706c1ce94de91ea805ffbf6198a9ba4320ef50e6207ee1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76217995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da8839e93bd725eaa611e5287b8bd89ee9893ad4d64f8d23856437c058fb27b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
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
	-	`sha256:26aa0c6396d98d67cdb7cff725afeddc08a54386e1d5e68f922a402f902d2924`  
		Last Modified: Thu, 09 Jan 2025 01:29:00 GMT  
		Size: 32.9 MB (32943089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ed0b4e6953a4bbe30d89c2f6151304b7cf0496993f171b508a19e501ebb706`  
		Last Modified: Thu, 09 Jan 2025 01:28:58 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aecade86a1d865576697d59d99d03142a53200eb9c65045733a02e9b371744a`  
		Last Modified: Thu, 09 Jan 2025 01:28:59 GMT  
		Size: 826.3 KB (826320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067fa511713f9b64b2eac2a775759f1e7b8a632164010b713826377a5acfdf6d`  
		Last Modified: Thu, 09 Jan 2025 01:28:58 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77067613a67569ad413a6087f23c33cefaa8aa92e74697b79800bc235fdf47ee`  
		Last Modified: Thu, 09 Jan 2025 01:28:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:a71bca1eab6c6d29e8714a2d1acc82c79ba777a3230a2f23b64b5c624c0ddb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b08a6c05ed8f0e3db87d40776586c32e466c4025c5f194ebd53603ad5de5cd`

```dockerfile
```

-	Layers:
	-	`sha256:a1e946c2ab4d20f8dc014e4a54b3a6e9a94a86970d63c6b3775d03e328ed6da7`  
		Last Modified: Thu, 09 Jan 2025 01:28:58 GMT  
		Size: 2.2 MB (2157510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e080193b6d487618c1b09ea228820916ecde56ee3afde851edf6def943baa7d`  
		Last Modified: Thu, 09 Jan 2025 01:28:58 GMT  
		Size: 30.7 KB (30696 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; riscv64

```console
$ docker pull composer@sha256:5d855d116a11db35f6a8ad2be607bd8e5624eeb94475fe41679a24f4c4ffb032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73581176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebda7e74b0a3215d8eff4cfa7e70191f9eb54e0c56c6fffe7736ce1a76bff18`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
		Size: 3.4 MB (3445761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9c93fa8ac38e6017fe5251627d738084239fbab425319ead8bdece897e493`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe2d3ee20829a994ce6548409e985a58c1c6ec2238583410057ae0e6dfe95a1`  
		Last Modified: Fri, 20 Dec 2024 22:27:49 GMT  
		Size: 13.6 MB (13580504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a67918c3771135e7a2b16f42498ea94d985dc8f6407db3a3ee60e1e3e9373b`  
		Last Modified: Fri, 20 Dec 2024 22:27:47 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e567d61ea86fdc5c63b8ce75eb88bcda35c75049600dcb0b112964a7da3ac42f`  
		Last Modified: Fri, 20 Dec 2024 22:27:50 GMT  
		Size: 20.8 MB (20797397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263bcc5a009f020e39d0e162f139f8f8433852481d7368c9cde637ffd9f841e5`  
		Last Modified: Fri, 20 Dec 2024 22:27:47 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9ec8a613ce316b270ee3a65ed2d2041d6579061f1f8b0d0725f55b6f9e84fc`  
		Last Modified: Fri, 20 Dec 2024 22:27:48 GMT  
		Size: 19.9 KB (19885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe21f96e7307414693b828f2173bcaa37df5cd8443ce028ad761b4e69270f7`  
		Last Modified: Sat, 21 Dec 2024 14:35:27 GMT  
		Size: 31.0 MB (31000197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4008aa8424d8743580595dbf0803a9aa275eb20020eb2e8e47ed5c19aeeee6bf`  
		Last Modified: Sat, 21 Dec 2024 14:35:22 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57af59a23156600be33dba882bdf1a5e0021aa8a1a596a9177787f956d9b64a`  
		Last Modified: Sat, 21 Dec 2024 14:35:22 GMT  
		Size: 1.4 MB (1378532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081edbee53f3a9cf4b66b37a4a382dd412be359ae83d996f3486c00c340e622a`  
		Last Modified: Sat, 21 Dec 2024 14:35:22 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e210a352cd82457991648bd5510e28668c55ff115eda1b4507fe4a714e7923f0`  
		Last Modified: Sat, 21 Dec 2024 14:35:23 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:a2c7dca9aa5fcbd3871b7007b05cf47f7f2d2b368637d8b079f0f646f5bfd5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c674cd3c5293d3d1f3dd5b6b93134ecbce04724ce045e1deed00622bf30caee`

```dockerfile
```

-	Layers:
	-	`sha256:242ae2fc62a46e8658c8d4da70cdfd90b2baddb6395de29095bf372fb27560a9`  
		Last Modified: Sat, 21 Dec 2024 14:35:22 GMT  
		Size: 2.2 MB (2157752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec0097a6dfb339beb94a49db7f8925afc8a4499c4aa2a06fb1902165559b3486`  
		Last Modified: Sat, 21 Dec 2024 14:35:21 GMT  
		Size: 30.7 KB (30699 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; s390x

```console
$ docker pull composer@sha256:d02c93f2bed1ac62f9a10175194a7d1c3ff57a7ab1da35b5d838c9ce8f57dc8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74474247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9396e94046532c68a1e2079f216151ef6b76b0c87971d41b90a863dcf11e38`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
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
	-	`sha256:3f63ed19a544e5e26e1152afe55e1e34f250a8fe3982b62ef0754513377c899c`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 31.7 MB (31674581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59aadc194319e2220294cf3ff3a08addb3a57ecf676d4fb858a0ff81e0bd6c8d`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeeba213ea4c8637e0fc7148dff1096de416af696a8f3d82c2d9a49ce3c7cc28`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 822.3 KB (822308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7854c8ea0ad3ff17f9fe195d3544e9cbd21ff3acba3640292dfe831f78d84`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b983b49b572dbb392ac1688ac9013e00106127d063358984a7bb4cbfa8b94f`  
		Last Modified: Tue, 07 Jan 2025 15:51:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:6200dcf316dc362bab148966c3916a70a89158c498ad90838c65184d3c53df57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2181014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39799757773592a16da8bcbdb6995319725643d812b9d58541e8f5b510740554`

```dockerfile
```

-	Layers:
	-	`sha256:7a722c2780e1984cf94a58e3060e8f419a5e9faca1e4ba334aee11586a18bcaf`  
		Last Modified: Tue, 07 Jan 2025 15:51:40 GMT  
		Size: 2.2 MB (2150360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee0ca95466511e3dc9b15d260a86ebe0dc6036ed10cdb8212e7ac94f0614e79`  
		Last Modified: Tue, 07 Jan 2025 15:51:40 GMT  
		Size: 30.7 KB (30654 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8`

```console
$ docker pull composer@sha256:5343ca2d163000fc433898aba00818152bece4bf10d46745102378ace3964eed
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

### `composer:2.8` - linux; amd64

```console
$ docker pull composer@sha256:005298f3a8e453451ef3bf7b15bea492d29101a86bfa8407341d0b12038767ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74326216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53abc0a37f7ee2356900dd8be0983112aca615687e2fdcff5cd9232b69ca7b09`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:978a5b5b12769c41e9b5454d72092585972d47afc882215a4e67bfc88f493d5b`  
		Last Modified: Wed, 08 Jan 2025 18:23:13 GMT  
		Size: 31.9 MB (31896574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd30bbc7a30aecea7ad4e5f034902fbe2aea4b830d50751110bf328769b935d`  
		Last Modified: Wed, 08 Jan 2025 18:23:13 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f715b47c3e106a8a84813784dd5a6789a75cf4f1a2b83348b02dddae9efe6cd5`  
		Last Modified: Wed, 08 Jan 2025 18:23:13 GMT  
		Size: 965.6 KB (965645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db0149e0574a30416bd1757e8aa3fa032d928877beb21c19e749444aef6f6c4`  
		Last Modified: Wed, 08 Jan 2025 18:23:13 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afbc72cb26a761175852095f9aa309ccc07b9fa82ed03ddca84e352eb95eec8`  
		Last Modified: Wed, 08 Jan 2025 18:23:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:9d3e14b7d9b12b6593806213c69f200adb4eb03853681321f6a129b4917a7f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94fce35936248103dff28c70c7980eb4751a8a0d2137edda229bf8153dd787b9`

```dockerfile
```

-	Layers:
	-	`sha256:bccd273f9b6cb004932051c1a84a4c3b9c7085addbebadb6b0509df3ccbaf03b`  
		Last Modified: Wed, 08 Jan 2025 18:23:13 GMT  
		Size: 2.2 MB (2159247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5c182f2e98dc5d74159bb452b1e911f95f67e01096d4e4db9f66fac94095d3e`  
		Last Modified: Wed, 08 Jan 2025 18:23:13 GMT  
		Size: 31.0 KB (30958 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v6

```console
$ docker pull composer@sha256:33037a2771fa573b556f6f6f9b34a624d607f2e5ad17400931d72e522e7e0b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70883858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2742f0de5a004bc434bb7a5cdeeff99f5cb1e8cc1657ac03bdd12766e61d221b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:8bfbe143528e86684282cbfd298570a16342fbf7feefa882f4ff4af7f9116796`  
		Last Modified: Tue, 07 Jan 2025 18:31:35 GMT  
		Size: 30.6 MB (30640654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a227f011e7035c2e61babbdbf90fea0a1845e1422312eda1608ae428cda1dead`  
		Last Modified: Tue, 07 Jan 2025 18:31:34 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb4d70fa8e2e9e943104bb6ab3e28f71390a553840cdba5cbd7d8b618fa243b`  
		Last Modified: Tue, 07 Jan 2025 18:32:59 GMT  
		Size: 965.3 KB (965306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3826a6b574a6d595615f31b1ef9fae34a30dd1e418f79cee3bc7ab6a295e46ee`  
		Last Modified: Thu, 12 Dec 2024 19:28:04 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a40b7b2051e2d3ecb4c9cc96ce48f3cf1110f183d98c8e8df9222924c2c99b`  
		Last Modified: Tue, 07 Jan 2025 18:32:58 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:2f1c770454c1f9a39dc50afb470a9b303fbe20cec59ff4f1ea52a5865418d5c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180abf7fdf1d40f88a8ff64fb696c6dc3fe366f009e811e2a5fb3a979399e388`

```dockerfile
```

-	Layers:
	-	`sha256:cb72041883c9070c4153b3ab41d1755dcab7079e741903798832e7f29382bdb3`  
		Last Modified: Tue, 07 Jan 2025 18:32:58 GMT  
		Size: 30.8 KB (30844 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v7

```console
$ docker pull composer@sha256:594f53ed686765023ab6d53e4af003b79d54804802b89d575f23947c8360d70f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68909642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa3aff9d167a0aafd70dbccf29d249d860926dda0e4dc2f690134b0481ffebf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:0a2bf4fd23a4343e4fa39d2a63004ae4de297973415bc8809c9c56b1097caf8a`  
		Last Modified: Tue, 07 Jan 2025 18:37:42 GMT  
		Size: 30.2 MB (30150038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89da730f1c4439581b1de7342d8be357e2ea326296a6c567ba8c4e6dad0fd87e`  
		Last Modified: Tue, 07 Jan 2025 18:37:41 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6a1bad3eb85e0825e2a02155cda0ee2fe950d9e630efe3af93ce9a7886e632`  
		Last Modified: Tue, 07 Jan 2025 18:39:18 GMT  
		Size: 956.5 KB (956472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de4418b34011a326f53b6ef2ec2a18d2d74182277c0113bf6ddfb50428af1cc`  
		Last Modified: Tue, 07 Jan 2025 18:39:18 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4faa8b49ea62821ab26a87a3077ae98e271392d81fb83435adb091d96b34cff`  
		Last Modified: Tue, 07 Jan 2025 18:39:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:68947fc357f316533e66560925f64ac5c9bb0afd25a3aa7476e5f1ab0906c76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2184753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b0c05709ce6b958c6e8499802fc327c393298d2aaccbf1e9c73d062398ea6c`

```dockerfile
```

-	Layers:
	-	`sha256:8b8b8d795164c1e481dd469dee447f8c307553b607c9172fb3b7152cc5faac97`  
		Last Modified: Tue, 07 Jan 2025 18:39:18 GMT  
		Size: 2.2 MB (2153693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1807ecf10b7f0743c949836b691547a273d14ce37eca27b9bedc46ef878adfb9`  
		Last Modified: Tue, 07 Jan 2025 18:39:17 GMT  
		Size: 31.1 KB (31060 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:df5c4f311d7e77e252ad95f8f7ea66b3aa98394396e14cc9c7ea3ebb5b792b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74306091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7234ed006eb005ba5fba955cd5fba1a60de1a7af6badef61aa432ed5e52d0fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:a0c59331d5588d1a35cef8b8de8c57f9df896f2230d66caa4f7510c076bcf10b`  
		Last Modified: Tue, 07 Jan 2025 16:07:22 GMT  
		Size: 32.0 MB (32004107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bc1dca7afc6e7b778ae0cc6c16db02fce566edf2e75b273bdf7c721ed764f9`  
		Last Modified: Tue, 07 Jan 2025 16:07:20 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b939a8afce976fe45002973da6930697f18eae7fa27e8ce49dd2c17f65d1e5`  
		Last Modified: Tue, 07 Jan 2025 16:08:40 GMT  
		Size: 965.5 KB (965463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d8fee934fea50432c31925b35c4f56fde5213f691658f7dadc905edb60c69b`  
		Last Modified: Tue, 07 Jan 2025 16:08:40 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bdaaa2c66e9b7e2e40087cc900107f729d95917438796593acc5d49d16a25b`  
		Last Modified: Tue, 07 Jan 2025 16:08:40 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:5b3109cf34a8a6a9015cd8e20d5b60c4266fb5e5472d93092d79a788e22a1660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2184613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69df30c47d82fc2af4aba3ceca927f09a66f7144746a1ef19ab80acf5aa9f172`

```dockerfile
```

-	Layers:
	-	`sha256:cc0b071dfc1da5169488f1763875f769e28e8e5d06cba6d51427f582356b8d82`  
		Last Modified: Tue, 07 Jan 2025 16:08:40 GMT  
		Size: 2.2 MB (2153521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3593f9cd7e2f2a95a36b9cc0e63c452c488712bf7dc7f1a117dd35912fb9b537`  
		Last Modified: Tue, 07 Jan 2025 16:08:40 GMT  
		Size: 31.1 KB (31092 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; 386

```console
$ docker pull composer@sha256:c31ead984e1ee2d8efec17df384d63f4e1c5d854b428c40c215228a5ece6636b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54202544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a87b5519f7dbb8909d8ada69772bedef00855c1778fdb78caa889240def67d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:9057d2e3075e68379daa14741eee46f10348413e4debd93c3164c6d9281ff2ce`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 11.4 MB (11421295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9c3281d500418c6584ec3d0940fad88e375e39cbcb6f7b1f1f1605654ff468`  
		Last Modified: Wed, 08 Jan 2025 18:23:08 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7282b8d7cb806abb76d8b38dcb1f442799b33e340ddb3fb87aa3c65fe781f850`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 940.9 KB (940882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5cba85e675197ad1c4e50d53e4e0729a14dc95038bda054e5abd51eb1af7f2`  
		Last Modified: Wed, 08 Jan 2025 18:23:08 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f05948628ca40470c501b71b53616ed24606f1134506db08b96b27478c89d57`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:b3f96e58c405edfc5b23834bcd9683db84046ee1fa81b8d46f155e9fed60f03a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.8 KB (459822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1529a78ef0f77904d171c12f07aa6b11918c33f3b928126ca142a4367ec504ed`

```dockerfile
```

-	Layers:
	-	`sha256:c9238aa73cb4939daf0b36f8780096b38dffd6ec4dc7652dfc9f0af2bde3c4af`  
		Last Modified: Wed, 08 Jan 2025 18:23:08 GMT  
		Size: 428.9 KB (428900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c908b98f3fbcad032d5c687df01d8b71bdca05c3d5d9ede3de79959a5952e43`  
		Last Modified: Wed, 08 Jan 2025 18:23:08 GMT  
		Size: 30.9 KB (30922 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; ppc64le

```console
$ docker pull composer@sha256:97d2f5c73782a176aa8eeb4a6fb89685e3a6d796f569677b6f72f969cf9934f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76363875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf75369f387c182b0ae224de9bda281b6a897383b3ab57c201fcc90604499a3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:26aa0c6396d98d67cdb7cff725afeddc08a54386e1d5e68f922a402f902d2924`  
		Last Modified: Thu, 09 Jan 2025 01:29:00 GMT  
		Size: 32.9 MB (32943089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ed0b4e6953a4bbe30d89c2f6151304b7cf0496993f171b508a19e501ebb706`  
		Last Modified: Thu, 09 Jan 2025 01:28:58 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44629d85a30e074812821013cc532460d1a718009c13171f14849c0d657818a4`  
		Last Modified: Thu, 09 Jan 2025 01:30:41 GMT  
		Size: 972.2 KB (972200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae0870d155edbd5d8f44620e8fd1417a0014da3dfe8abbbbca1c3d61219eb81`  
		Last Modified: Thu, 09 Jan 2025 01:30:41 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02e4c72de67abe0992326a86fdd96d036c896006eefc4ebc2e4c8e8d2585b5c`  
		Last Modified: Thu, 09 Jan 2025 01:30:41 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:fa6b1fc46b576c78c7a115d62747e15d639dbd1203fe43c6bc77acf5aa1a232b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a72a373632f2591e90cab7db68d37ee6482a4c2edb1d976f21cf62c54c5e1c`

```dockerfile
```

-	Layers:
	-	`sha256:efae3b02ff4c673696f9f89debaabbaab703435f95f36e7e6c432283c9def1b9`  
		Last Modified: Thu, 09 Jan 2025 01:30:41 GMT  
		Size: 2.2 MB (2157810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b48f891f351b49b85f862d539710519a715d6ec7d72820a70c1457ed976bf76c`  
		Last Modified: Thu, 09 Jan 2025 01:30:41 GMT  
		Size: 31.0 KB (31006 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; riscv64

```console
$ docker pull composer@sha256:3e462cf88e80da773ee73a33af30f6d3d26181850646602bdd129b9e6b83e354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73723546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574b603af8bd97b8da7d159df81aadf76084e5f3c79ea67b42293b551a37a8e9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
		Size: 3.4 MB (3445761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9c93fa8ac38e6017fe5251627d738084239fbab425319ead8bdece897e493`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe2d3ee20829a994ce6548409e985a58c1c6ec2238583410057ae0e6dfe95a1`  
		Last Modified: Fri, 20 Dec 2024 22:27:49 GMT  
		Size: 13.6 MB (13580504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a67918c3771135e7a2b16f42498ea94d985dc8f6407db3a3ee60e1e3e9373b`  
		Last Modified: Fri, 20 Dec 2024 22:27:47 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e567d61ea86fdc5c63b8ce75eb88bcda35c75049600dcb0b112964a7da3ac42f`  
		Last Modified: Fri, 20 Dec 2024 22:27:50 GMT  
		Size: 20.8 MB (20797397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263bcc5a009f020e39d0e162f139f8f8433852481d7368c9cde637ffd9f841e5`  
		Last Modified: Fri, 20 Dec 2024 22:27:47 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9ec8a613ce316b270ee3a65ed2d2041d6579061f1f8b0d0725f55b6f9e84fc`  
		Last Modified: Fri, 20 Dec 2024 22:27:48 GMT  
		Size: 19.9 KB (19885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe21f96e7307414693b828f2173bcaa37df5cd8443ce028ad761b4e69270f7`  
		Last Modified: Sat, 21 Dec 2024 14:35:27 GMT  
		Size: 31.0 MB (31000197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4008aa8424d8743580595dbf0803a9aa275eb20020eb2e8e47ed5c19aeeee6bf`  
		Last Modified: Sat, 21 Dec 2024 14:35:22 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5e822a66d5151001774d542d9094b01daf100ed2157872f9877d906d3c58a9`  
		Last Modified: Sat, 21 Dec 2024 14:45:40 GMT  
		Size: 1.5 MB (1520901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d77b818da6a47633d65ab0ff8e7daaed7befa104f5c9fa09f8e82e8de6c9d7`  
		Last Modified: Sat, 21 Dec 2024 14:45:40 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9571248a3d79f630c65eb387c628804b009f25caf903c98b8310385c46a5a5bd`  
		Last Modified: Sat, 21 Dec 2024 14:45:40 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:74b44e5f1a6c0f35773105a798bc63b173bf7cb75c4af4fff3ed81bacc21ff2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50e5ce06ed6611b3c5d9bdf45873ac77f16e159372983bec4c7a1b140cc719b`

```dockerfile
```

-	Layers:
	-	`sha256:398b33f39dac14afa5780baf352eea65f1df765dec833491135a12f9ba4832c3`  
		Last Modified: Sat, 21 Dec 2024 14:45:40 GMT  
		Size: 2.2 MB (2158052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4e925469f2c58d80e4fb70d7fbe2424ee1f9a79db882fb4c3076c60ee921b42`  
		Last Modified: Sat, 21 Dec 2024 14:45:39 GMT  
		Size: 31.0 KB (31009 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; s390x

```console
$ docker pull composer@sha256:08f3eeed2a12f83f65d960fac5be4e0480c8734b7238bf20cf349178db442c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74620254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3785283d6b78dee3e29f5436fad47897fe6bbbf6ceefda0279058cc184d8e1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:3f63ed19a544e5e26e1152afe55e1e34f250a8fe3982b62ef0754513377c899c`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 31.7 MB (31674581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59aadc194319e2220294cf3ff3a08addb3a57ecf676d4fb858a0ff81e0bd6c8d`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b198938ddcda767ec453fd4c4438c1abaf40aedd368a78f6db8d56a6bd554a0`  
		Last Modified: Tue, 07 Jan 2025 15:53:31 GMT  
		Size: 968.3 KB (968314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0861e10c690483650a5c5b80a34f8062cf1c4991e5345d85cd0d17d56bb1ff`  
		Last Modified: Tue, 07 Jan 2025 15:53:31 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af048d98bf3c8a90c18d2c3115fa12f26188777034752c35b1c625281aa269c`  
		Last Modified: Tue, 07 Jan 2025 15:53:31 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:05f1fd51a10262cb513a2306d8841324bbae54348258bc3f43dc9b5b74169b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2181612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db7690f86ec1f52b5f920e134a8d3e09182d744d83472f8a9b493fe2b6b199b`

```dockerfile
```

-	Layers:
	-	`sha256:c5501f10e797650932c9d815eb6f1a7b7f7dd5eb6ccf761df1bdcb2feca404f7`  
		Last Modified: Tue, 07 Jan 2025 15:53:31 GMT  
		Size: 2.2 MB (2150654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a21f1b92bdd5f3c0b884d4d21f5cd59fe82cc515164be3abafa0e6508e82ae3`  
		Last Modified: Tue, 07 Jan 2025 15:53:30 GMT  
		Size: 31.0 KB (30958 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8.4`

```console
$ docker pull composer@sha256:5343ca2d163000fc433898aba00818152bece4bf10d46745102378ace3964eed
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

### `composer:2.8.4` - linux; amd64

```console
$ docker pull composer@sha256:005298f3a8e453451ef3bf7b15bea492d29101a86bfa8407341d0b12038767ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74326216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53abc0a37f7ee2356900dd8be0983112aca615687e2fdcff5cd9232b69ca7b09`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:978a5b5b12769c41e9b5454d72092585972d47afc882215a4e67bfc88f493d5b`  
		Last Modified: Wed, 08 Jan 2025 18:23:13 GMT  
		Size: 31.9 MB (31896574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd30bbc7a30aecea7ad4e5f034902fbe2aea4b830d50751110bf328769b935d`  
		Last Modified: Wed, 08 Jan 2025 18:23:13 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f715b47c3e106a8a84813784dd5a6789a75cf4f1a2b83348b02dddae9efe6cd5`  
		Last Modified: Wed, 08 Jan 2025 18:23:13 GMT  
		Size: 965.6 KB (965645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db0149e0574a30416bd1757e8aa3fa032d928877beb21c19e749444aef6f6c4`  
		Last Modified: Wed, 08 Jan 2025 18:23:13 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afbc72cb26a761175852095f9aa309ccc07b9fa82ed03ddca84e352eb95eec8`  
		Last Modified: Wed, 08 Jan 2025 18:23:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.4` - unknown; unknown

```console
$ docker pull composer@sha256:9d3e14b7d9b12b6593806213c69f200adb4eb03853681321f6a129b4917a7f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94fce35936248103dff28c70c7980eb4751a8a0d2137edda229bf8153dd787b9`

```dockerfile
```

-	Layers:
	-	`sha256:bccd273f9b6cb004932051c1a84a4c3b9c7085addbebadb6b0509df3ccbaf03b`  
		Last Modified: Wed, 08 Jan 2025 18:23:13 GMT  
		Size: 2.2 MB (2159247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5c182f2e98dc5d74159bb452b1e911f95f67e01096d4e4db9f66fac94095d3e`  
		Last Modified: Wed, 08 Jan 2025 18:23:13 GMT  
		Size: 31.0 KB (30958 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.4` - linux; arm variant v6

```console
$ docker pull composer@sha256:33037a2771fa573b556f6f6f9b34a624d607f2e5ad17400931d72e522e7e0b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70883858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2742f0de5a004bc434bb7a5cdeeff99f5cb1e8cc1657ac03bdd12766e61d221b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:8bfbe143528e86684282cbfd298570a16342fbf7feefa882f4ff4af7f9116796`  
		Last Modified: Tue, 07 Jan 2025 18:31:35 GMT  
		Size: 30.6 MB (30640654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a227f011e7035c2e61babbdbf90fea0a1845e1422312eda1608ae428cda1dead`  
		Last Modified: Tue, 07 Jan 2025 18:31:34 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb4d70fa8e2e9e943104bb6ab3e28f71390a553840cdba5cbd7d8b618fa243b`  
		Last Modified: Tue, 07 Jan 2025 18:32:59 GMT  
		Size: 965.3 KB (965306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3826a6b574a6d595615f31b1ef9fae34a30dd1e418f79cee3bc7ab6a295e46ee`  
		Last Modified: Thu, 12 Dec 2024 19:28:04 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a40b7b2051e2d3ecb4c9cc96ce48f3cf1110f183d98c8e8df9222924c2c99b`  
		Last Modified: Tue, 07 Jan 2025 18:32:58 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.4` - unknown; unknown

```console
$ docker pull composer@sha256:2f1c770454c1f9a39dc50afb470a9b303fbe20cec59ff4f1ea52a5865418d5c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180abf7fdf1d40f88a8ff64fb696c6dc3fe366f009e811e2a5fb3a979399e388`

```dockerfile
```

-	Layers:
	-	`sha256:cb72041883c9070c4153b3ab41d1755dcab7079e741903798832e7f29382bdb3`  
		Last Modified: Tue, 07 Jan 2025 18:32:58 GMT  
		Size: 30.8 KB (30844 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.4` - linux; arm variant v7

```console
$ docker pull composer@sha256:594f53ed686765023ab6d53e4af003b79d54804802b89d575f23947c8360d70f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68909642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa3aff9d167a0aafd70dbccf29d249d860926dda0e4dc2f690134b0481ffebf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:0a2bf4fd23a4343e4fa39d2a63004ae4de297973415bc8809c9c56b1097caf8a`  
		Last Modified: Tue, 07 Jan 2025 18:37:42 GMT  
		Size: 30.2 MB (30150038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89da730f1c4439581b1de7342d8be357e2ea326296a6c567ba8c4e6dad0fd87e`  
		Last Modified: Tue, 07 Jan 2025 18:37:41 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6a1bad3eb85e0825e2a02155cda0ee2fe950d9e630efe3af93ce9a7886e632`  
		Last Modified: Tue, 07 Jan 2025 18:39:18 GMT  
		Size: 956.5 KB (956472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de4418b34011a326f53b6ef2ec2a18d2d74182277c0113bf6ddfb50428af1cc`  
		Last Modified: Tue, 07 Jan 2025 18:39:18 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4faa8b49ea62821ab26a87a3077ae98e271392d81fb83435adb091d96b34cff`  
		Last Modified: Tue, 07 Jan 2025 18:39:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.4` - unknown; unknown

```console
$ docker pull composer@sha256:68947fc357f316533e66560925f64ac5c9bb0afd25a3aa7476e5f1ab0906c76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2184753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b0c05709ce6b958c6e8499802fc327c393298d2aaccbf1e9c73d062398ea6c`

```dockerfile
```

-	Layers:
	-	`sha256:8b8b8d795164c1e481dd469dee447f8c307553b607c9172fb3b7152cc5faac97`  
		Last Modified: Tue, 07 Jan 2025 18:39:18 GMT  
		Size: 2.2 MB (2153693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1807ecf10b7f0743c949836b691547a273d14ce37eca27b9bedc46ef878adfb9`  
		Last Modified: Tue, 07 Jan 2025 18:39:17 GMT  
		Size: 31.1 KB (31060 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.4` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:df5c4f311d7e77e252ad95f8f7ea66b3aa98394396e14cc9c7ea3ebb5b792b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74306091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7234ed006eb005ba5fba955cd5fba1a60de1a7af6badef61aa432ed5e52d0fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:a0c59331d5588d1a35cef8b8de8c57f9df896f2230d66caa4f7510c076bcf10b`  
		Last Modified: Tue, 07 Jan 2025 16:07:22 GMT  
		Size: 32.0 MB (32004107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bc1dca7afc6e7b778ae0cc6c16db02fce566edf2e75b273bdf7c721ed764f9`  
		Last Modified: Tue, 07 Jan 2025 16:07:20 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b939a8afce976fe45002973da6930697f18eae7fa27e8ce49dd2c17f65d1e5`  
		Last Modified: Tue, 07 Jan 2025 16:08:40 GMT  
		Size: 965.5 KB (965463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d8fee934fea50432c31925b35c4f56fde5213f691658f7dadc905edb60c69b`  
		Last Modified: Tue, 07 Jan 2025 16:08:40 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bdaaa2c66e9b7e2e40087cc900107f729d95917438796593acc5d49d16a25b`  
		Last Modified: Tue, 07 Jan 2025 16:08:40 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.4` - unknown; unknown

```console
$ docker pull composer@sha256:5b3109cf34a8a6a9015cd8e20d5b60c4266fb5e5472d93092d79a788e22a1660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2184613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69df30c47d82fc2af4aba3ceca927f09a66f7144746a1ef19ab80acf5aa9f172`

```dockerfile
```

-	Layers:
	-	`sha256:cc0b071dfc1da5169488f1763875f769e28e8e5d06cba6d51427f582356b8d82`  
		Last Modified: Tue, 07 Jan 2025 16:08:40 GMT  
		Size: 2.2 MB (2153521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3593f9cd7e2f2a95a36b9cc0e63c452c488712bf7dc7f1a117dd35912fb9b537`  
		Last Modified: Tue, 07 Jan 2025 16:08:40 GMT  
		Size: 31.1 KB (31092 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.4` - linux; 386

```console
$ docker pull composer@sha256:c31ead984e1ee2d8efec17df384d63f4e1c5d854b428c40c215228a5ece6636b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54202544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a87b5519f7dbb8909d8ada69772bedef00855c1778fdb78caa889240def67d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:9057d2e3075e68379daa14741eee46f10348413e4debd93c3164c6d9281ff2ce`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 11.4 MB (11421295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9c3281d500418c6584ec3d0940fad88e375e39cbcb6f7b1f1f1605654ff468`  
		Last Modified: Wed, 08 Jan 2025 18:23:08 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7282b8d7cb806abb76d8b38dcb1f442799b33e340ddb3fb87aa3c65fe781f850`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 940.9 KB (940882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5cba85e675197ad1c4e50d53e4e0729a14dc95038bda054e5abd51eb1af7f2`  
		Last Modified: Wed, 08 Jan 2025 18:23:08 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f05948628ca40470c501b71b53616ed24606f1134506db08b96b27478c89d57`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.4` - unknown; unknown

```console
$ docker pull composer@sha256:b3f96e58c405edfc5b23834bcd9683db84046ee1fa81b8d46f155e9fed60f03a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.8 KB (459822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1529a78ef0f77904d171c12f07aa6b11918c33f3b928126ca142a4367ec504ed`

```dockerfile
```

-	Layers:
	-	`sha256:c9238aa73cb4939daf0b36f8780096b38dffd6ec4dc7652dfc9f0af2bde3c4af`  
		Last Modified: Wed, 08 Jan 2025 18:23:08 GMT  
		Size: 428.9 KB (428900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c908b98f3fbcad032d5c687df01d8b71bdca05c3d5d9ede3de79959a5952e43`  
		Last Modified: Wed, 08 Jan 2025 18:23:08 GMT  
		Size: 30.9 KB (30922 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.4` - linux; ppc64le

```console
$ docker pull composer@sha256:97d2f5c73782a176aa8eeb4a6fb89685e3a6d796f569677b6f72f969cf9934f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76363875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf75369f387c182b0ae224de9bda281b6a897383b3ab57c201fcc90604499a3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:26aa0c6396d98d67cdb7cff725afeddc08a54386e1d5e68f922a402f902d2924`  
		Last Modified: Thu, 09 Jan 2025 01:29:00 GMT  
		Size: 32.9 MB (32943089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ed0b4e6953a4bbe30d89c2f6151304b7cf0496993f171b508a19e501ebb706`  
		Last Modified: Thu, 09 Jan 2025 01:28:58 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44629d85a30e074812821013cc532460d1a718009c13171f14849c0d657818a4`  
		Last Modified: Thu, 09 Jan 2025 01:30:41 GMT  
		Size: 972.2 KB (972200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae0870d155edbd5d8f44620e8fd1417a0014da3dfe8abbbbca1c3d61219eb81`  
		Last Modified: Thu, 09 Jan 2025 01:30:41 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02e4c72de67abe0992326a86fdd96d036c896006eefc4ebc2e4c8e8d2585b5c`  
		Last Modified: Thu, 09 Jan 2025 01:30:41 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.4` - unknown; unknown

```console
$ docker pull composer@sha256:fa6b1fc46b576c78c7a115d62747e15d639dbd1203fe43c6bc77acf5aa1a232b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a72a373632f2591e90cab7db68d37ee6482a4c2edb1d976f21cf62c54c5e1c`

```dockerfile
```

-	Layers:
	-	`sha256:efae3b02ff4c673696f9f89debaabbaab703435f95f36e7e6c432283c9def1b9`  
		Last Modified: Thu, 09 Jan 2025 01:30:41 GMT  
		Size: 2.2 MB (2157810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b48f891f351b49b85f862d539710519a715d6ec7d72820a70c1457ed976bf76c`  
		Last Modified: Thu, 09 Jan 2025 01:30:41 GMT  
		Size: 31.0 KB (31006 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.4` - linux; riscv64

```console
$ docker pull composer@sha256:3e462cf88e80da773ee73a33af30f6d3d26181850646602bdd129b9e6b83e354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73723546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574b603af8bd97b8da7d159df81aadf76084e5f3c79ea67b42293b551a37a8e9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
		Size: 3.4 MB (3445761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9c93fa8ac38e6017fe5251627d738084239fbab425319ead8bdece897e493`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe2d3ee20829a994ce6548409e985a58c1c6ec2238583410057ae0e6dfe95a1`  
		Last Modified: Fri, 20 Dec 2024 22:27:49 GMT  
		Size: 13.6 MB (13580504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a67918c3771135e7a2b16f42498ea94d985dc8f6407db3a3ee60e1e3e9373b`  
		Last Modified: Fri, 20 Dec 2024 22:27:47 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e567d61ea86fdc5c63b8ce75eb88bcda35c75049600dcb0b112964a7da3ac42f`  
		Last Modified: Fri, 20 Dec 2024 22:27:50 GMT  
		Size: 20.8 MB (20797397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263bcc5a009f020e39d0e162f139f8f8433852481d7368c9cde637ffd9f841e5`  
		Last Modified: Fri, 20 Dec 2024 22:27:47 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9ec8a613ce316b270ee3a65ed2d2041d6579061f1f8b0d0725f55b6f9e84fc`  
		Last Modified: Fri, 20 Dec 2024 22:27:48 GMT  
		Size: 19.9 KB (19885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe21f96e7307414693b828f2173bcaa37df5cd8443ce028ad761b4e69270f7`  
		Last Modified: Sat, 21 Dec 2024 14:35:27 GMT  
		Size: 31.0 MB (31000197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4008aa8424d8743580595dbf0803a9aa275eb20020eb2e8e47ed5c19aeeee6bf`  
		Last Modified: Sat, 21 Dec 2024 14:35:22 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5e822a66d5151001774d542d9094b01daf100ed2157872f9877d906d3c58a9`  
		Last Modified: Sat, 21 Dec 2024 14:45:40 GMT  
		Size: 1.5 MB (1520901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d77b818da6a47633d65ab0ff8e7daaed7befa104f5c9fa09f8e82e8de6c9d7`  
		Last Modified: Sat, 21 Dec 2024 14:45:40 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9571248a3d79f630c65eb387c628804b009f25caf903c98b8310385c46a5a5bd`  
		Last Modified: Sat, 21 Dec 2024 14:45:40 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.4` - unknown; unknown

```console
$ docker pull composer@sha256:74b44e5f1a6c0f35773105a798bc63b173bf7cb75c4af4fff3ed81bacc21ff2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50e5ce06ed6611b3c5d9bdf45873ac77f16e159372983bec4c7a1b140cc719b`

```dockerfile
```

-	Layers:
	-	`sha256:398b33f39dac14afa5780baf352eea65f1df765dec833491135a12f9ba4832c3`  
		Last Modified: Sat, 21 Dec 2024 14:45:40 GMT  
		Size: 2.2 MB (2158052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4e925469f2c58d80e4fb70d7fbe2424ee1f9a79db882fb4c3076c60ee921b42`  
		Last Modified: Sat, 21 Dec 2024 14:45:39 GMT  
		Size: 31.0 KB (31009 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.4` - linux; s390x

```console
$ docker pull composer@sha256:08f3eeed2a12f83f65d960fac5be4e0480c8734b7238bf20cf349178db442c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74620254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3785283d6b78dee3e29f5436fad47897fe6bbbf6ceefda0279058cc184d8e1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:3f63ed19a544e5e26e1152afe55e1e34f250a8fe3982b62ef0754513377c899c`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 31.7 MB (31674581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59aadc194319e2220294cf3ff3a08addb3a57ecf676d4fb858a0ff81e0bd6c8d`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b198938ddcda767ec453fd4c4438c1abaf40aedd368a78f6db8d56a6bd554a0`  
		Last Modified: Tue, 07 Jan 2025 15:53:31 GMT  
		Size: 968.3 KB (968314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0861e10c690483650a5c5b80a34f8062cf1c4991e5345d85cd0d17d56bb1ff`  
		Last Modified: Tue, 07 Jan 2025 15:53:31 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af048d98bf3c8a90c18d2c3115fa12f26188777034752c35b1c625281aa269c`  
		Last Modified: Tue, 07 Jan 2025 15:53:31 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.4` - unknown; unknown

```console
$ docker pull composer@sha256:05f1fd51a10262cb513a2306d8841324bbae54348258bc3f43dc9b5b74169b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2181612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db7690f86ec1f52b5f920e134a8d3e09182d744d83472f8a9b493fe2b6b199b`

```dockerfile
```

-	Layers:
	-	`sha256:c5501f10e797650932c9d815eb6f1a7b7f7dd5eb6ccf761df1bdcb2feca404f7`  
		Last Modified: Tue, 07 Jan 2025 15:53:31 GMT  
		Size: 2.2 MB (2150654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a21f1b92bdd5f3c0b884d4d21f5cd59fe82cc515164be3abafa0e6508e82ae3`  
		Last Modified: Tue, 07 Jan 2025 15:53:30 GMT  
		Size: 31.0 KB (30958 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:latest`

```console
$ docker pull composer@sha256:5343ca2d163000fc433898aba00818152bece4bf10d46745102378ace3964eed
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

### `composer:latest` - linux; amd64

```console
$ docker pull composer@sha256:005298f3a8e453451ef3bf7b15bea492d29101a86bfa8407341d0b12038767ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74326216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53abc0a37f7ee2356900dd8be0983112aca615687e2fdcff5cd9232b69ca7b09`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:978a5b5b12769c41e9b5454d72092585972d47afc882215a4e67bfc88f493d5b`  
		Last Modified: Wed, 08 Jan 2025 18:23:13 GMT  
		Size: 31.9 MB (31896574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd30bbc7a30aecea7ad4e5f034902fbe2aea4b830d50751110bf328769b935d`  
		Last Modified: Wed, 08 Jan 2025 18:23:13 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f715b47c3e106a8a84813784dd5a6789a75cf4f1a2b83348b02dddae9efe6cd5`  
		Last Modified: Wed, 08 Jan 2025 18:23:13 GMT  
		Size: 965.6 KB (965645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db0149e0574a30416bd1757e8aa3fa032d928877beb21c19e749444aef6f6c4`  
		Last Modified: Wed, 08 Jan 2025 18:23:13 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afbc72cb26a761175852095f9aa309ccc07b9fa82ed03ddca84e352eb95eec8`  
		Last Modified: Wed, 08 Jan 2025 18:23:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:9d3e14b7d9b12b6593806213c69f200adb4eb03853681321f6a129b4917a7f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94fce35936248103dff28c70c7980eb4751a8a0d2137edda229bf8153dd787b9`

```dockerfile
```

-	Layers:
	-	`sha256:bccd273f9b6cb004932051c1a84a4c3b9c7085addbebadb6b0509df3ccbaf03b`  
		Last Modified: Wed, 08 Jan 2025 18:23:13 GMT  
		Size: 2.2 MB (2159247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5c182f2e98dc5d74159bb452b1e911f95f67e01096d4e4db9f66fac94095d3e`  
		Last Modified: Wed, 08 Jan 2025 18:23:13 GMT  
		Size: 31.0 KB (30958 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:33037a2771fa573b556f6f6f9b34a624d607f2e5ad17400931d72e522e7e0b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70883858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2742f0de5a004bc434bb7a5cdeeff99f5cb1e8cc1657ac03bdd12766e61d221b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:8bfbe143528e86684282cbfd298570a16342fbf7feefa882f4ff4af7f9116796`  
		Last Modified: Tue, 07 Jan 2025 18:31:35 GMT  
		Size: 30.6 MB (30640654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a227f011e7035c2e61babbdbf90fea0a1845e1422312eda1608ae428cda1dead`  
		Last Modified: Tue, 07 Jan 2025 18:31:34 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb4d70fa8e2e9e943104bb6ab3e28f71390a553840cdba5cbd7d8b618fa243b`  
		Last Modified: Tue, 07 Jan 2025 18:32:59 GMT  
		Size: 965.3 KB (965306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3826a6b574a6d595615f31b1ef9fae34a30dd1e418f79cee3bc7ab6a295e46ee`  
		Last Modified: Thu, 12 Dec 2024 19:28:04 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a40b7b2051e2d3ecb4c9cc96ce48f3cf1110f183d98c8e8df9222924c2c99b`  
		Last Modified: Tue, 07 Jan 2025 18:32:58 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:2f1c770454c1f9a39dc50afb470a9b303fbe20cec59ff4f1ea52a5865418d5c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180abf7fdf1d40f88a8ff64fb696c6dc3fe366f009e811e2a5fb3a979399e388`

```dockerfile
```

-	Layers:
	-	`sha256:cb72041883c9070c4153b3ab41d1755dcab7079e741903798832e7f29382bdb3`  
		Last Modified: Tue, 07 Jan 2025 18:32:58 GMT  
		Size: 30.8 KB (30844 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:594f53ed686765023ab6d53e4af003b79d54804802b89d575f23947c8360d70f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68909642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa3aff9d167a0aafd70dbccf29d249d860926dda0e4dc2f690134b0481ffebf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:0a2bf4fd23a4343e4fa39d2a63004ae4de297973415bc8809c9c56b1097caf8a`  
		Last Modified: Tue, 07 Jan 2025 18:37:42 GMT  
		Size: 30.2 MB (30150038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89da730f1c4439581b1de7342d8be357e2ea326296a6c567ba8c4e6dad0fd87e`  
		Last Modified: Tue, 07 Jan 2025 18:37:41 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6a1bad3eb85e0825e2a02155cda0ee2fe950d9e630efe3af93ce9a7886e632`  
		Last Modified: Tue, 07 Jan 2025 18:39:18 GMT  
		Size: 956.5 KB (956472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de4418b34011a326f53b6ef2ec2a18d2d74182277c0113bf6ddfb50428af1cc`  
		Last Modified: Tue, 07 Jan 2025 18:39:18 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4faa8b49ea62821ab26a87a3077ae98e271392d81fb83435adb091d96b34cff`  
		Last Modified: Tue, 07 Jan 2025 18:39:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:68947fc357f316533e66560925f64ac5c9bb0afd25a3aa7476e5f1ab0906c76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2184753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b0c05709ce6b958c6e8499802fc327c393298d2aaccbf1e9c73d062398ea6c`

```dockerfile
```

-	Layers:
	-	`sha256:8b8b8d795164c1e481dd469dee447f8c307553b607c9172fb3b7152cc5faac97`  
		Last Modified: Tue, 07 Jan 2025 18:39:18 GMT  
		Size: 2.2 MB (2153693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1807ecf10b7f0743c949836b691547a273d14ce37eca27b9bedc46ef878adfb9`  
		Last Modified: Tue, 07 Jan 2025 18:39:17 GMT  
		Size: 31.1 KB (31060 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:df5c4f311d7e77e252ad95f8f7ea66b3aa98394396e14cc9c7ea3ebb5b792b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74306091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7234ed006eb005ba5fba955cd5fba1a60de1a7af6badef61aa432ed5e52d0fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:a0c59331d5588d1a35cef8b8de8c57f9df896f2230d66caa4f7510c076bcf10b`  
		Last Modified: Tue, 07 Jan 2025 16:07:22 GMT  
		Size: 32.0 MB (32004107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bc1dca7afc6e7b778ae0cc6c16db02fce566edf2e75b273bdf7c721ed764f9`  
		Last Modified: Tue, 07 Jan 2025 16:07:20 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b939a8afce976fe45002973da6930697f18eae7fa27e8ce49dd2c17f65d1e5`  
		Last Modified: Tue, 07 Jan 2025 16:08:40 GMT  
		Size: 965.5 KB (965463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d8fee934fea50432c31925b35c4f56fde5213f691658f7dadc905edb60c69b`  
		Last Modified: Tue, 07 Jan 2025 16:08:40 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bdaaa2c66e9b7e2e40087cc900107f729d95917438796593acc5d49d16a25b`  
		Last Modified: Tue, 07 Jan 2025 16:08:40 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:5b3109cf34a8a6a9015cd8e20d5b60c4266fb5e5472d93092d79a788e22a1660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2184613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69df30c47d82fc2af4aba3ceca927f09a66f7144746a1ef19ab80acf5aa9f172`

```dockerfile
```

-	Layers:
	-	`sha256:cc0b071dfc1da5169488f1763875f769e28e8e5d06cba6d51427f582356b8d82`  
		Last Modified: Tue, 07 Jan 2025 16:08:40 GMT  
		Size: 2.2 MB (2153521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3593f9cd7e2f2a95a36b9cc0e63c452c488712bf7dc7f1a117dd35912fb9b537`  
		Last Modified: Tue, 07 Jan 2025 16:08:40 GMT  
		Size: 31.1 KB (31092 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; 386

```console
$ docker pull composer@sha256:c31ead984e1ee2d8efec17df384d63f4e1c5d854b428c40c215228a5ece6636b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54202544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a87b5519f7dbb8909d8ada69772bedef00855c1778fdb78caa889240def67d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:9057d2e3075e68379daa14741eee46f10348413e4debd93c3164c6d9281ff2ce`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 11.4 MB (11421295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9c3281d500418c6584ec3d0940fad88e375e39cbcb6f7b1f1f1605654ff468`  
		Last Modified: Wed, 08 Jan 2025 18:23:08 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7282b8d7cb806abb76d8b38dcb1f442799b33e340ddb3fb87aa3c65fe781f850`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 940.9 KB (940882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5cba85e675197ad1c4e50d53e4e0729a14dc95038bda054e5abd51eb1af7f2`  
		Last Modified: Wed, 08 Jan 2025 18:23:08 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f05948628ca40470c501b71b53616ed24606f1134506db08b96b27478c89d57`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:b3f96e58c405edfc5b23834bcd9683db84046ee1fa81b8d46f155e9fed60f03a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.8 KB (459822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1529a78ef0f77904d171c12f07aa6b11918c33f3b928126ca142a4367ec504ed`

```dockerfile
```

-	Layers:
	-	`sha256:c9238aa73cb4939daf0b36f8780096b38dffd6ec4dc7652dfc9f0af2bde3c4af`  
		Last Modified: Wed, 08 Jan 2025 18:23:08 GMT  
		Size: 428.9 KB (428900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c908b98f3fbcad032d5c687df01d8b71bdca05c3d5d9ede3de79959a5952e43`  
		Last Modified: Wed, 08 Jan 2025 18:23:08 GMT  
		Size: 30.9 KB (30922 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; ppc64le

```console
$ docker pull composer@sha256:97d2f5c73782a176aa8eeb4a6fb89685e3a6d796f569677b6f72f969cf9934f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76363875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf75369f387c182b0ae224de9bda281b6a897383b3ab57c201fcc90604499a3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:26aa0c6396d98d67cdb7cff725afeddc08a54386e1d5e68f922a402f902d2924`  
		Last Modified: Thu, 09 Jan 2025 01:29:00 GMT  
		Size: 32.9 MB (32943089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ed0b4e6953a4bbe30d89c2f6151304b7cf0496993f171b508a19e501ebb706`  
		Last Modified: Thu, 09 Jan 2025 01:28:58 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44629d85a30e074812821013cc532460d1a718009c13171f14849c0d657818a4`  
		Last Modified: Thu, 09 Jan 2025 01:30:41 GMT  
		Size: 972.2 KB (972200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae0870d155edbd5d8f44620e8fd1417a0014da3dfe8abbbbca1c3d61219eb81`  
		Last Modified: Thu, 09 Jan 2025 01:30:41 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02e4c72de67abe0992326a86fdd96d036c896006eefc4ebc2e4c8e8d2585b5c`  
		Last Modified: Thu, 09 Jan 2025 01:30:41 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:fa6b1fc46b576c78c7a115d62747e15d639dbd1203fe43c6bc77acf5aa1a232b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a72a373632f2591e90cab7db68d37ee6482a4c2edb1d976f21cf62c54c5e1c`

```dockerfile
```

-	Layers:
	-	`sha256:efae3b02ff4c673696f9f89debaabbaab703435f95f36e7e6c432283c9def1b9`  
		Last Modified: Thu, 09 Jan 2025 01:30:41 GMT  
		Size: 2.2 MB (2157810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b48f891f351b49b85f862d539710519a715d6ec7d72820a70c1457ed976bf76c`  
		Last Modified: Thu, 09 Jan 2025 01:30:41 GMT  
		Size: 31.0 KB (31006 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; riscv64

```console
$ docker pull composer@sha256:3e462cf88e80da773ee73a33af30f6d3d26181850646602bdd129b9e6b83e354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73723546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574b603af8bd97b8da7d159df81aadf76084e5f3c79ea67b42293b551a37a8e9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
		Size: 3.4 MB (3445761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9c93fa8ac38e6017fe5251627d738084239fbab425319ead8bdece897e493`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe2d3ee20829a994ce6548409e985a58c1c6ec2238583410057ae0e6dfe95a1`  
		Last Modified: Fri, 20 Dec 2024 22:27:49 GMT  
		Size: 13.6 MB (13580504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a67918c3771135e7a2b16f42498ea94d985dc8f6407db3a3ee60e1e3e9373b`  
		Last Modified: Fri, 20 Dec 2024 22:27:47 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e567d61ea86fdc5c63b8ce75eb88bcda35c75049600dcb0b112964a7da3ac42f`  
		Last Modified: Fri, 20 Dec 2024 22:27:50 GMT  
		Size: 20.8 MB (20797397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263bcc5a009f020e39d0e162f139f8f8433852481d7368c9cde637ffd9f841e5`  
		Last Modified: Fri, 20 Dec 2024 22:27:47 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9ec8a613ce316b270ee3a65ed2d2041d6579061f1f8b0d0725f55b6f9e84fc`  
		Last Modified: Fri, 20 Dec 2024 22:27:48 GMT  
		Size: 19.9 KB (19885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe21f96e7307414693b828f2173bcaa37df5cd8443ce028ad761b4e69270f7`  
		Last Modified: Sat, 21 Dec 2024 14:35:27 GMT  
		Size: 31.0 MB (31000197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4008aa8424d8743580595dbf0803a9aa275eb20020eb2e8e47ed5c19aeeee6bf`  
		Last Modified: Sat, 21 Dec 2024 14:35:22 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5e822a66d5151001774d542d9094b01daf100ed2157872f9877d906d3c58a9`  
		Last Modified: Sat, 21 Dec 2024 14:45:40 GMT  
		Size: 1.5 MB (1520901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d77b818da6a47633d65ab0ff8e7daaed7befa104f5c9fa09f8e82e8de6c9d7`  
		Last Modified: Sat, 21 Dec 2024 14:45:40 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9571248a3d79f630c65eb387c628804b009f25caf903c98b8310385c46a5a5bd`  
		Last Modified: Sat, 21 Dec 2024 14:45:40 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:74b44e5f1a6c0f35773105a798bc63b173bf7cb75c4af4fff3ed81bacc21ff2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50e5ce06ed6611b3c5d9bdf45873ac77f16e159372983bec4c7a1b140cc719b`

```dockerfile
```

-	Layers:
	-	`sha256:398b33f39dac14afa5780baf352eea65f1df765dec833491135a12f9ba4832c3`  
		Last Modified: Sat, 21 Dec 2024 14:45:40 GMT  
		Size: 2.2 MB (2158052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4e925469f2c58d80e4fb70d7fbe2424ee1f9a79db882fb4c3076c60ee921b42`  
		Last Modified: Sat, 21 Dec 2024 14:45:39 GMT  
		Size: 31.0 KB (31009 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; s390x

```console
$ docker pull composer@sha256:08f3eeed2a12f83f65d960fac5be4e0480c8734b7238bf20cf349178db442c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74620254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3785283d6b78dee3e29f5436fad47897fe6bbbf6ceefda0279058cc184d8e1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
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
	-	`sha256:3f63ed19a544e5e26e1152afe55e1e34f250a8fe3982b62ef0754513377c899c`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 31.7 MB (31674581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59aadc194319e2220294cf3ff3a08addb3a57ecf676d4fb858a0ff81e0bd6c8d`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b198938ddcda767ec453fd4c4438c1abaf40aedd368a78f6db8d56a6bd554a0`  
		Last Modified: Tue, 07 Jan 2025 15:53:31 GMT  
		Size: 968.3 KB (968314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0861e10c690483650a5c5b80a34f8062cf1c4991e5345d85cd0d17d56bb1ff`  
		Last Modified: Tue, 07 Jan 2025 15:53:31 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af048d98bf3c8a90c18d2c3115fa12f26188777034752c35b1c625281aa269c`  
		Last Modified: Tue, 07 Jan 2025 15:53:31 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:05f1fd51a10262cb513a2306d8841324bbae54348258bc3f43dc9b5b74169b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2181612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db7690f86ec1f52b5f920e134a8d3e09182d744d83472f8a9b493fe2b6b199b`

```dockerfile
```

-	Layers:
	-	`sha256:c5501f10e797650932c9d815eb6f1a7b7f7dd5eb6ccf761df1bdcb2feca404f7`  
		Last Modified: Tue, 07 Jan 2025 15:53:31 GMT  
		Size: 2.2 MB (2150654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a21f1b92bdd5f3c0b884d4d21f5cd59fe82cc515164be3abafa0e6508e82ae3`  
		Last Modified: Tue, 07 Jan 2025 15:53:30 GMT  
		Size: 31.0 KB (30958 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:lts`

```console
$ docker pull composer@sha256:2f5608ca4dea71332fc362322d8fd9faf8af679f884cd8c0809b57e783bb55fb
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

### `composer:lts` - linux; amd64

```console
$ docker pull composer@sha256:d89f1b39885bc5fd7230772d2ba753b001ef77858206d86fe7653a5680d977d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74179967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064c853712449649329197128dea85b249dbfa8e337bdc0f28f7a46a70915f3c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
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
	-	`sha256:885cabab622328790c1b0fe029609594a60d1dde6f69dcb4cea95adfd92d8126`  
		Last Modified: Wed, 08 Jan 2025 18:23:12 GMT  
		Size: 31.9 MB (31896321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414b7b71fdb41abcb4ae1fc4672f9a1c2e0378ffde03fd52bb6bab21e8fc0792`  
		Last Modified: Wed, 08 Jan 2025 18:23:11 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c787e639b4347e933e17af93685e9678f55ff58887a31392ccd4a7b6c4a04fd`  
		Last Modified: Wed, 08 Jan 2025 18:23:12 GMT  
		Size: 819.6 KB (819649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5cba85e675197ad1c4e50d53e4e0729a14dc95038bda054e5abd51eb1af7f2`  
		Last Modified: Wed, 08 Jan 2025 18:23:08 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f05948628ca40470c501b71b53616ed24606f1134506db08b96b27478c89d57`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:e45b9734520af4d27ebe5f162005179af56ea71821d5ec27960ba2d08c1e90c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb109ab9b1f9daa010442645eef215da3ca8046f484ec0f4c357aa364ee6301`

```dockerfile
```

-	Layers:
	-	`sha256:70d3ef1a5d9e813dea628ac0de8bccdbd4c7beaaf5646fbbfcc90e33ffe4a213`  
		Last Modified: Wed, 08 Jan 2025 18:23:12 GMT  
		Size: 2.2 MB (2158953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e154f1263271bc00c1114370b3fea24edcdfb2143040971529c027ea928cde8f`  
		Last Modified: Wed, 08 Jan 2025 18:23:11 GMT  
		Size: 30.7 KB (30654 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v6

```console
$ docker pull composer@sha256:62780dfe0305b97d5c117da225f07089b5f049f9e28e63e77dace73ce3be1059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70737552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5123431ad90ce368101720cec24a22a396bc0b32e9dad29788f08e0848902788`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
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
	-	`sha256:8bfbe143528e86684282cbfd298570a16342fbf7feefa882f4ff4af7f9116796`  
		Last Modified: Tue, 07 Jan 2025 18:31:35 GMT  
		Size: 30.6 MB (30640654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a227f011e7035c2e61babbdbf90fea0a1845e1422312eda1608ae428cda1dead`  
		Last Modified: Tue, 07 Jan 2025 18:31:34 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a7f50a6a0b2d3bba683179b2ca8b3a6f06bfd4c4cd4cf9d7d8019fa8fdc3ed`  
		Last Modified: Tue, 07 Jan 2025 18:31:34 GMT  
		Size: 819.0 KB (819000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386d76b9a3e1f7c21e5a182c9d58502bc43af53578e67a16921add85659a9209`  
		Last Modified: Thu, 12 Dec 2024 19:27:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ff64dd899232449206800cffdc8869754b2909076233d33db06ddad1cdf3ab`  
		Last Modified: Tue, 07 Jan 2025 18:31:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:aca531ab11f0ec9cd82cb1561c71c8fd21045677fc332e31a991ebb62624fbb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84182bcd4d0972d594520d297fcd46e7f9820bc7b675b07ec118cd18508497c3`

```dockerfile
```

-	Layers:
	-	`sha256:7c740e78fe3d45b7ccc1292fa27e081e2817856eec1830607b76f5dd8f647675`  
		Last Modified: Tue, 07 Jan 2025 18:31:34 GMT  
		Size: 30.5 KB (30533 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v7

```console
$ docker pull composer@sha256:fe2e86e7783ca0794c0e26052f87bea5460a351e4a0a71f6c97dc848bab0f1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68763325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f539003ccc43375331a561f2fbddb2a1c4347d8a4e39b08b7e306c26e9374198`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
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
	-	`sha256:0a2bf4fd23a4343e4fa39d2a63004ae4de297973415bc8809c9c56b1097caf8a`  
		Last Modified: Tue, 07 Jan 2025 18:37:42 GMT  
		Size: 30.2 MB (30150038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89da730f1c4439581b1de7342d8be357e2ea326296a6c567ba8c4e6dad0fd87e`  
		Last Modified: Tue, 07 Jan 2025 18:37:41 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2866b818ce1acc063a90c52ca34e07472abd17b06d97f5cb4c3b576311e570d`  
		Last Modified: Tue, 07 Jan 2025 18:37:41 GMT  
		Size: 810.2 KB (810155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337e1d50532e32becc0231c4249de3f6ef29b28253de129ee5a78b1a3fc79e81`  
		Last Modified: Tue, 07 Jan 2025 18:37:41 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee87b2232654b3eb1c36caa684f8ccff56b1e37b1330e3f3c15eaa721a6e05f`  
		Last Modified: Tue, 07 Jan 2025 18:37:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:21398388870c6e26950eafb43b83ba774b8b8576a75dfaf38e50299d51adeb55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2184139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf47be48517aeedaf551be239ec81ba466518ad613e69ee63afb0609f455f15e`

```dockerfile
```

-	Layers:
	-	`sha256:517cce97251c609db3e3991630f2a5bc39f4422390d90007aea3d5ed3ad5fec6`  
		Last Modified: Tue, 07 Jan 2025 18:37:41 GMT  
		Size: 2.2 MB (2153391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10cd029e98742e609faaefa58d1cc5b64bc0ad33f0885eef827514a44f223b6a`  
		Last Modified: Tue, 07 Jan 2025 18:37:40 GMT  
		Size: 30.7 KB (30748 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:c54955436e867221e15e7b0b6889f5ad546095abfc856d42fc9ea083c93f4902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74159791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eeca8fe0441bd3d71568d6b9999e2f1547544b1965debcddb86d0e4c5ec555d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
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
	-	`sha256:a0c59331d5588d1a35cef8b8de8c57f9df896f2230d66caa4f7510c076bcf10b`  
		Last Modified: Tue, 07 Jan 2025 16:07:22 GMT  
		Size: 32.0 MB (32004107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bc1dca7afc6e7b778ae0cc6c16db02fce566edf2e75b273bdf7c721ed764f9`  
		Last Modified: Tue, 07 Jan 2025 16:07:20 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22f76f0fb079af01086f273a0c5a2c90c6164c8dbc6e94f26d29d86d625562a`  
		Last Modified: Tue, 07 Jan 2025 16:07:20 GMT  
		Size: 819.2 KB (819160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57850e2434c721ad60730949863bf3ad1b08b34367f7a9fdb22370cf20bdd38e`  
		Last Modified: Tue, 07 Jan 2025 16:07:20 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c75b7341e5165a5268e0c27fa486773dd4d578f8919cfa4c33ee9c14d9497c8`  
		Last Modified: Tue, 07 Jan 2025 16:07:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:f8584b8f4d9369dc4f295402f8bda2017d3d8ab6343c5e4c15fa5f4f08a4e026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2183990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e713c1a2820caba98c9259e6a458d567f77191e4c6f01048a3990b203ea3f25a`

```dockerfile
```

-	Layers:
	-	`sha256:970567e858d48b4a4723956c594efaf4f894e54a2b7405a843923594a74cb803`  
		Last Modified: Tue, 07 Jan 2025 16:07:20 GMT  
		Size: 2.2 MB (2153215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c32f616e654e513df779676341c65f0f8ac0b9e2d8294c69943a2bac10c00ec1`  
		Last Modified: Tue, 07 Jan 2025 16:07:20 GMT  
		Size: 30.8 KB (30775 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; 386

```console
$ docker pull composer@sha256:d867c413160a359efb52c69460a4144a03ed8da734699116540299d612e7d018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54060154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af7e0c10eb7fb91b52fac4ece18f3eb62e4fa7689fed39c9599452fa129c511`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
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
	-	`sha256:8fbd829e35763ceb6dccaeefd114a90e3d353e0f2279bccdbc61d7043db2f3e0`  
		Last Modified: Wed, 08 Jan 2025 18:23:10 GMT  
		Size: 11.4 MB (11421298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7325392e6f571d6d6c867ba9360a98dcc25489b73ee76ef7f4cc6be5d7ec8b54`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a0ea9fde932ff4d6706282639ee6dcdc1ae58fb69c70f200d3eee65b8b57de`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 798.5 KB (798487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7ec707154224ea90d37a709253436de0e37251a0637392c70bf27f2cb93575`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f05948628ca40470c501b71b53616ed24606f1134506db08b96b27478c89d57`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:823a8609ebdc375e23fb68610b629e4d12c9313888f35a65ff975e30357de379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.2 KB (459234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d52cd67e2526878d1fcb3f39879549b565d84f150023a1c5a1bd68b5d13895e`

```dockerfile
```

-	Layers:
	-	`sha256:82ddaf0eaae76863fc7e561ba10ace7088adc1d9708f67a614019ef59ed65e5e`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 428.6 KB (428611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a65dfea9228e3d77283a647e8033aacefe3c50b6e536857822aa4f78535aef91`  
		Last Modified: Wed, 08 Jan 2025 18:23:09 GMT  
		Size: 30.6 KB (30623 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; ppc64le

```console
$ docker pull composer@sha256:c681ce6660052c5b5706c1ce94de91ea805ffbf6198a9ba4320ef50e6207ee1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76217995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da8839e93bd725eaa611e5287b8bd89ee9893ad4d64f8d23856437c058fb27b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
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
	-	`sha256:26aa0c6396d98d67cdb7cff725afeddc08a54386e1d5e68f922a402f902d2924`  
		Last Modified: Thu, 09 Jan 2025 01:29:00 GMT  
		Size: 32.9 MB (32943089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ed0b4e6953a4bbe30d89c2f6151304b7cf0496993f171b508a19e501ebb706`  
		Last Modified: Thu, 09 Jan 2025 01:28:58 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aecade86a1d865576697d59d99d03142a53200eb9c65045733a02e9b371744a`  
		Last Modified: Thu, 09 Jan 2025 01:28:59 GMT  
		Size: 826.3 KB (826320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067fa511713f9b64b2eac2a775759f1e7b8a632164010b713826377a5acfdf6d`  
		Last Modified: Thu, 09 Jan 2025 01:28:58 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77067613a67569ad413a6087f23c33cefaa8aa92e74697b79800bc235fdf47ee`  
		Last Modified: Thu, 09 Jan 2025 01:28:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:a71bca1eab6c6d29e8714a2d1acc82c79ba777a3230a2f23b64b5c624c0ddb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b08a6c05ed8f0e3db87d40776586c32e466c4025c5f194ebd53603ad5de5cd`

```dockerfile
```

-	Layers:
	-	`sha256:a1e946c2ab4d20f8dc014e4a54b3a6e9a94a86970d63c6b3775d03e328ed6da7`  
		Last Modified: Thu, 09 Jan 2025 01:28:58 GMT  
		Size: 2.2 MB (2157510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e080193b6d487618c1b09ea228820916ecde56ee3afde851edf6def943baa7d`  
		Last Modified: Thu, 09 Jan 2025 01:28:58 GMT  
		Size: 30.7 KB (30696 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; riscv64

```console
$ docker pull composer@sha256:5d855d116a11db35f6a8ad2be607bd8e5624eeb94475fe41679a24f4c4ffb032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73581176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebda7e74b0a3215d8eff4cfa7e70191f9eb54e0c56c6fffe7736ce1a76bff18`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
		Size: 3.4 MB (3445761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9c93fa8ac38e6017fe5251627d738084239fbab425319ead8bdece897e493`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe2d3ee20829a994ce6548409e985a58c1c6ec2238583410057ae0e6dfe95a1`  
		Last Modified: Fri, 20 Dec 2024 22:27:49 GMT  
		Size: 13.6 MB (13580504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a67918c3771135e7a2b16f42498ea94d985dc8f6407db3a3ee60e1e3e9373b`  
		Last Modified: Fri, 20 Dec 2024 22:27:47 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e567d61ea86fdc5c63b8ce75eb88bcda35c75049600dcb0b112964a7da3ac42f`  
		Last Modified: Fri, 20 Dec 2024 22:27:50 GMT  
		Size: 20.8 MB (20797397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263bcc5a009f020e39d0e162f139f8f8433852481d7368c9cde637ffd9f841e5`  
		Last Modified: Fri, 20 Dec 2024 22:27:47 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9ec8a613ce316b270ee3a65ed2d2041d6579061f1f8b0d0725f55b6f9e84fc`  
		Last Modified: Fri, 20 Dec 2024 22:27:48 GMT  
		Size: 19.9 KB (19885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe21f96e7307414693b828f2173bcaa37df5cd8443ce028ad761b4e69270f7`  
		Last Modified: Sat, 21 Dec 2024 14:35:27 GMT  
		Size: 31.0 MB (31000197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4008aa8424d8743580595dbf0803a9aa275eb20020eb2e8e47ed5c19aeeee6bf`  
		Last Modified: Sat, 21 Dec 2024 14:35:22 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57af59a23156600be33dba882bdf1a5e0021aa8a1a596a9177787f956d9b64a`  
		Last Modified: Sat, 21 Dec 2024 14:35:22 GMT  
		Size: 1.4 MB (1378532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081edbee53f3a9cf4b66b37a4a382dd412be359ae83d996f3486c00c340e622a`  
		Last Modified: Sat, 21 Dec 2024 14:35:22 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e210a352cd82457991648bd5510e28668c55ff115eda1b4507fe4a714e7923f0`  
		Last Modified: Sat, 21 Dec 2024 14:35:23 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:a2c7dca9aa5fcbd3871b7007b05cf47f7f2d2b368637d8b079f0f646f5bfd5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c674cd3c5293d3d1f3dd5b6b93134ecbce04724ce045e1deed00622bf30caee`

```dockerfile
```

-	Layers:
	-	`sha256:242ae2fc62a46e8658c8d4da70cdfd90b2baddb6395de29095bf372fb27560a9`  
		Last Modified: Sat, 21 Dec 2024 14:35:22 GMT  
		Size: 2.2 MB (2157752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec0097a6dfb339beb94a49db7f8925afc8a4499c4aa2a06fb1902165559b3486`  
		Last Modified: Sat, 21 Dec 2024 14:35:21 GMT  
		Size: 30.7 KB (30699 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; s390x

```console
$ docker pull composer@sha256:d02c93f2bed1ac62f9a10175194a7d1c3ff57a7ab1da35b5d838c9ce8f57dc8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74474247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9396e94046532c68a1e2079f216151ef6b76b0c87971d41b90a863dcf11e38`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
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
	-	`sha256:3f63ed19a544e5e26e1152afe55e1e34f250a8fe3982b62ef0754513377c899c`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 31.7 MB (31674581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59aadc194319e2220294cf3ff3a08addb3a57ecf676d4fb858a0ff81e0bd6c8d`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeeba213ea4c8637e0fc7148dff1096de416af696a8f3d82c2d9a49ce3c7cc28`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 822.3 KB (822308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7854c8ea0ad3ff17f9fe195d3544e9cbd21ff3acba3640292dfe831f78d84`  
		Last Modified: Tue, 07 Jan 2025 15:51:41 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b983b49b572dbb392ac1688ac9013e00106127d063358984a7bb4cbfa8b94f`  
		Last Modified: Tue, 07 Jan 2025 15:51:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:6200dcf316dc362bab148966c3916a70a89158c498ad90838c65184d3c53df57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2181014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39799757773592a16da8bcbdb6995319725643d812b9d58541e8f5b510740554`

```dockerfile
```

-	Layers:
	-	`sha256:7a722c2780e1984cf94a58e3060e8f419a5e9faca1e4ba334aee11586a18bcaf`  
		Last Modified: Tue, 07 Jan 2025 15:51:40 GMT  
		Size: 2.2 MB (2150360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee0ca95466511e3dc9b15d260a86ebe0dc6036ed10cdb8212e7ac94f0614e79`  
		Last Modified: Tue, 07 Jan 2025 15:51:40 GMT  
		Size: 30.7 KB (30654 bytes)  
		MIME: application/vnd.in-toto+json
