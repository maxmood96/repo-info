<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `composer`

-	[`composer:1`](#composer1)
-	[`composer:1.10`](#composer110)
-	[`composer:1.10.27`](#composer11027)
-	[`composer:2`](#composer2)
-	[`composer:2.2`](#composer22)
-	[`composer:2.2.25`](#composer2225)
-	[`composer:2.8`](#composer28)
-	[`composer:2.8.12`](#composer2812)
-	[`composer:latest`](#composerlatest)

## `composer:1`

```console
$ docker pull composer@sha256:99e3617363b7ac15816ef0a18a0ec36c50afad5a15bd96eb5ad9f4338b15e3ac
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
$ docker pull composer@sha256:21b92ee4888f73150b1395f5fbacc250326b35bc40c7a706134915efc5d4902d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76113131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd30692117240b5f5559653f46089e535e2e4b7337615e1d44e454428cba725c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:6edff2afe33934322951d9852a7173f4acf1fd7d82862dd04effc6aa7706f9a5`  
		Last Modified: Wed, 08 Oct 2025 23:38:27 GMT  
		Size: 33.9 MB (33926546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3381cec6a9c10e2bfd5a7edd8beb7927d20ace55a743bfad8eb63b3e14df4a32`  
		Last Modified: Wed, 08 Oct 2025 23:38:24 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7050997d253252815459918ade05f07515ce3df0b19411222ceae484c8465036`  
		Last Modified: Wed, 08 Oct 2025 23:38:24 GMT  
		Size: 1.3 MB (1254965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b83d55eb27b4efd5b5bdcf66dfb0219ef4bf9b63307e8682f18ea2102db698`  
		Last Modified: Wed, 08 Oct 2025 23:38:24 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ee9fe0c3413897e0e82404a21c14464223ced79c1a14a98921138a77a4d4d4`  
		Last Modified: Wed, 08 Oct 2025 23:38:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:82baa414e20ff60c4efced77836a2ce6a05f3b9d292e354670b197df42403c2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3382609f160e7e87d5548608855d2ab8ffe9b296cdc40bbdc8238f0f76af0ab`

```dockerfile
```

-	Layers:
	-	`sha256:1ec05eba9f5589e7c959a576ba33900afe2fe355f3575ef3259f0ca6c56a6005`  
		Last Modified: Thu, 09 Oct 2025 01:13:39 GMT  
		Size: 2.2 MB (2171917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2121f269f237373af8b898a8f4abaeeadfa376b03dcb8124b426520375469456`  
		Last Modified: Thu, 09 Oct 2025 01:13:40 GMT  
		Size: 31.4 KB (31359 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v6

```console
$ docker pull composer@sha256:fd3c22ea9c3e6b8e8742c88b08ceb03da4e7c265f7171fa025de30b30dc61804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73226594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2031a8124687aaf4d8f5fb338a4981b7b27a18900742b84aa1593eee9d975a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:e9f167349fd9df823e2096861b1b95483b1ba5057c8defbfb34900edb05b9775`  
		Last Modified: Wed, 08 Oct 2025 23:01:37 GMT  
		Size: 33.8 MB (33785117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e68099f81bec9fa6a8d90ab833e44f06b803fcdd4a540e9ba1b4c43a62cf639`  
		Last Modified: Wed, 08 Oct 2025 23:01:35 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b1f3495b9c3f465c2de48015f4e3ad51c92871cfd6e1943e62892dd9327e52`  
		Last Modified: Wed, 08 Oct 2025 23:01:35 GMT  
		Size: 736.0 KB (736001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7dbf391d862c0d383819437f8ca9ab49fab5c6e4f8d8545db4334d13f561c8`  
		Last Modified: Wed, 08 Oct 2025 23:01:35 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba793248964df420e5053e74410d6762d6d767238c51bbde6bcb5e216585765`  
		Last Modified: Wed, 08 Oct 2025 23:01:35 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:87dc005135571c008b70e07bd82cf8783bb8f2aab2034502696f20246a43f009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 KB (31239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b725a401b356868e26fb1dc4b6ceed6e5fea0eae76f82a84fee33caae5bc9296`

```dockerfile
```

-	Layers:
	-	`sha256:63d4d36057fa997ed1ae00ff03000b451c49a67022f7e3b838b0babb00ddb195`  
		Last Modified: Thu, 09 Oct 2025 01:13:44 GMT  
		Size: 31.2 KB (31239 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v7

```console
$ docker pull composer@sha256:66e89f5f91755c0e8149a5b34c88c495e617e81a3d4efd111e1788d43e8fc8ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70461183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9e57bee90e41324d2e6afb78b3783b5acc90e99646066b31cb2cbc05b0212f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:8b1c4f99874201655f66d007b405db57135965bc0117a375e0021fb0b36cceb5`  
		Last Modified: Wed, 08 Oct 2025 23:18:28 GMT  
		Size: 32.1 MB (32064308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa4d5e9b411f22a1a3dac1708e3cc58dd4de967bb39c323acf7a702189fef40`  
		Last Modified: Wed, 08 Oct 2025 23:18:26 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae6d4e9257e34c882a61217e4d67f21176a986b3fcb1f5a900b62a595457124`  
		Last Modified: Wed, 08 Oct 2025 23:18:26 GMT  
		Size: 1.2 MB (1172171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c457bd4dafb6d043fce8ae383b47122c1940f638894597c1b3aea547da69b4d`  
		Last Modified: Wed, 08 Oct 2025 23:18:26 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1f7ad0ed399d99de3171f69578b0655fd0943ed7c627525cf342d5f8555d34`  
		Last Modified: Wed, 08 Oct 2025 23:18:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:d0b92bd8c393d1d808d65e0e6ea7f1794780c177f1e4e92b1359101dd60deeca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b07d96a6acbf0782b46243c2ad3ed852ae9fed8a9a176b25dc9d1728292bf43`

```dockerfile
```

-	Layers:
	-	`sha256:1483e279024e17cd2783eae4cbfadad38b2f1dd368ba276b4a91c9c5c9ddf201`  
		Last Modified: Thu, 09 Oct 2025 01:13:48 GMT  
		Size: 2.2 MB (2172233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c533c8ca68e0d07cfdf6ae7c6dde5052d5d6c503f67f51de0305e00e5ca5f71`  
		Last Modified: Thu, 09 Oct 2025 01:13:48 GMT  
		Size: 31.5 KB (31457 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:8cc883dccd9d8feafabfa985a8703a320686efa6381cca79d6afb76bb1235a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75558895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764ec6a1b7e40228823f262a101acd818d305a72163baa01cad75a6687b413ba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:905a6cbf20fd9e08366ec4dd9285a6b608b610cdcfa77657ff8c77324e0dde72`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 34.0 MB (34005570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a34113696a520aa300a755e94cffa631e8034e082adf6168e3994b6f8a01e87`  
		Last Modified: Wed, 08 Oct 2025 22:58:09 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82617ad15aa2b66ece6a37535fa9a646458cd791c99d0589758d875e123ea110`  
		Last Modified: Wed, 08 Oct 2025 22:58:09 GMT  
		Size: 735.3 KB (735334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97bd5ef7c342495e8288ea76118738839f7d46ad0bb9bb585f481495464e102e`  
		Last Modified: Wed, 08 Oct 2025 22:58:09 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09e5fe2ac68c491bdb1d5b906af7ffe9be50572ec7752a869939aa825566154`  
		Last Modified: Wed, 08 Oct 2025 22:58:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:16e469f77f02c48bdb30e04af858b5b8583c996c66e3866f378529eac3be988c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f50477b0742caa7a9bb70f785da5d74e3248104c5939d4616aea59c993b7b6`

```dockerfile
```

-	Layers:
	-	`sha256:c4c6eeecda81b1394bd9bd5eaf1927c4aaf7466f77ccfa981b7815779c82a174`  
		Last Modified: Thu, 09 Oct 2025 01:13:52 GMT  
		Size: 2.2 MB (2172057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e561416962abcb2861c4e43b48a375ec541dd3862a1b57635e8964e25f99a1`  
		Last Modified: Thu, 09 Oct 2025 01:13:53 GMT  
		Size: 31.5 KB (31478 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; 386

```console
$ docker pull composer@sha256:22ea29f1efdd0dcd4e7653522ff70c796c120b76f14387c9034ce4856c88d775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76522262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432b042faed64152cae973ec41c958a5c6dbd7eff22539cb063403cd2ab313e4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:8f96afe96888927c07d63c423ff083dfb4af121a839a70e6cc0675df0e62f67b`  
		Last Modified: Wed, 08 Oct 2025 22:20:19 GMT  
		Size: 34.4 MB (34438902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b670de3121211b4089ba1eab69ef85c7498b281113539ea79e34909a81fc0686`  
		Last Modified: Wed, 08 Oct 2025 22:20:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23012e0ddb03e495cc0fc1bf3afb58e6cf2b55ffaa0bd4cfc78ba5141f004847`  
		Last Modified: Wed, 08 Oct 2025 22:20:17 GMT  
		Size: 747.2 KB (747250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118ac6aa02eb078bda58b5e880a5ebd476e2cda73dfdd4a067362437da886083`  
		Last Modified: Wed, 08 Oct 2025 22:20:17 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884bb5ad9aba61105ca250836bfd1d5ab5844af88b36bd31619f4f877f5bc158`  
		Last Modified: Wed, 08 Oct 2025 22:20:16 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:43fbb3a7f04ac89a79d4fa954f2cf353cd962a8d688ff3b6fde60b15c18ea510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f58cc542db9b14bb82969c2cdf4d39f60e282a9af4707a78904eb801bddd985a`

```dockerfile
```

-	Layers:
	-	`sha256:18556ee951361e1187cadad2a29ffc63bce2429772d592c9b47ab844bc86503b`  
		Last Modified: Thu, 09 Oct 2025 01:13:57 GMT  
		Size: 2.2 MB (2171705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ee73b1f9aa10864bbc8ecbae01b2c5bf963a437467749fb6515aa11e85b563`  
		Last Modified: Thu, 09 Oct 2025 01:13:57 GMT  
		Size: 31.3 KB (31325 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; ppc64le

```console
$ docker pull composer@sha256:c416ed5f2f8f09d0d8c8509687056bf37e8b3718596697fbed8a00c3e4065b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77896026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421fb4400f520cd72bf4465036f9a6731090631cfa151a9551bab73aae6f894c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:fcc750c69d5845f08b366fcf588ae6020f2df3bb4a5bf650228778ed0a9fde88`  
		Last Modified: Thu, 09 Oct 2025 05:56:38 GMT  
		Size: 35.2 MB (35236113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0dfb7c3cec49e9a0f110d7243d5d9fcce6cda1e117d0fbaa88cf3efa29c872`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e998d65137a46960c8059678b90d25f2a77f449a0a44119c66532fb5f8f5f167`  
		Last Modified: Thu, 09 Oct 2025 05:58:29 GMT  
		Size: 742.4 KB (742403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bbd5ac72432bf87c159972d572f1739ff678e1655f14b21a99093998fd43d6`  
		Last Modified: Thu, 09 Oct 2025 05:58:28 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613c29e6ca40c556a4aff54c2d10401c5b940ff3589615473258dc824be6c8a7`  
		Last Modified: Thu, 09 Oct 2025 05:58:29 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:cc26fff65a01f87cc64e9dd846f89d74ede5e3fb236ceb922614f9b0d3ec66c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd282959229cefd4bf2b7fb6fe6845ed8ac4c32dccfae157f390827fa39dbd0`

```dockerfile
```

-	Layers:
	-	`sha256:838bd75f5cf1f94b6e95ac7430ca27b98b1d63fa61e73b27146412e7a6e5de7a`  
		Last Modified: Thu, 09 Oct 2025 07:13:32 GMT  
		Size: 2.2 MB (2170474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a93244b3dab0b93c5c1716ec6b34e6802d86a7fdcf329c4692361dfafe96a62c`  
		Last Modified: Thu, 09 Oct 2025 07:13:33 GMT  
		Size: 31.4 KB (31398 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; riscv64

```console
$ docker pull composer@sha256:5834b8a06dd2f81ae2c169854effbc2b8336519e90d7c722f3db6611afdb7b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75333432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eeb5db528c743775226b64fa3b9451e4a57c816341d6e205104173bebebe55a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Mon, 13 Oct 2025 01:16:18 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c293b040c7a67eeac13c53a522990f19f36e1b39939bdc55cbe7dbeefa2c82`  
		Last Modified: Sat, 11 Oct 2025 17:48:45 GMT  
		Size: 3.6 MB (3594168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4153c5fef55d21621d3f69b9fd9a25c43bda1995413d8f4dcacf545b0d8d2a0b`  
		Last Modified: Sat, 11 Oct 2025 04:03:27 GMT  
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
	-	`sha256:8086d8efed09e7df388724484c2e24d189528f19da5afbedccd3e94622be6286`  
		Last Modified: Fri, 26 Sep 2025 22:46:25 GMT  
		Size: 31.1 MB (31111630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8335f4e7521dca07f16a62141ea1763295dac7280d3dd4e5fa1c649800e6a8`  
		Last Modified: Fri, 26 Sep 2025 22:46:22 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c842a34fa1d9690db9332bd3beb0983d75c520c53cfd24ca466e480e63be13`  
		Last Modified: Fri, 26 Sep 2025 22:51:59 GMT  
		Size: 1.4 MB (1421784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9d9f316b641510b3dddaffdfdffb99bcd13619ee2f3d1c95b2eb668cc525de`  
		Last Modified: Fri, 26 Sep 2025 22:51:59 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795607a884d53ab6b443ba473d95bc8bd3a314d5276ff35757627b11425490a2`  
		Last Modified: Fri, 26 Sep 2025 22:51:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:9c46c9bd674c3488e9774a1a052a6536e35b985b8871e7e44b9cf886c0979214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2197529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:197f62f3697c9f4c48b694876c4acbd9ed323acb88b6eda9012a5a56e97bd57a`

```dockerfile
```

-	Layers:
	-	`sha256:e14e1a41de524181b1584d8cedd2f375567a3aba837c6967cc6bc0d13f7b8e56`  
		Last Modified: Sat, 27 Sep 2025 01:13:36 GMT  
		Size: 2.2 MB (2166128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7b075e7fbbfe30f9c8c7bd47b6b5acfff48406c26f3e6df20c584db55870fab`  
		Last Modified: Sat, 27 Sep 2025 01:13:37 GMT  
		Size: 31.4 KB (31401 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; s390x

```console
$ docker pull composer@sha256:26408d88508f4f7cb19ba479978f4635e80dda89d665193eb42b55542d2c7436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73603507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab568f50e9d7c0a246ea3ce15cee6528be46cd6c3de8aa431a198a14fc3e1de3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:4e5219110d4f3e49ef43fca54c828f77476de52c08e27b490e23eb605777c4b8`  
		Last Modified: Thu, 09 Oct 2025 08:07:33 GMT  
		Size: 31.8 MB (31841368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b912ad325203381f087b9b20815b78a8a62274eb021560b83d0a130fdadc83`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac75b7b2c1b476a0d8ac230e1cad683ecc1f114063aa0796f12aadff29c06016`  
		Last Modified: Thu, 09 Oct 2025 08:08:19 GMT  
		Size: 738.8 KB (738767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f88ca6b9cba1d8764e1fbb641ddabc71c96313aeadc6777def8c92ccee0034b`  
		Last Modified: Thu, 09 Oct 2025 08:08:18 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59816c81f47bedb9d02df0b3667757e756dcc9c91c55f7de36e3950801f70e3`  
		Last Modified: Thu, 09 Oct 2025 08:08:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:dcc172465f65803e48404584778813d264b0cfc5d742098907b3205dd0e72c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042c9a57e84213e673789fa653a3acb6c9523aefd01dbe422f34091aafa0ab8b`

```dockerfile
```

-	Layers:
	-	`sha256:c117b90ca2d5a440239665a540ac370fdaa697c6c0ffbc7a917938590f1bfeed`  
		Last Modified: Thu, 09 Oct 2025 10:13:50 GMT  
		Size: 2.2 MB (2168529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63c0794e0dece018c8ee4067cba4af5748868b849f1ab33f153e325bb35f7d26`  
		Last Modified: Thu, 09 Oct 2025 10:13:51 GMT  
		Size: 31.4 KB (31356 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10`

```console
$ docker pull composer@sha256:99e3617363b7ac15816ef0a18a0ec36c50afad5a15bd96eb5ad9f4338b15e3ac
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
$ docker pull composer@sha256:21b92ee4888f73150b1395f5fbacc250326b35bc40c7a706134915efc5d4902d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76113131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd30692117240b5f5559653f46089e535e2e4b7337615e1d44e454428cba725c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:6edff2afe33934322951d9852a7173f4acf1fd7d82862dd04effc6aa7706f9a5`  
		Last Modified: Wed, 08 Oct 2025 23:38:27 GMT  
		Size: 33.9 MB (33926546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3381cec6a9c10e2bfd5a7edd8beb7927d20ace55a743bfad8eb63b3e14df4a32`  
		Last Modified: Wed, 08 Oct 2025 23:38:24 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7050997d253252815459918ade05f07515ce3df0b19411222ceae484c8465036`  
		Last Modified: Wed, 08 Oct 2025 23:38:24 GMT  
		Size: 1.3 MB (1254965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b83d55eb27b4efd5b5bdcf66dfb0219ef4bf9b63307e8682f18ea2102db698`  
		Last Modified: Wed, 08 Oct 2025 23:38:24 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ee9fe0c3413897e0e82404a21c14464223ced79c1a14a98921138a77a4d4d4`  
		Last Modified: Wed, 08 Oct 2025 23:38:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:82baa414e20ff60c4efced77836a2ce6a05f3b9d292e354670b197df42403c2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3382609f160e7e87d5548608855d2ab8ffe9b296cdc40bbdc8238f0f76af0ab`

```dockerfile
```

-	Layers:
	-	`sha256:1ec05eba9f5589e7c959a576ba33900afe2fe355f3575ef3259f0ca6c56a6005`  
		Last Modified: Thu, 09 Oct 2025 01:13:39 GMT  
		Size: 2.2 MB (2171917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2121f269f237373af8b898a8f4abaeeadfa376b03dcb8124b426520375469456`  
		Last Modified: Thu, 09 Oct 2025 01:13:40 GMT  
		Size: 31.4 KB (31359 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v6

```console
$ docker pull composer@sha256:fd3c22ea9c3e6b8e8742c88b08ceb03da4e7c265f7171fa025de30b30dc61804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73226594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2031a8124687aaf4d8f5fb338a4981b7b27a18900742b84aa1593eee9d975a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:e9f167349fd9df823e2096861b1b95483b1ba5057c8defbfb34900edb05b9775`  
		Last Modified: Wed, 08 Oct 2025 23:01:37 GMT  
		Size: 33.8 MB (33785117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e68099f81bec9fa6a8d90ab833e44f06b803fcdd4a540e9ba1b4c43a62cf639`  
		Last Modified: Wed, 08 Oct 2025 23:01:35 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b1f3495b9c3f465c2de48015f4e3ad51c92871cfd6e1943e62892dd9327e52`  
		Last Modified: Wed, 08 Oct 2025 23:01:35 GMT  
		Size: 736.0 KB (736001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7dbf391d862c0d383819437f8ca9ab49fab5c6e4f8d8545db4334d13f561c8`  
		Last Modified: Wed, 08 Oct 2025 23:01:35 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba793248964df420e5053e74410d6762d6d767238c51bbde6bcb5e216585765`  
		Last Modified: Wed, 08 Oct 2025 23:01:35 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:87dc005135571c008b70e07bd82cf8783bb8f2aab2034502696f20246a43f009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 KB (31239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b725a401b356868e26fb1dc4b6ceed6e5fea0eae76f82a84fee33caae5bc9296`

```dockerfile
```

-	Layers:
	-	`sha256:63d4d36057fa997ed1ae00ff03000b451c49a67022f7e3b838b0babb00ddb195`  
		Last Modified: Thu, 09 Oct 2025 01:13:44 GMT  
		Size: 31.2 KB (31239 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v7

```console
$ docker pull composer@sha256:66e89f5f91755c0e8149a5b34c88c495e617e81a3d4efd111e1788d43e8fc8ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70461183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9e57bee90e41324d2e6afb78b3783b5acc90e99646066b31cb2cbc05b0212f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:8b1c4f99874201655f66d007b405db57135965bc0117a375e0021fb0b36cceb5`  
		Last Modified: Wed, 08 Oct 2025 23:18:28 GMT  
		Size: 32.1 MB (32064308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa4d5e9b411f22a1a3dac1708e3cc58dd4de967bb39c323acf7a702189fef40`  
		Last Modified: Wed, 08 Oct 2025 23:18:26 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae6d4e9257e34c882a61217e4d67f21176a986b3fcb1f5a900b62a595457124`  
		Last Modified: Wed, 08 Oct 2025 23:18:26 GMT  
		Size: 1.2 MB (1172171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c457bd4dafb6d043fce8ae383b47122c1940f638894597c1b3aea547da69b4d`  
		Last Modified: Wed, 08 Oct 2025 23:18:26 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1f7ad0ed399d99de3171f69578b0655fd0943ed7c627525cf342d5f8555d34`  
		Last Modified: Wed, 08 Oct 2025 23:18:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:d0b92bd8c393d1d808d65e0e6ea7f1794780c177f1e4e92b1359101dd60deeca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b07d96a6acbf0782b46243c2ad3ed852ae9fed8a9a176b25dc9d1728292bf43`

```dockerfile
```

-	Layers:
	-	`sha256:1483e279024e17cd2783eae4cbfadad38b2f1dd368ba276b4a91c9c5c9ddf201`  
		Last Modified: Thu, 09 Oct 2025 01:13:48 GMT  
		Size: 2.2 MB (2172233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c533c8ca68e0d07cfdf6ae7c6dde5052d5d6c503f67f51de0305e00e5ca5f71`  
		Last Modified: Thu, 09 Oct 2025 01:13:48 GMT  
		Size: 31.5 KB (31457 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:8cc883dccd9d8feafabfa985a8703a320686efa6381cca79d6afb76bb1235a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75558895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764ec6a1b7e40228823f262a101acd818d305a72163baa01cad75a6687b413ba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:905a6cbf20fd9e08366ec4dd9285a6b608b610cdcfa77657ff8c77324e0dde72`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 34.0 MB (34005570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a34113696a520aa300a755e94cffa631e8034e082adf6168e3994b6f8a01e87`  
		Last Modified: Wed, 08 Oct 2025 22:58:09 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82617ad15aa2b66ece6a37535fa9a646458cd791c99d0589758d875e123ea110`  
		Last Modified: Wed, 08 Oct 2025 22:58:09 GMT  
		Size: 735.3 KB (735334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97bd5ef7c342495e8288ea76118738839f7d46ad0bb9bb585f481495464e102e`  
		Last Modified: Wed, 08 Oct 2025 22:58:09 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09e5fe2ac68c491bdb1d5b906af7ffe9be50572ec7752a869939aa825566154`  
		Last Modified: Wed, 08 Oct 2025 22:58:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:16e469f77f02c48bdb30e04af858b5b8583c996c66e3866f378529eac3be988c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f50477b0742caa7a9bb70f785da5d74e3248104c5939d4616aea59c993b7b6`

```dockerfile
```

-	Layers:
	-	`sha256:c4c6eeecda81b1394bd9bd5eaf1927c4aaf7466f77ccfa981b7815779c82a174`  
		Last Modified: Thu, 09 Oct 2025 01:13:52 GMT  
		Size: 2.2 MB (2172057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e561416962abcb2861c4e43b48a375ec541dd3862a1b57635e8964e25f99a1`  
		Last Modified: Thu, 09 Oct 2025 01:13:53 GMT  
		Size: 31.5 KB (31478 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; 386

```console
$ docker pull composer@sha256:22ea29f1efdd0dcd4e7653522ff70c796c120b76f14387c9034ce4856c88d775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76522262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432b042faed64152cae973ec41c958a5c6dbd7eff22539cb063403cd2ab313e4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:8f96afe96888927c07d63c423ff083dfb4af121a839a70e6cc0675df0e62f67b`  
		Last Modified: Wed, 08 Oct 2025 22:20:19 GMT  
		Size: 34.4 MB (34438902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b670de3121211b4089ba1eab69ef85c7498b281113539ea79e34909a81fc0686`  
		Last Modified: Wed, 08 Oct 2025 22:20:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23012e0ddb03e495cc0fc1bf3afb58e6cf2b55ffaa0bd4cfc78ba5141f004847`  
		Last Modified: Wed, 08 Oct 2025 22:20:17 GMT  
		Size: 747.2 KB (747250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118ac6aa02eb078bda58b5e880a5ebd476e2cda73dfdd4a067362437da886083`  
		Last Modified: Wed, 08 Oct 2025 22:20:17 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884bb5ad9aba61105ca250836bfd1d5ab5844af88b36bd31619f4f877f5bc158`  
		Last Modified: Wed, 08 Oct 2025 22:20:16 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:43fbb3a7f04ac89a79d4fa954f2cf353cd962a8d688ff3b6fde60b15c18ea510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f58cc542db9b14bb82969c2cdf4d39f60e282a9af4707a78904eb801bddd985a`

```dockerfile
```

-	Layers:
	-	`sha256:18556ee951361e1187cadad2a29ffc63bce2429772d592c9b47ab844bc86503b`  
		Last Modified: Thu, 09 Oct 2025 01:13:57 GMT  
		Size: 2.2 MB (2171705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ee73b1f9aa10864bbc8ecbae01b2c5bf963a437467749fb6515aa11e85b563`  
		Last Modified: Thu, 09 Oct 2025 01:13:57 GMT  
		Size: 31.3 KB (31325 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; ppc64le

```console
$ docker pull composer@sha256:c416ed5f2f8f09d0d8c8509687056bf37e8b3718596697fbed8a00c3e4065b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77896026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421fb4400f520cd72bf4465036f9a6731090631cfa151a9551bab73aae6f894c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:fcc750c69d5845f08b366fcf588ae6020f2df3bb4a5bf650228778ed0a9fde88`  
		Last Modified: Thu, 09 Oct 2025 05:56:38 GMT  
		Size: 35.2 MB (35236113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0dfb7c3cec49e9a0f110d7243d5d9fcce6cda1e117d0fbaa88cf3efa29c872`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e998d65137a46960c8059678b90d25f2a77f449a0a44119c66532fb5f8f5f167`  
		Last Modified: Thu, 09 Oct 2025 05:58:29 GMT  
		Size: 742.4 KB (742403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bbd5ac72432bf87c159972d572f1739ff678e1655f14b21a99093998fd43d6`  
		Last Modified: Thu, 09 Oct 2025 05:58:28 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613c29e6ca40c556a4aff54c2d10401c5b940ff3589615473258dc824be6c8a7`  
		Last Modified: Thu, 09 Oct 2025 05:58:29 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:cc26fff65a01f87cc64e9dd846f89d74ede5e3fb236ceb922614f9b0d3ec66c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd282959229cefd4bf2b7fb6fe6845ed8ac4c32dccfae157f390827fa39dbd0`

```dockerfile
```

-	Layers:
	-	`sha256:838bd75f5cf1f94b6e95ac7430ca27b98b1d63fa61e73b27146412e7a6e5de7a`  
		Last Modified: Thu, 09 Oct 2025 07:13:32 GMT  
		Size: 2.2 MB (2170474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a93244b3dab0b93c5c1716ec6b34e6802d86a7fdcf329c4692361dfafe96a62c`  
		Last Modified: Thu, 09 Oct 2025 07:13:33 GMT  
		Size: 31.4 KB (31398 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; riscv64

```console
$ docker pull composer@sha256:5834b8a06dd2f81ae2c169854effbc2b8336519e90d7c722f3db6611afdb7b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75333432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eeb5db528c743775226b64fa3b9451e4a57c816341d6e205104173bebebe55a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Mon, 13 Oct 2025 01:16:18 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c293b040c7a67eeac13c53a522990f19f36e1b39939bdc55cbe7dbeefa2c82`  
		Last Modified: Sat, 11 Oct 2025 17:48:45 GMT  
		Size: 3.6 MB (3594168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4153c5fef55d21621d3f69b9fd9a25c43bda1995413d8f4dcacf545b0d8d2a0b`  
		Last Modified: Sat, 11 Oct 2025 04:03:27 GMT  
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
	-	`sha256:8086d8efed09e7df388724484c2e24d189528f19da5afbedccd3e94622be6286`  
		Last Modified: Fri, 26 Sep 2025 22:46:25 GMT  
		Size: 31.1 MB (31111630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8335f4e7521dca07f16a62141ea1763295dac7280d3dd4e5fa1c649800e6a8`  
		Last Modified: Fri, 26 Sep 2025 22:46:22 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c842a34fa1d9690db9332bd3beb0983d75c520c53cfd24ca466e480e63be13`  
		Last Modified: Fri, 26 Sep 2025 22:51:59 GMT  
		Size: 1.4 MB (1421784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9d9f316b641510b3dddaffdfdffb99bcd13619ee2f3d1c95b2eb668cc525de`  
		Last Modified: Fri, 26 Sep 2025 22:51:59 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795607a884d53ab6b443ba473d95bc8bd3a314d5276ff35757627b11425490a2`  
		Last Modified: Fri, 26 Sep 2025 22:51:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:9c46c9bd674c3488e9774a1a052a6536e35b985b8871e7e44b9cf886c0979214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2197529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:197f62f3697c9f4c48b694876c4acbd9ed323acb88b6eda9012a5a56e97bd57a`

```dockerfile
```

-	Layers:
	-	`sha256:e14e1a41de524181b1584d8cedd2f375567a3aba837c6967cc6bc0d13f7b8e56`  
		Last Modified: Sat, 27 Sep 2025 01:13:36 GMT  
		Size: 2.2 MB (2166128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7b075e7fbbfe30f9c8c7bd47b6b5acfff48406c26f3e6df20c584db55870fab`  
		Last Modified: Sat, 27 Sep 2025 01:13:37 GMT  
		Size: 31.4 KB (31401 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; s390x

```console
$ docker pull composer@sha256:26408d88508f4f7cb19ba479978f4635e80dda89d665193eb42b55542d2c7436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73603507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab568f50e9d7c0a246ea3ce15cee6528be46cd6c3de8aa431a198a14fc3e1de3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:4e5219110d4f3e49ef43fca54c828f77476de52c08e27b490e23eb605777c4b8`  
		Last Modified: Thu, 09 Oct 2025 08:07:33 GMT  
		Size: 31.8 MB (31841368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b912ad325203381f087b9b20815b78a8a62274eb021560b83d0a130fdadc83`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac75b7b2c1b476a0d8ac230e1cad683ecc1f114063aa0796f12aadff29c06016`  
		Last Modified: Thu, 09 Oct 2025 08:08:19 GMT  
		Size: 738.8 KB (738767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f88ca6b9cba1d8764e1fbb641ddabc71c96313aeadc6777def8c92ccee0034b`  
		Last Modified: Thu, 09 Oct 2025 08:08:18 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59816c81f47bedb9d02df0b3667757e756dcc9c91c55f7de36e3950801f70e3`  
		Last Modified: Thu, 09 Oct 2025 08:08:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:dcc172465f65803e48404584778813d264b0cfc5d742098907b3205dd0e72c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042c9a57e84213e673789fa653a3acb6c9523aefd01dbe422f34091aafa0ab8b`

```dockerfile
```

-	Layers:
	-	`sha256:c117b90ca2d5a440239665a540ac370fdaa697c6c0ffbc7a917938590f1bfeed`  
		Last Modified: Thu, 09 Oct 2025 10:13:50 GMT  
		Size: 2.2 MB (2168529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63c0794e0dece018c8ee4067cba4af5748868b849f1ab33f153e325bb35f7d26`  
		Last Modified: Thu, 09 Oct 2025 10:13:51 GMT  
		Size: 31.4 KB (31356 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10.27`

```console
$ docker pull composer@sha256:99e3617363b7ac15816ef0a18a0ec36c50afad5a15bd96eb5ad9f4338b15e3ac
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
$ docker pull composer@sha256:21b92ee4888f73150b1395f5fbacc250326b35bc40c7a706134915efc5d4902d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76113131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd30692117240b5f5559653f46089e535e2e4b7337615e1d44e454428cba725c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:6edff2afe33934322951d9852a7173f4acf1fd7d82862dd04effc6aa7706f9a5`  
		Last Modified: Wed, 08 Oct 2025 23:38:27 GMT  
		Size: 33.9 MB (33926546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3381cec6a9c10e2bfd5a7edd8beb7927d20ace55a743bfad8eb63b3e14df4a32`  
		Last Modified: Wed, 08 Oct 2025 23:38:24 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7050997d253252815459918ade05f07515ce3df0b19411222ceae484c8465036`  
		Last Modified: Wed, 08 Oct 2025 23:38:24 GMT  
		Size: 1.3 MB (1254965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b83d55eb27b4efd5b5bdcf66dfb0219ef4bf9b63307e8682f18ea2102db698`  
		Last Modified: Wed, 08 Oct 2025 23:38:24 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ee9fe0c3413897e0e82404a21c14464223ced79c1a14a98921138a77a4d4d4`  
		Last Modified: Wed, 08 Oct 2025 23:38:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:82baa414e20ff60c4efced77836a2ce6a05f3b9d292e354670b197df42403c2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3382609f160e7e87d5548608855d2ab8ffe9b296cdc40bbdc8238f0f76af0ab`

```dockerfile
```

-	Layers:
	-	`sha256:1ec05eba9f5589e7c959a576ba33900afe2fe355f3575ef3259f0ca6c56a6005`  
		Last Modified: Thu, 09 Oct 2025 01:13:39 GMT  
		Size: 2.2 MB (2171917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2121f269f237373af8b898a8f4abaeeadfa376b03dcb8124b426520375469456`  
		Last Modified: Thu, 09 Oct 2025 01:13:40 GMT  
		Size: 31.4 KB (31359 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v6

```console
$ docker pull composer@sha256:fd3c22ea9c3e6b8e8742c88b08ceb03da4e7c265f7171fa025de30b30dc61804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73226594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2031a8124687aaf4d8f5fb338a4981b7b27a18900742b84aa1593eee9d975a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:e9f167349fd9df823e2096861b1b95483b1ba5057c8defbfb34900edb05b9775`  
		Last Modified: Wed, 08 Oct 2025 23:01:37 GMT  
		Size: 33.8 MB (33785117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e68099f81bec9fa6a8d90ab833e44f06b803fcdd4a540e9ba1b4c43a62cf639`  
		Last Modified: Wed, 08 Oct 2025 23:01:35 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b1f3495b9c3f465c2de48015f4e3ad51c92871cfd6e1943e62892dd9327e52`  
		Last Modified: Wed, 08 Oct 2025 23:01:35 GMT  
		Size: 736.0 KB (736001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7dbf391d862c0d383819437f8ca9ab49fab5c6e4f8d8545db4334d13f561c8`  
		Last Modified: Wed, 08 Oct 2025 23:01:35 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba793248964df420e5053e74410d6762d6d767238c51bbde6bcb5e216585765`  
		Last Modified: Wed, 08 Oct 2025 23:01:35 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:87dc005135571c008b70e07bd82cf8783bb8f2aab2034502696f20246a43f009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 KB (31239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b725a401b356868e26fb1dc4b6ceed6e5fea0eae76f82a84fee33caae5bc9296`

```dockerfile
```

-	Layers:
	-	`sha256:63d4d36057fa997ed1ae00ff03000b451c49a67022f7e3b838b0babb00ddb195`  
		Last Modified: Thu, 09 Oct 2025 01:13:44 GMT  
		Size: 31.2 KB (31239 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v7

```console
$ docker pull composer@sha256:66e89f5f91755c0e8149a5b34c88c495e617e81a3d4efd111e1788d43e8fc8ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70461183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9e57bee90e41324d2e6afb78b3783b5acc90e99646066b31cb2cbc05b0212f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:8b1c4f99874201655f66d007b405db57135965bc0117a375e0021fb0b36cceb5`  
		Last Modified: Wed, 08 Oct 2025 23:18:28 GMT  
		Size: 32.1 MB (32064308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa4d5e9b411f22a1a3dac1708e3cc58dd4de967bb39c323acf7a702189fef40`  
		Last Modified: Wed, 08 Oct 2025 23:18:26 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae6d4e9257e34c882a61217e4d67f21176a986b3fcb1f5a900b62a595457124`  
		Last Modified: Wed, 08 Oct 2025 23:18:26 GMT  
		Size: 1.2 MB (1172171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c457bd4dafb6d043fce8ae383b47122c1940f638894597c1b3aea547da69b4d`  
		Last Modified: Wed, 08 Oct 2025 23:18:26 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1f7ad0ed399d99de3171f69578b0655fd0943ed7c627525cf342d5f8555d34`  
		Last Modified: Wed, 08 Oct 2025 23:18:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:d0b92bd8c393d1d808d65e0e6ea7f1794780c177f1e4e92b1359101dd60deeca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b07d96a6acbf0782b46243c2ad3ed852ae9fed8a9a176b25dc9d1728292bf43`

```dockerfile
```

-	Layers:
	-	`sha256:1483e279024e17cd2783eae4cbfadad38b2f1dd368ba276b4a91c9c5c9ddf201`  
		Last Modified: Thu, 09 Oct 2025 01:13:48 GMT  
		Size: 2.2 MB (2172233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c533c8ca68e0d07cfdf6ae7c6dde5052d5d6c503f67f51de0305e00e5ca5f71`  
		Last Modified: Thu, 09 Oct 2025 01:13:48 GMT  
		Size: 31.5 KB (31457 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:8cc883dccd9d8feafabfa985a8703a320686efa6381cca79d6afb76bb1235a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75558895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764ec6a1b7e40228823f262a101acd818d305a72163baa01cad75a6687b413ba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:905a6cbf20fd9e08366ec4dd9285a6b608b610cdcfa77657ff8c77324e0dde72`  
		Last Modified: Wed, 08 Oct 2025 22:58:11 GMT  
		Size: 34.0 MB (34005570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a34113696a520aa300a755e94cffa631e8034e082adf6168e3994b6f8a01e87`  
		Last Modified: Wed, 08 Oct 2025 22:58:09 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82617ad15aa2b66ece6a37535fa9a646458cd791c99d0589758d875e123ea110`  
		Last Modified: Wed, 08 Oct 2025 22:58:09 GMT  
		Size: 735.3 KB (735334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97bd5ef7c342495e8288ea76118738839f7d46ad0bb9bb585f481495464e102e`  
		Last Modified: Wed, 08 Oct 2025 22:58:09 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09e5fe2ac68c491bdb1d5b906af7ffe9be50572ec7752a869939aa825566154`  
		Last Modified: Wed, 08 Oct 2025 22:58:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:16e469f77f02c48bdb30e04af858b5b8583c996c66e3866f378529eac3be988c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f50477b0742caa7a9bb70f785da5d74e3248104c5939d4616aea59c993b7b6`

```dockerfile
```

-	Layers:
	-	`sha256:c4c6eeecda81b1394bd9bd5eaf1927c4aaf7466f77ccfa981b7815779c82a174`  
		Last Modified: Thu, 09 Oct 2025 01:13:52 GMT  
		Size: 2.2 MB (2172057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e561416962abcb2861c4e43b48a375ec541dd3862a1b57635e8964e25f99a1`  
		Last Modified: Thu, 09 Oct 2025 01:13:53 GMT  
		Size: 31.5 KB (31478 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; 386

```console
$ docker pull composer@sha256:22ea29f1efdd0dcd4e7653522ff70c796c120b76f14387c9034ce4856c88d775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76522262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432b042faed64152cae973ec41c958a5c6dbd7eff22539cb063403cd2ab313e4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:8f96afe96888927c07d63c423ff083dfb4af121a839a70e6cc0675df0e62f67b`  
		Last Modified: Wed, 08 Oct 2025 22:20:19 GMT  
		Size: 34.4 MB (34438902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b670de3121211b4089ba1eab69ef85c7498b281113539ea79e34909a81fc0686`  
		Last Modified: Wed, 08 Oct 2025 22:20:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23012e0ddb03e495cc0fc1bf3afb58e6cf2b55ffaa0bd4cfc78ba5141f004847`  
		Last Modified: Wed, 08 Oct 2025 22:20:17 GMT  
		Size: 747.2 KB (747250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118ac6aa02eb078bda58b5e880a5ebd476e2cda73dfdd4a067362437da886083`  
		Last Modified: Wed, 08 Oct 2025 22:20:17 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884bb5ad9aba61105ca250836bfd1d5ab5844af88b36bd31619f4f877f5bc158`  
		Last Modified: Wed, 08 Oct 2025 22:20:16 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:43fbb3a7f04ac89a79d4fa954f2cf353cd962a8d688ff3b6fde60b15c18ea510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f58cc542db9b14bb82969c2cdf4d39f60e282a9af4707a78904eb801bddd985a`

```dockerfile
```

-	Layers:
	-	`sha256:18556ee951361e1187cadad2a29ffc63bce2429772d592c9b47ab844bc86503b`  
		Last Modified: Thu, 09 Oct 2025 01:13:57 GMT  
		Size: 2.2 MB (2171705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ee73b1f9aa10864bbc8ecbae01b2c5bf963a437467749fb6515aa11e85b563`  
		Last Modified: Thu, 09 Oct 2025 01:13:57 GMT  
		Size: 31.3 KB (31325 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; ppc64le

```console
$ docker pull composer@sha256:c416ed5f2f8f09d0d8c8509687056bf37e8b3718596697fbed8a00c3e4065b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77896026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421fb4400f520cd72bf4465036f9a6731090631cfa151a9551bab73aae6f894c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:fcc750c69d5845f08b366fcf588ae6020f2df3bb4a5bf650228778ed0a9fde88`  
		Last Modified: Thu, 09 Oct 2025 05:56:38 GMT  
		Size: 35.2 MB (35236113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0dfb7c3cec49e9a0f110d7243d5d9fcce6cda1e117d0fbaa88cf3efa29c872`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e998d65137a46960c8059678b90d25f2a77f449a0a44119c66532fb5f8f5f167`  
		Last Modified: Thu, 09 Oct 2025 05:58:29 GMT  
		Size: 742.4 KB (742403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bbd5ac72432bf87c159972d572f1739ff678e1655f14b21a99093998fd43d6`  
		Last Modified: Thu, 09 Oct 2025 05:58:28 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613c29e6ca40c556a4aff54c2d10401c5b940ff3589615473258dc824be6c8a7`  
		Last Modified: Thu, 09 Oct 2025 05:58:29 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:cc26fff65a01f87cc64e9dd846f89d74ede5e3fb236ceb922614f9b0d3ec66c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd282959229cefd4bf2b7fb6fe6845ed8ac4c32dccfae157f390827fa39dbd0`

```dockerfile
```

-	Layers:
	-	`sha256:838bd75f5cf1f94b6e95ac7430ca27b98b1d63fa61e73b27146412e7a6e5de7a`  
		Last Modified: Thu, 09 Oct 2025 07:13:32 GMT  
		Size: 2.2 MB (2170474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a93244b3dab0b93c5c1716ec6b34e6802d86a7fdcf329c4692361dfafe96a62c`  
		Last Modified: Thu, 09 Oct 2025 07:13:33 GMT  
		Size: 31.4 KB (31398 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; riscv64

```console
$ docker pull composer@sha256:5834b8a06dd2f81ae2c169854effbc2b8336519e90d7c722f3db6611afdb7b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75333432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eeb5db528c743775226b64fa3b9451e4a57c816341d6e205104173bebebe55a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Mon, 13 Oct 2025 01:16:18 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c293b040c7a67eeac13c53a522990f19f36e1b39939bdc55cbe7dbeefa2c82`  
		Last Modified: Sat, 11 Oct 2025 17:48:45 GMT  
		Size: 3.6 MB (3594168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4153c5fef55d21621d3f69b9fd9a25c43bda1995413d8f4dcacf545b0d8d2a0b`  
		Last Modified: Sat, 11 Oct 2025 04:03:27 GMT  
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
	-	`sha256:8086d8efed09e7df388724484c2e24d189528f19da5afbedccd3e94622be6286`  
		Last Modified: Fri, 26 Sep 2025 22:46:25 GMT  
		Size: 31.1 MB (31111630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8335f4e7521dca07f16a62141ea1763295dac7280d3dd4e5fa1c649800e6a8`  
		Last Modified: Fri, 26 Sep 2025 22:46:22 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c842a34fa1d9690db9332bd3beb0983d75c520c53cfd24ca466e480e63be13`  
		Last Modified: Fri, 26 Sep 2025 22:51:59 GMT  
		Size: 1.4 MB (1421784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9d9f316b641510b3dddaffdfdffb99bcd13619ee2f3d1c95b2eb668cc525de`  
		Last Modified: Fri, 26 Sep 2025 22:51:59 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795607a884d53ab6b443ba473d95bc8bd3a314d5276ff35757627b11425490a2`  
		Last Modified: Fri, 26 Sep 2025 22:51:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:9c46c9bd674c3488e9774a1a052a6536e35b985b8871e7e44b9cf886c0979214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2197529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:197f62f3697c9f4c48b694876c4acbd9ed323acb88b6eda9012a5a56e97bd57a`

```dockerfile
```

-	Layers:
	-	`sha256:e14e1a41de524181b1584d8cedd2f375567a3aba837c6967cc6bc0d13f7b8e56`  
		Last Modified: Sat, 27 Sep 2025 01:13:36 GMT  
		Size: 2.2 MB (2166128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7b075e7fbbfe30f9c8c7bd47b6b5acfff48406c26f3e6df20c584db55870fab`  
		Last Modified: Sat, 27 Sep 2025 01:13:37 GMT  
		Size: 31.4 KB (31401 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; s390x

```console
$ docker pull composer@sha256:26408d88508f4f7cb19ba479978f4635e80dda89d665193eb42b55542d2c7436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73603507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab568f50e9d7c0a246ea3ce15cee6528be46cd6c3de8aa431a198a14fc3e1de3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:4e5219110d4f3e49ef43fca54c828f77476de52c08e27b490e23eb605777c4b8`  
		Last Modified: Thu, 09 Oct 2025 08:07:33 GMT  
		Size: 31.8 MB (31841368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b912ad325203381f087b9b20815b78a8a62274eb021560b83d0a130fdadc83`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac75b7b2c1b476a0d8ac230e1cad683ecc1f114063aa0796f12aadff29c06016`  
		Last Modified: Thu, 09 Oct 2025 08:08:19 GMT  
		Size: 738.8 KB (738767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f88ca6b9cba1d8764e1fbb641ddabc71c96313aeadc6777def8c92ccee0034b`  
		Last Modified: Thu, 09 Oct 2025 08:08:18 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59816c81f47bedb9d02df0b3667757e756dcc9c91c55f7de36e3950801f70e3`  
		Last Modified: Thu, 09 Oct 2025 08:08:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:dcc172465f65803e48404584778813d264b0cfc5d742098907b3205dd0e72c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042c9a57e84213e673789fa653a3acb6c9523aefd01dbe422f34091aafa0ab8b`

```dockerfile
```

-	Layers:
	-	`sha256:c117b90ca2d5a440239665a540ac370fdaa697c6c0ffbc7a917938590f1bfeed`  
		Last Modified: Thu, 09 Oct 2025 10:13:50 GMT  
		Size: 2.2 MB (2168529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63c0794e0dece018c8ee4067cba4af5748868b849f1ab33f153e325bb35f7d26`  
		Last Modified: Thu, 09 Oct 2025 10:13:51 GMT  
		Size: 31.4 KB (31356 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2`

```console
$ docker pull composer@sha256:e4580e48611e8f22e3440b1334557c9e8e893f753b05c67237fdddc0ece7d582
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
$ docker pull composer@sha256:e6bb44785d7241c1aa8401c0c180f904995bebaadf6f9ab0bf668457a491b9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76352034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e3260f706ce27b3ab500c309575abca3892b04b5a07ceaafb9149f7d27aa41`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:7432aafef02307143bba29ffd243e3f04304b1807be61bf76435deabbb0758df`  
		Last Modified: Wed, 08 Oct 2025 23:38:28 GMT  
		Size: 33.9 MB (33926475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fad6092b1df4c88e89b597e81d0fefac2f2d75c80ccb72b8568ef4cfcc60d78`  
		Last Modified: Wed, 08 Oct 2025 23:38:25 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e99b1f89065123d11766026ed9b0d5a4a432302f861722d06b6e0b6336d903a`  
		Last Modified: Wed, 08 Oct 2025 23:38:26 GMT  
		Size: 1.5 MB (1493930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c332e00e89e1a6519f970796f145c0c3295bfb3fb24cc9b4c725c1c0ab01b826`  
		Last Modified: Wed, 08 Oct 2025 23:38:25 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ee9fe0c3413897e0e82404a21c14464223ced79c1a14a98921138a77a4d4d4`  
		Last Modified: Wed, 08 Oct 2025 23:38:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:44c03ff785c4abd36dd0e62f469464c68cd3b8aa13e791dde3dacc7871457790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470ade5e6c4e5efc01c54cdd69d2f92988b06f0b6fed3dc5b90ec5988d929c0a`

```dockerfile
```

-	Layers:
	-	`sha256:420794ff931b66a1f588d676f15552e7364d671939d998e4787c704848a0ea41`  
		Last Modified: Thu, 09 Oct 2025 01:14:09 GMT  
		Size: 2.2 MB (2173415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46b9bc78f2b6aee9e13b019bb0ff3219a5ae25f616cc3cd9b919bf541495a99a`  
		Last Modified: Thu, 09 Oct 2025 01:14:10 GMT  
		Size: 31.7 KB (31658 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v6

```console
$ docker pull composer@sha256:066dfe9368db60c15722653809215179f53cac794ba97cef6d487bb82dfe3ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73464661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150b2ae5648792c8d1a90962e1f1d10f9f5e42b021ac09d403149674f613a897`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:55907e0a0d97a2fff768eed8119a26c68c46291f0356b9f6ab5f15fe11271ebc`  
		Last Modified: Wed, 08 Oct 2025 23:01:24 GMT  
		Size: 33.8 MB (33785137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf44481a6a4a1aac1f5296d10701bdcc2237fcb40ff9425f0de42521c83f839`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c57d6da6f51151ceefa7e8854b8cc35a96ff7c22c0c6de2e86d259b25c9f46`  
		Last Modified: Wed, 08 Oct 2025 23:01:19 GMT  
		Size: 974.0 KB (974037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf78ceeb6dbde8bea48099903a49ed8724c508d216eb8645fc3886903d78efa`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64b1528a9bd520ff23f1ee943c82b6cf59e607a6c36efbcad71899bba19342a`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:ab35ff3471d6f3380d681c65ace2105523b82f138fda910b80b62c3aa181babd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bdf6b5f6ea337235e0adc51c29b36742904baca5d57ac631593b92a8f09604e`

```dockerfile
```

-	Layers:
	-	`sha256:bd9b70b7db28b1b594f5cfa9063ffda6bccaeb4d6ee0921954a02d963dee7573`  
		Last Modified: Thu, 09 Oct 2025 01:14:14 GMT  
		Size: 31.5 KB (31546 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v7

```console
$ docker pull composer@sha256:f41c01ccc01d54af8efc65b7cb9c60a563a6d75524452e6ef9f9c5747e37f51d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70699465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8853953912a39c4f8989eb4936d769995cc08387f0e61090ccc4e6203dc0abf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:1a4af95259bd581f451256ef02f27d6be391c232301f29ea529603ad3209f1f8`  
		Last Modified: Wed, 08 Oct 2025 23:18:11 GMT  
		Size: 32.1 MB (32064307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5218dbe1eddcee4c0851b467212efa963d76151fab105a661669a1e473252b6`  
		Last Modified: Wed, 08 Oct 2025 23:18:09 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fa5ae6c85d8e6af4f100ad64720ae2fd1887ee49e1361990a4813c044f7a5a`  
		Last Modified: Wed, 08 Oct 2025 23:18:09 GMT  
		Size: 1.4 MB (1410445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de89c304165cc7fd6eb4dadc1639306a17257d22ef64304b82f6a0cce143ac84`  
		Last Modified: Wed, 08 Oct 2025 23:18:09 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae5885f9e785d81ab2aa2b6f4a6dce2eb1077ae2da80c3d3b48c6bbf3f2bb16`  
		Last Modified: Wed, 08 Oct 2025 23:18:09 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:1e45776555ba2f3c429d83ffdd848f561c27999b8b2c4bc9813269c33919b9fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a60bf3cfebd70398e8685f8915c0ec275260be9ee167ede378ce12c11e337d7`

```dockerfile
```

-	Layers:
	-	`sha256:984a2a4532ab17eaec3230b94cc85da6a8ec12e3247a7860adc974a24acfb6da`  
		Last Modified: Thu, 09 Oct 2025 01:14:17 GMT  
		Size: 2.2 MB (2173739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa77d58ef12adc720694b933df0185e829a31f2f2f2860096ecf5c683470a86f`  
		Last Modified: Thu, 09 Oct 2025 01:14:18 GMT  
		Size: 31.8 KB (31764 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:231213badba64061194379e913485a9376a14c8753f4d84135e6c9c48ad8d7f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75797731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720bb2065653fbaa53ef45f166d9ae880e1d8eeaa01af447b63b069f661c9362`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:05be2f2fe0c6d3539b2824695cf4df7385787688403ea67197511f9ad0640164`  
		Last Modified: Wed, 08 Oct 2025 22:58:05 GMT  
		Size: 34.0 MB (34006042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e5ee166c845bc9ce53ceaed767d0a11dd333b51b991a682e9688df2e657b24`  
		Last Modified: Wed, 08 Oct 2025 22:58:02 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360bbfda074695914273a729635701189c213b7eb6953dcccfc9e6c7bf8f84a5`  
		Last Modified: Wed, 08 Oct 2025 22:58:02 GMT  
		Size: 973.7 KB (973687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887dadf5f97131ade60fafdb5d7f3eea6b1a69c8bc4f2f18af3fc51b7459e2df`  
		Last Modified: Wed, 08 Oct 2025 22:58:02 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c5722929998f97764e8d53d060ab6ac850d94e87c95696425f951da684a723`  
		Last Modified: Wed, 08 Oct 2025 22:58:02 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:96005ecb1b0ae7afd570fc18f2ae00d10c34ab5e9610f2a92f727131f7ea4436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2b5abb2a73ccc3ae0c6d16384a9f2b4b77c83e761228cf38cca359171a6ad2`

```dockerfile
```

-	Layers:
	-	`sha256:79036f99c9459174eb104dbe582b30aab5871a6d9d37ace423e02cb1530d37ec`  
		Last Modified: Thu, 09 Oct 2025 01:14:21 GMT  
		Size: 2.2 MB (2173567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d46bfe0c45127c0fbc3e70294648b6bd38c23c0c8cbb960f15ea10f0b852562a`  
		Last Modified: Thu, 09 Oct 2025 01:14:22 GMT  
		Size: 31.8 KB (31785 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; 386

```console
$ docker pull composer@sha256:6a3f59afde5da4f6b9391506fd900207e40da42032ccce4c3a7defc62b2462c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76763054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab3a848e4eb86c5bf794f27b4df607df07c420abaefb00cff3ab79b3e1670b6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:7c691ac10422996916b935f8d5d84a5c1ab8afbdf533b13d09eae9b03592b329`  
		Last Modified: Wed, 08 Oct 2025 22:20:22 GMT  
		Size: 34.4 MB (34438942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2545756380f549a9469fc9d4c18d7a997645d3a03b61f261a3fc4a6f9f752a3d`  
		Last Modified: Wed, 08 Oct 2025 22:20:19 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecac885c6f8db12081e32083bf44add84b16502729661d8e96118c0e93337e7`  
		Last Modified: Wed, 08 Oct 2025 22:20:19 GMT  
		Size: 988.0 KB (987992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85182bb7b0422e9ec0aa46ad6183a65962e34466d5ff40358928e6874b4187bc`  
		Last Modified: Wed, 08 Oct 2025 22:20:19 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165978b0065dd1a488f56ceedad46669c24393a8d1ae17c19d77fc28ee618546`  
		Last Modified: Wed, 08 Oct 2025 22:20:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:12faaabda51e751a6d02fa7dea31c5abf6fca15284ce889b619ff8799cdfe0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8881957ec1fd99edd6312721df54f2bb0a9c285c495a54d2f0499aba8bc5c5dc`

```dockerfile
```

-	Layers:
	-	`sha256:a6f1f72a228cb3ba026b803dbe8d58f1cf9fca624240f77fa1ea92c0dc5fe45b`  
		Last Modified: Thu, 09 Oct 2025 01:14:25 GMT  
		Size: 2.2 MB (2173198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c02c6ab31783a75024eee8c58c538d3c2b0825d407c25dbfc27cc45e4d51b30`  
		Last Modified: Thu, 09 Oct 2025 01:14:26 GMT  
		Size: 31.6 KB (31619 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; ppc64le

```console
$ docker pull composer@sha256:7ab8f18c7690e96c4b2c0f98ca57e42441737139252d67b4213aa405cfadaeac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78134372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf72e7a7216358538fcfc4866b29268353f4cb0bf3c5f8cd1e41b25e84f7ca00`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:fcc750c69d5845f08b366fcf588ae6020f2df3bb4a5bf650228778ed0a9fde88`  
		Last Modified: Thu, 09 Oct 2025 05:56:38 GMT  
		Size: 35.2 MB (35236113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0dfb7c3cec49e9a0f110d7243d5d9fcce6cda1e117d0fbaa88cf3efa29c872`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7069cbe03c650f9a782b558ea0c7b6eecf0b31471b705b90de9c985fc0584766`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 980.7 KB (980738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c9dfb2c75ab180a836d1a22b7399619b9d8544f6da246eac510b495b3be44b`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b721d4ea96a39181ad8693b4a8d88fb1845f909261dbf8a034cd63e16768dd99`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:11e9c625adf643934ca29589b3d294bb86103370ed72644386527ce5e5e3df3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05059bd123cffb6b560400732d38d0b86867c15100aba79c3223f2169599616d`

```dockerfile
```

-	Layers:
	-	`sha256:765e6400901500e644e76705796817786597f0dba11e9dca3548e9d777025dae`  
		Last Modified: Thu, 09 Oct 2025 07:13:45 GMT  
		Size: 2.2 MB (2171978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c016add85054c3cb7f2c16c4beb8f8dcc5bffc8fb5f7477d3a53ac2a593a2b85`  
		Last Modified: Thu, 09 Oct 2025 07:13:46 GMT  
		Size: 31.7 KB (31703 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; riscv64

```console
$ docker pull composer@sha256:1d531f6222655c15d072a9f6db8453e8a0bb032e4e4204b83817a74d2738c89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75573351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:926f7969346e4ee5064706f5c4b1f5e399bccdef23b37f9421219bf5d40ee091`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Mon, 13 Oct 2025 01:16:18 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c293b040c7a67eeac13c53a522990f19f36e1b39939bdc55cbe7dbeefa2c82`  
		Last Modified: Sat, 11 Oct 2025 17:48:45 GMT  
		Size: 3.6 MB (3594168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4153c5fef55d21621d3f69b9fd9a25c43bda1995413d8f4dcacf545b0d8d2a0b`  
		Last Modified: Sat, 11 Oct 2025 04:03:27 GMT  
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
	-	`sha256:8086d8efed09e7df388724484c2e24d189528f19da5afbedccd3e94622be6286`  
		Last Modified: Fri, 26 Sep 2025 22:46:25 GMT  
		Size: 31.1 MB (31111630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8335f4e7521dca07f16a62141ea1763295dac7280d3dd4e5fa1c649800e6a8`  
		Last Modified: Fri, 26 Sep 2025 22:46:22 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0ef6f0c64bcbebb0c9adeffe61d4e88a267775c3fca323f5008de3d0e3c947`  
		Last Modified: Fri, 26 Sep 2025 22:46:24 GMT  
		Size: 1.7 MB (1661695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c641845927f76b5160006d48115323bd484a02695abfee72587ac201bd713c0f`  
		Last Modified: Fri, 26 Sep 2025 22:46:21 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54910dead3ff72d407b9dc0093aeac9afbb0f4344d8a1d5419239b27d70dbed5`  
		Last Modified: Fri, 26 Sep 2025 22:41:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:97ec634f4b90008c36a551927bd082c289dfb90e0b33d13a9541c2bf7c2a5d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752d59df2b2f1b5806148eaf6c119d6d985be21308bb75140b4222f049c7e186`

```dockerfile
```

-	Layers:
	-	`sha256:d775e1e4f433aceb275670915f58d34c36f1c0f603c4614c4bca4298fe974ca7`  
		Last Modified: Sat, 27 Sep 2025 01:13:54 GMT  
		Size: 2.2 MB (2167632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4727df4b0fc0a73f9cdbcafaa18cc5beaba3f4d82f0d041afdbee85b219b2bf4`  
		Last Modified: Sat, 27 Sep 2025 01:13:54 GMT  
		Size: 31.7 KB (31706 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; s390x

```console
$ docker pull composer@sha256:05595a53f3002bbd2ba712d1885651be62400b12bd14119f40191f7ae3aef015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73841920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502f45c09a39566b91313513de05acd6f1490e3c336a2c7fd24cac084ddf44dc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:4e5219110d4f3e49ef43fca54c828f77476de52c08e27b490e23eb605777c4b8`  
		Last Modified: Thu, 09 Oct 2025 08:07:33 GMT  
		Size: 31.8 MB (31841368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b912ad325203381f087b9b20815b78a8a62274eb021560b83d0a130fdadc83`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b3763f27effcdcc686b244b630554f55656ad8f43c1abc3b8c8d516d707acd`  
		Last Modified: Thu, 09 Oct 2025 08:07:32 GMT  
		Size: 977.2 KB (977171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e53287954018bc60f63bea842b06e6a30715c50a10e7021e3bad0e4ea802725`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3888304b21042155b83dc5bbfb55b5a62ecaa2401bd061ba507b2c2bfd3fa7d`  
		Last Modified: Thu, 09 Oct 2025 08:07:32 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:a1dd369e5929c064afc2005875b7732ba60490562cbaf47c857940c7b8e6bc0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3ea6c568cc3c0b5074248845f5f93c92bb29da444b2c7be0d1529405b9ec94`

```dockerfile
```

-	Layers:
	-	`sha256:a19650be819af7eb6ff88e79275de8056eac5a7f961dda45b1832e83ffd71794`  
		Last Modified: Thu, 09 Oct 2025 10:14:06 GMT  
		Size: 2.2 MB (2170027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:136b3d48a9b0c3a1e679291b71cf94a1e413d4692a883077c8c2fd3fc32b15cc`  
		Last Modified: Thu, 09 Oct 2025 10:14:07 GMT  
		Size: 31.7 KB (31654 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2`

```console
$ docker pull composer@sha256:7f7036a14f5ad08776321428508bb7685f877d18c9177dee3d23e31b13ae7f96
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
$ docker pull composer@sha256:01983ae4d412045b95dd95e2b27661e360dd713cf403b6d750357fd9ad96d51a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76198116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07bddbd34a7099befc1c8cdab00da8cebc0867ac2e2a06f01ac72f10fd818332`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:f5b796b0586f7e488886b4e11c5301cd26f1f9c10fa478eb14a56afa658444ca`  
		Last Modified: Wed, 08 Oct 2025 23:38:31 GMT  
		Size: 33.9 MB (33926489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3381cec6a9c10e2bfd5a7edd8beb7927d20ace55a743bfad8eb63b3e14df4a32`  
		Last Modified: Wed, 08 Oct 2025 23:38:24 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16705bf0460a56ec767b359f0e5b9c68f52e189f1ed3b2a97e000ae244ecda33`  
		Last Modified: Wed, 08 Oct 2025 23:38:29 GMT  
		Size: 1.3 MB (1339998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c332e00e89e1a6519f970796f145c0c3295bfb3fb24cc9b4c725c1c0ab01b826`  
		Last Modified: Wed, 08 Oct 2025 23:38:25 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d59934fe422570de0809a76cf7486e0b7edd93ffe3fd772c7eb647a50adee9c`  
		Last Modified: Wed, 08 Oct 2025 23:38:29 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:40d279388fd8c5dcb2d756af60e17abeaa242fdc844e728ea529651c0dbf524c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca00fa9112c5c2ecf0e08e04e977b8ec645a0f5621bdf6984a6d56dc24e24ef4`

```dockerfile
```

-	Layers:
	-	`sha256:f1504689e64a7928afb421aba732b09a042f7062a3f019cf905b32c59d874656`  
		Last Modified: Thu, 09 Oct 2025 01:14:29 GMT  
		Size: 2.2 MB (2172821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:881a1e4bc9346d8f39afe05a98653a7e972037535a7238026422e76f8ce756d8`  
		Last Modified: Thu, 09 Oct 2025 01:14:30 GMT  
		Size: 31.1 KB (31055 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v6

```console
$ docker pull composer@sha256:638c5bf4fb8bfa433b384321d06159b9bff3d1636a93bf72597c0d948c312098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73311026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21720c44735e716524b565a518595b11a2bdd55682cc1baf0e2fe6dd4c32d1af`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:68455ef2f43a3fa36a23c2f7c0a5633a0d4d8e43b58781f77303e0a3edfad3e7`  
		Last Modified: Wed, 08 Oct 2025 23:01:27 GMT  
		Size: 33.8 MB (33785178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ad39949f272411da0b5dd780473428399b86521a97d5bfb7caa8fbb3ae2635`  
		Last Modified: Wed, 08 Oct 2025 23:01:23 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b02ec04b81e58430487a3156eabbe58cbc04f4735e9c311f3c5102317a5600c`  
		Last Modified: Wed, 08 Oct 2025 23:01:22 GMT  
		Size: 820.4 KB (820361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d2d3bc39a3fd1303f22c183383b039d4ac568d5c723fca053eecd8b785ca2b`  
		Last Modified: Wed, 08 Oct 2025 23:01:22 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d58e00f99fb07e1e7565bcce8b31fd7ac1d6d14a99b3a9af0743ad74cb62b2`  
		Last Modified: Wed, 08 Oct 2025 23:01:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:7df5e3d18215429808aa154b35398b652bed13b69164bdd3b5dd83e4c34fda19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 KB (30927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fdb48d018a30f41a6bc49a54e1d379f62cf95af30fb3af6c116a8701dcc1431`

```dockerfile
```

-	Layers:
	-	`sha256:f9d011be024c92fca27faaf3f73b40082cbc61b867abfd47fcacf332612545d7`  
		Last Modified: Thu, 09 Oct 2025 01:14:33 GMT  
		Size: 30.9 KB (30927 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v7

```console
$ docker pull composer@sha256:cdb3b1921dab252ed106400a515a4f24051c43b163ab253a8b6739ecbbfd0567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70545677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096c2a5a0dcbee3db2b92bca9db4ba6764ac9b4550b8ecf509f7e216a36acc5c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:6469be76b2480b59ade42061c5f6f2980bf0a1d0888ba971b402086d1a51143e`  
		Last Modified: Wed, 08 Oct 2025 23:18:15 GMT  
		Size: 32.1 MB (32064416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b925355723226ebe1853d3cbe9cda40dd6e84f885b6cc4ea6707f3db74e62cee`  
		Last Modified: Wed, 08 Oct 2025 23:18:12 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9866a8f5318000adfc7b27e6243ee26d77491af717fe06adccac520e5dd25db`  
		Last Modified: Wed, 08 Oct 2025 23:18:13 GMT  
		Size: 1.3 MB (1256547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db0c2c956edfb4d65f19dc0ec09284a8957234931fe83f4ffbe50c881481d2c`  
		Last Modified: Wed, 08 Oct 2025 23:18:12 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae5885f9e785d81ab2aa2b6f4a6dce2eb1077ae2da80c3d3b48c6bbf3f2bb16`  
		Last Modified: Wed, 08 Oct 2025 23:18:09 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:d7bfa454a2e88566f106b93cae2c68209a1c7119280d121a8a2465c52ef1e901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253312d0850be9a92b8e4bec2ee4c8b4abfb575c0ca0c6b203543a71aab91981`

```dockerfile
```

-	Layers:
	-	`sha256:2b150906fbc3b12978edc75f28fbf35254f848b49cac52ff7196cbc16027e1c5`  
		Last Modified: Thu, 09 Oct 2025 01:14:38 GMT  
		Size: 2.2 MB (2173129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c12f5b7d1d3f68a4cba7b94d27af0b25dfb9ae008913b87b58bbaf1074900e0`  
		Last Modified: Thu, 09 Oct 2025 01:14:39 GMT  
		Size: 31.1 KB (31145 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:90d6f81dc470cc08bd1016e0da876b9cafa498df18fe35bc5d5dee5111292a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75643796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f5fb8fac6c985ca27c848183f4f8bf90d199616de84f9e7399278dceefa749`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:ba97844282cae72e5254436e69daeced2dfb8628acb059285022d2182626b365`  
		Last Modified: Wed, 08 Oct 2025 22:58:10 GMT  
		Size: 34.0 MB (34005909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ade816c804912502931df09aa99dd578a1a3f2bcfec02a78712e320bfe2162`  
		Last Modified: Wed, 08 Oct 2025 22:58:06 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa7769370e520c78fed28e828a245579c2661ed7e08ea630d9086e26ab86aac`  
		Last Modified: Wed, 08 Oct 2025 22:58:07 GMT  
		Size: 819.9 KB (819887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa9e4ccc76a45dd5a148aa2f5adcf4930f6a8e784ac95b063f0dd28db3d585a`  
		Last Modified: Wed, 08 Oct 2025 22:58:07 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64fe4eb9dc22ee110077aec8ccfa0bb1a7768a42019fe86fd33b0978a4f69b3`  
		Last Modified: Wed, 08 Oct 2025 22:58:07 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:3fc425f5bb6ecc46a21aad2f3c296da41adaa0a03099b6ff82d85917edbbddaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02871e1d5fc3e015157005a10e726c1237afb29ba2dd9bebab95fdb322640b89`

```dockerfile
```

-	Layers:
	-	`sha256:661cab21f918cc31c757554e5d8cd7702b6bae21d5ac332706d18d97e12f21c8`  
		Last Modified: Thu, 09 Oct 2025 01:14:42 GMT  
		Size: 2.2 MB (2172949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5680c3d6e99418ecc55eff0385bfe2da2cd7f7c15468e7eca1ceec444d3337a2`  
		Last Modified: Thu, 09 Oct 2025 01:14:43 GMT  
		Size: 31.2 KB (31160 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; 386

```console
$ docker pull composer@sha256:275bc5dfce3abe347734c2762514557633d0a6bf7c73e2d6b1c495c9e5aa26c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76609305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796c645fad2ea8d964783b23fb82aedfb209d979c230b00c25604fd831096c12`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:8e5f2af774e5761a1156b63a7ec95c84b3dab008e08a7829523496014e1529f9`  
		Last Modified: Wed, 08 Oct 2025 22:20:17 GMT  
		Size: 34.4 MB (34439092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7eba0d03998e7c05ff8f15fdc7328f5ea1d180cd4436aca79e71d622ad13243`  
		Last Modified: Wed, 08 Oct 2025 22:20:13 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c64f1ca5cf7493dd3ccc28a76979c5ce0b18eed786f6e805642284bb41c768`  
		Last Modified: Wed, 08 Oct 2025 22:20:13 GMT  
		Size: 834.1 KB (834094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d878e8b4cdcf7f66b7884cdf73113fc9e64eb235ec7828bb92c010e477b827e`  
		Last Modified: Wed, 08 Oct 2025 22:20:13 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165978b0065dd1a488f56ceedad46669c24393a8d1ae17c19d77fc28ee618546`  
		Last Modified: Wed, 08 Oct 2025 22:20:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:816444e56181200f8cd6d8158d188ea33fc66af77e7d16820756f503798345b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88ca97d43c7ee6a0792d6eb9b92cdaedc5378819a3f3194f930ba54fbb144fb`

```dockerfile
```

-	Layers:
	-	`sha256:50a705e5d1e5adeb495ef7c327d48c64f431c7d49929f6983489c817106fb1ba`  
		Last Modified: Thu, 09 Oct 2025 01:14:46 GMT  
		Size: 2.2 MB (2172614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7818eef4056a356f4c197d5b6583c3d7767bc31473193323c947d9fba7918179`  
		Last Modified: Thu, 09 Oct 2025 01:14:47 GMT  
		Size: 31.0 KB (31025 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; ppc64le

```console
$ docker pull composer@sha256:267d948789f1e8ba32cd6c41d2d7c2e7f47b99ff376989cfec7d686580aa7db5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77980496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a844aaec8a96a60c5fdc3fbb39e4112ecd4d81e9c30d44f6ab529364b233833`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:fcc750c69d5845f08b366fcf588ae6020f2df3bb4a5bf650228778ed0a9fde88`  
		Last Modified: Thu, 09 Oct 2025 05:56:38 GMT  
		Size: 35.2 MB (35236113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0dfb7c3cec49e9a0f110d7243d5d9fcce6cda1e117d0fbaa88cf3efa29c872`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd01430c925e9bd74329f8c7402b67430ebd0095258f6391d5871865462ab45f`  
		Last Modified: Thu, 09 Oct 2025 05:57:27 GMT  
		Size: 826.9 KB (826863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde899e55f9456e44648f217589cdd59dea02a52ff0559202e0b126d0af8906d`  
		Last Modified: Thu, 09 Oct 2025 05:57:27 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31207cd067ce60336a44109182e5fd7c56a5e49782e4279d6da7042776c941e9`  
		Last Modified: Thu, 09 Oct 2025 05:57:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:0c145e84e5a67b29c59c9876f199eb3cdbe4174dd7a1a19a4e1c2ce05bf15567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5b716ecda48acad1ac905c3c3a5e753f362ed822fb6302eaea2b7fd19b487e`

```dockerfile
```

-	Layers:
	-	`sha256:4c5b326fc1172de42accb95fd5eb0f14dfdaed8af440a3c57ef3550af56628c9`  
		Last Modified: Thu, 09 Oct 2025 07:13:52 GMT  
		Size: 2.2 MB (2171372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91da73e4223b24a5c15a122491267b152c515232ed5594db74a1db1c66cf6138`  
		Last Modified: Thu, 09 Oct 2025 07:13:53 GMT  
		Size: 31.1 KB (31088 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; riscv64

```console
$ docker pull composer@sha256:1687605dca2ecfacc6eaabe67b29dadbcac2de80f74036d0a25cb6c8e9ef4b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75420120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf9d946e52d3cbc2cb39ab7381a7dbc00b45fce4892e3ded5408a9bbe222cd3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Mon, 13 Oct 2025 01:16:18 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c293b040c7a67eeac13c53a522990f19f36e1b39939bdc55cbe7dbeefa2c82`  
		Last Modified: Sat, 11 Oct 2025 17:48:45 GMT  
		Size: 3.6 MB (3594168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4153c5fef55d21621d3f69b9fd9a25c43bda1995413d8f4dcacf545b0d8d2a0b`  
		Last Modified: Sat, 11 Oct 2025 04:03:27 GMT  
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
	-	`sha256:8086d8efed09e7df388724484c2e24d189528f19da5afbedccd3e94622be6286`  
		Last Modified: Fri, 26 Sep 2025 22:46:25 GMT  
		Size: 31.1 MB (31111630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8335f4e7521dca07f16a62141ea1763295dac7280d3dd4e5fa1c649800e6a8`  
		Last Modified: Fri, 26 Sep 2025 22:46:22 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25508299961ce601ee600b85d9a8aaeb951ba1ee475d6d645846406575d68b8c`  
		Last Modified: Fri, 26 Sep 2025 23:12:32 GMT  
		Size: 1.5 MB (1508462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f38cb87c5f84812216d276b6a2bf28a678cf0eb9103c9a791526aa520193b3`  
		Last Modified: Fri, 26 Sep 2025 23:12:52 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7c90ff9a3b5ba67295dc940e66b428e4f26a22621cf14df66a474da160559d`  
		Last Modified: Fri, 26 Sep 2025 23:12:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:2e48b5aa91c01b0f5b50ef7ebaa13dbf58ad173d9c0245b476840265e59e34ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2198117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91860890c1b23e33150a8fe202b5eb5585a267091a1b153cd121d74938dab16a`

```dockerfile
```

-	Layers:
	-	`sha256:106f84a997bad527222954bd0cc4ba4250fa3055fbfa1da69466373d68c26283`  
		Last Modified: Sat, 27 Sep 2025 01:14:14 GMT  
		Size: 2.2 MB (2167026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5773e57aaffa0f6d555871d13ee3f30e278182d3e08122ee3ba1e6a2f3afa5a`  
		Last Modified: Sat, 27 Sep 2025 01:14:15 GMT  
		Size: 31.1 KB (31091 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; s390x

```console
$ docker pull composer@sha256:1613f51eb6e97ebe0e044364b0efc85dee0a15f781e16f868c4da86b8598eca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73688072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa9b56fa76a4083186af4f23bc2142eba8efaa43417ec7a273d17b0b99989c3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:4e5219110d4f3e49ef43fca54c828f77476de52c08e27b490e23eb605777c4b8`  
		Last Modified: Thu, 09 Oct 2025 08:07:33 GMT  
		Size: 31.8 MB (31841368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b912ad325203381f087b9b20815b78a8a62274eb021560b83d0a130fdadc83`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f07303d79642f1f6fb404a8362ed6ae9eddc69cd78578e51091cb475493090`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 823.3 KB (823321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2253d23f87d556dbd49a9d60e5599181400a82b367969b3240ebfec9ed62e295`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055da3fa01337a487323a552025f2674b3813f2ae6ad386ea8de35aa22f6361d`  
		Last Modified: Thu, 09 Oct 2025 08:07:32 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:02d56363e74dcb994393bb3f8b0c29e018e3b0dd1b94972fae8ebe9d0c11c8b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2200485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0215206443c671d7a23d81c0bfa3a6935208899dc688605e06b3892f2ab44551`

```dockerfile
```

-	Layers:
	-	`sha256:561cc1a52b71fb0fa9ed6c468b6f2da2b033fd505534e1a90ec2206346fa38ed`  
		Last Modified: Thu, 09 Oct 2025 10:14:14 GMT  
		Size: 2.2 MB (2169433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5fc09a5ef7167a9597751e5d1f89d97f7ed736db1e45b06e009d9a11fc2aa89`  
		Last Modified: Thu, 09 Oct 2025 10:14:15 GMT  
		Size: 31.1 KB (31052 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2.25`

```console
$ docker pull composer@sha256:7f7036a14f5ad08776321428508bb7685f877d18c9177dee3d23e31b13ae7f96
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
$ docker pull composer@sha256:01983ae4d412045b95dd95e2b27661e360dd713cf403b6d750357fd9ad96d51a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76198116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07bddbd34a7099befc1c8cdab00da8cebc0867ac2e2a06f01ac72f10fd818332`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:f5b796b0586f7e488886b4e11c5301cd26f1f9c10fa478eb14a56afa658444ca`  
		Last Modified: Wed, 08 Oct 2025 23:38:31 GMT  
		Size: 33.9 MB (33926489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3381cec6a9c10e2bfd5a7edd8beb7927d20ace55a743bfad8eb63b3e14df4a32`  
		Last Modified: Wed, 08 Oct 2025 23:38:24 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16705bf0460a56ec767b359f0e5b9c68f52e189f1ed3b2a97e000ae244ecda33`  
		Last Modified: Wed, 08 Oct 2025 23:38:29 GMT  
		Size: 1.3 MB (1339998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c332e00e89e1a6519f970796f145c0c3295bfb3fb24cc9b4c725c1c0ab01b826`  
		Last Modified: Wed, 08 Oct 2025 23:38:25 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d59934fe422570de0809a76cf7486e0b7edd93ffe3fd772c7eb647a50adee9c`  
		Last Modified: Wed, 08 Oct 2025 23:38:29 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:40d279388fd8c5dcb2d756af60e17abeaa242fdc844e728ea529651c0dbf524c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca00fa9112c5c2ecf0e08e04e977b8ec645a0f5621bdf6984a6d56dc24e24ef4`

```dockerfile
```

-	Layers:
	-	`sha256:f1504689e64a7928afb421aba732b09a042f7062a3f019cf905b32c59d874656`  
		Last Modified: Thu, 09 Oct 2025 01:14:29 GMT  
		Size: 2.2 MB (2172821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:881a1e4bc9346d8f39afe05a98653a7e972037535a7238026422e76f8ce756d8`  
		Last Modified: Thu, 09 Oct 2025 01:14:30 GMT  
		Size: 31.1 KB (31055 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm variant v6

```console
$ docker pull composer@sha256:638c5bf4fb8bfa433b384321d06159b9bff3d1636a93bf72597c0d948c312098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73311026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21720c44735e716524b565a518595b11a2bdd55682cc1baf0e2fe6dd4c32d1af`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:68455ef2f43a3fa36a23c2f7c0a5633a0d4d8e43b58781f77303e0a3edfad3e7`  
		Last Modified: Wed, 08 Oct 2025 23:01:27 GMT  
		Size: 33.8 MB (33785178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ad39949f272411da0b5dd780473428399b86521a97d5bfb7caa8fbb3ae2635`  
		Last Modified: Wed, 08 Oct 2025 23:01:23 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b02ec04b81e58430487a3156eabbe58cbc04f4735e9c311f3c5102317a5600c`  
		Last Modified: Wed, 08 Oct 2025 23:01:22 GMT  
		Size: 820.4 KB (820361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d2d3bc39a3fd1303f22c183383b039d4ac568d5c723fca053eecd8b785ca2b`  
		Last Modified: Wed, 08 Oct 2025 23:01:22 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d58e00f99fb07e1e7565bcce8b31fd7ac1d6d14a99b3a9af0743ad74cb62b2`  
		Last Modified: Wed, 08 Oct 2025 23:01:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:7df5e3d18215429808aa154b35398b652bed13b69164bdd3b5dd83e4c34fda19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 KB (30927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fdb48d018a30f41a6bc49a54e1d379f62cf95af30fb3af6c116a8701dcc1431`

```dockerfile
```

-	Layers:
	-	`sha256:f9d011be024c92fca27faaf3f73b40082cbc61b867abfd47fcacf332612545d7`  
		Last Modified: Thu, 09 Oct 2025 01:14:33 GMT  
		Size: 30.9 KB (30927 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm variant v7

```console
$ docker pull composer@sha256:cdb3b1921dab252ed106400a515a4f24051c43b163ab253a8b6739ecbbfd0567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70545677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096c2a5a0dcbee3db2b92bca9db4ba6764ac9b4550b8ecf509f7e216a36acc5c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:6469be76b2480b59ade42061c5f6f2980bf0a1d0888ba971b402086d1a51143e`  
		Last Modified: Wed, 08 Oct 2025 23:18:15 GMT  
		Size: 32.1 MB (32064416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b925355723226ebe1853d3cbe9cda40dd6e84f885b6cc4ea6707f3db74e62cee`  
		Last Modified: Wed, 08 Oct 2025 23:18:12 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9866a8f5318000adfc7b27e6243ee26d77491af717fe06adccac520e5dd25db`  
		Last Modified: Wed, 08 Oct 2025 23:18:13 GMT  
		Size: 1.3 MB (1256547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db0c2c956edfb4d65f19dc0ec09284a8957234931fe83f4ffbe50c881481d2c`  
		Last Modified: Wed, 08 Oct 2025 23:18:12 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae5885f9e785d81ab2aa2b6f4a6dce2eb1077ae2da80c3d3b48c6bbf3f2bb16`  
		Last Modified: Wed, 08 Oct 2025 23:18:09 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:d7bfa454a2e88566f106b93cae2c68209a1c7119280d121a8a2465c52ef1e901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253312d0850be9a92b8e4bec2ee4c8b4abfb575c0ca0c6b203543a71aab91981`

```dockerfile
```

-	Layers:
	-	`sha256:2b150906fbc3b12978edc75f28fbf35254f848b49cac52ff7196cbc16027e1c5`  
		Last Modified: Thu, 09 Oct 2025 01:14:38 GMT  
		Size: 2.2 MB (2173129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c12f5b7d1d3f68a4cba7b94d27af0b25dfb9ae008913b87b58bbaf1074900e0`  
		Last Modified: Thu, 09 Oct 2025 01:14:39 GMT  
		Size: 31.1 KB (31145 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:90d6f81dc470cc08bd1016e0da876b9cafa498df18fe35bc5d5dee5111292a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75643796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f5fb8fac6c985ca27c848183f4f8bf90d199616de84f9e7399278dceefa749`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:ba97844282cae72e5254436e69daeced2dfb8628acb059285022d2182626b365`  
		Last Modified: Wed, 08 Oct 2025 22:58:10 GMT  
		Size: 34.0 MB (34005909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ade816c804912502931df09aa99dd578a1a3f2bcfec02a78712e320bfe2162`  
		Last Modified: Wed, 08 Oct 2025 22:58:06 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa7769370e520c78fed28e828a245579c2661ed7e08ea630d9086e26ab86aac`  
		Last Modified: Wed, 08 Oct 2025 22:58:07 GMT  
		Size: 819.9 KB (819887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa9e4ccc76a45dd5a148aa2f5adcf4930f6a8e784ac95b063f0dd28db3d585a`  
		Last Modified: Wed, 08 Oct 2025 22:58:07 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64fe4eb9dc22ee110077aec8ccfa0bb1a7768a42019fe86fd33b0978a4f69b3`  
		Last Modified: Wed, 08 Oct 2025 22:58:07 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:3fc425f5bb6ecc46a21aad2f3c296da41adaa0a03099b6ff82d85917edbbddaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02871e1d5fc3e015157005a10e726c1237afb29ba2dd9bebab95fdb322640b89`

```dockerfile
```

-	Layers:
	-	`sha256:661cab21f918cc31c757554e5d8cd7702b6bae21d5ac332706d18d97e12f21c8`  
		Last Modified: Thu, 09 Oct 2025 01:14:42 GMT  
		Size: 2.2 MB (2172949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5680c3d6e99418ecc55eff0385bfe2da2cd7f7c15468e7eca1ceec444d3337a2`  
		Last Modified: Thu, 09 Oct 2025 01:14:43 GMT  
		Size: 31.2 KB (31160 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; 386

```console
$ docker pull composer@sha256:275bc5dfce3abe347734c2762514557633d0a6bf7c73e2d6b1c495c9e5aa26c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76609305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796c645fad2ea8d964783b23fb82aedfb209d979c230b00c25604fd831096c12`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:8e5f2af774e5761a1156b63a7ec95c84b3dab008e08a7829523496014e1529f9`  
		Last Modified: Wed, 08 Oct 2025 22:20:17 GMT  
		Size: 34.4 MB (34439092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7eba0d03998e7c05ff8f15fdc7328f5ea1d180cd4436aca79e71d622ad13243`  
		Last Modified: Wed, 08 Oct 2025 22:20:13 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c64f1ca5cf7493dd3ccc28a76979c5ce0b18eed786f6e805642284bb41c768`  
		Last Modified: Wed, 08 Oct 2025 22:20:13 GMT  
		Size: 834.1 KB (834094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d878e8b4cdcf7f66b7884cdf73113fc9e64eb235ec7828bb92c010e477b827e`  
		Last Modified: Wed, 08 Oct 2025 22:20:13 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165978b0065dd1a488f56ceedad46669c24393a8d1ae17c19d77fc28ee618546`  
		Last Modified: Wed, 08 Oct 2025 22:20:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:816444e56181200f8cd6d8158d188ea33fc66af77e7d16820756f503798345b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88ca97d43c7ee6a0792d6eb9b92cdaedc5378819a3f3194f930ba54fbb144fb`

```dockerfile
```

-	Layers:
	-	`sha256:50a705e5d1e5adeb495ef7c327d48c64f431c7d49929f6983489c817106fb1ba`  
		Last Modified: Thu, 09 Oct 2025 01:14:46 GMT  
		Size: 2.2 MB (2172614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7818eef4056a356f4c197d5b6583c3d7767bc31473193323c947d9fba7918179`  
		Last Modified: Thu, 09 Oct 2025 01:14:47 GMT  
		Size: 31.0 KB (31025 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; ppc64le

```console
$ docker pull composer@sha256:267d948789f1e8ba32cd6c41d2d7c2e7f47b99ff376989cfec7d686580aa7db5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77980496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a844aaec8a96a60c5fdc3fbb39e4112ecd4d81e9c30d44f6ab529364b233833`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:fcc750c69d5845f08b366fcf588ae6020f2df3bb4a5bf650228778ed0a9fde88`  
		Last Modified: Thu, 09 Oct 2025 05:56:38 GMT  
		Size: 35.2 MB (35236113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0dfb7c3cec49e9a0f110d7243d5d9fcce6cda1e117d0fbaa88cf3efa29c872`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd01430c925e9bd74329f8c7402b67430ebd0095258f6391d5871865462ab45f`  
		Last Modified: Thu, 09 Oct 2025 05:57:27 GMT  
		Size: 826.9 KB (826863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde899e55f9456e44648f217589cdd59dea02a52ff0559202e0b126d0af8906d`  
		Last Modified: Thu, 09 Oct 2025 05:57:27 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31207cd067ce60336a44109182e5fd7c56a5e49782e4279d6da7042776c941e9`  
		Last Modified: Thu, 09 Oct 2025 05:57:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:0c145e84e5a67b29c59c9876f199eb3cdbe4174dd7a1a19a4e1c2ce05bf15567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5b716ecda48acad1ac905c3c3a5e753f362ed822fb6302eaea2b7fd19b487e`

```dockerfile
```

-	Layers:
	-	`sha256:4c5b326fc1172de42accb95fd5eb0f14dfdaed8af440a3c57ef3550af56628c9`  
		Last Modified: Thu, 09 Oct 2025 07:13:52 GMT  
		Size: 2.2 MB (2171372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91da73e4223b24a5c15a122491267b152c515232ed5594db74a1db1c66cf6138`  
		Last Modified: Thu, 09 Oct 2025 07:13:53 GMT  
		Size: 31.1 KB (31088 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; riscv64

```console
$ docker pull composer@sha256:1687605dca2ecfacc6eaabe67b29dadbcac2de80f74036d0a25cb6c8e9ef4b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75420120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf9d946e52d3cbc2cb39ab7381a7dbc00b45fce4892e3ded5408a9bbe222cd3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Mon, 13 Oct 2025 01:16:18 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c293b040c7a67eeac13c53a522990f19f36e1b39939bdc55cbe7dbeefa2c82`  
		Last Modified: Sat, 11 Oct 2025 17:48:45 GMT  
		Size: 3.6 MB (3594168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4153c5fef55d21621d3f69b9fd9a25c43bda1995413d8f4dcacf545b0d8d2a0b`  
		Last Modified: Sat, 11 Oct 2025 04:03:27 GMT  
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
	-	`sha256:8086d8efed09e7df388724484c2e24d189528f19da5afbedccd3e94622be6286`  
		Last Modified: Fri, 26 Sep 2025 22:46:25 GMT  
		Size: 31.1 MB (31111630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8335f4e7521dca07f16a62141ea1763295dac7280d3dd4e5fa1c649800e6a8`  
		Last Modified: Fri, 26 Sep 2025 22:46:22 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25508299961ce601ee600b85d9a8aaeb951ba1ee475d6d645846406575d68b8c`  
		Last Modified: Fri, 26 Sep 2025 23:12:32 GMT  
		Size: 1.5 MB (1508462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f38cb87c5f84812216d276b6a2bf28a678cf0eb9103c9a791526aa520193b3`  
		Last Modified: Fri, 26 Sep 2025 23:12:52 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7c90ff9a3b5ba67295dc940e66b428e4f26a22621cf14df66a474da160559d`  
		Last Modified: Fri, 26 Sep 2025 23:12:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:2e48b5aa91c01b0f5b50ef7ebaa13dbf58ad173d9c0245b476840265e59e34ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2198117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91860890c1b23e33150a8fe202b5eb5585a267091a1b153cd121d74938dab16a`

```dockerfile
```

-	Layers:
	-	`sha256:106f84a997bad527222954bd0cc4ba4250fa3055fbfa1da69466373d68c26283`  
		Last Modified: Sat, 27 Sep 2025 01:14:14 GMT  
		Size: 2.2 MB (2167026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5773e57aaffa0f6d555871d13ee3f30e278182d3e08122ee3ba1e6a2f3afa5a`  
		Last Modified: Sat, 27 Sep 2025 01:14:15 GMT  
		Size: 31.1 KB (31091 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; s390x

```console
$ docker pull composer@sha256:1613f51eb6e97ebe0e044364b0efc85dee0a15f781e16f868c4da86b8598eca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73688072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa9b56fa76a4083186af4f23bc2142eba8efaa43417ec7a273d17b0b99989c3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
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
	-	`sha256:4e5219110d4f3e49ef43fca54c828f77476de52c08e27b490e23eb605777c4b8`  
		Last Modified: Thu, 09 Oct 2025 08:07:33 GMT  
		Size: 31.8 MB (31841368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b912ad325203381f087b9b20815b78a8a62274eb021560b83d0a130fdadc83`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f07303d79642f1f6fb404a8362ed6ae9eddc69cd78578e51091cb475493090`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 823.3 KB (823321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2253d23f87d556dbd49a9d60e5599181400a82b367969b3240ebfec9ed62e295`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055da3fa01337a487323a552025f2674b3813f2ae6ad386ea8de35aa22f6361d`  
		Last Modified: Thu, 09 Oct 2025 08:07:32 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:02d56363e74dcb994393bb3f8b0c29e018e3b0dd1b94972fae8ebe9d0c11c8b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2200485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0215206443c671d7a23d81c0bfa3a6935208899dc688605e06b3892f2ab44551`

```dockerfile
```

-	Layers:
	-	`sha256:561cc1a52b71fb0fa9ed6c468b6f2da2b033fd505534e1a90ec2206346fa38ed`  
		Last Modified: Thu, 09 Oct 2025 10:14:14 GMT  
		Size: 2.2 MB (2169433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5fc09a5ef7167a9597751e5d1f89d97f7ed736db1e45b06e009d9a11fc2aa89`  
		Last Modified: Thu, 09 Oct 2025 10:14:15 GMT  
		Size: 31.1 KB (31052 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8`

```console
$ docker pull composer@sha256:e4580e48611e8f22e3440b1334557c9e8e893f753b05c67237fdddc0ece7d582
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
$ docker pull composer@sha256:e6bb44785d7241c1aa8401c0c180f904995bebaadf6f9ab0bf668457a491b9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76352034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e3260f706ce27b3ab500c309575abca3892b04b5a07ceaafb9149f7d27aa41`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:7432aafef02307143bba29ffd243e3f04304b1807be61bf76435deabbb0758df`  
		Last Modified: Wed, 08 Oct 2025 23:38:28 GMT  
		Size: 33.9 MB (33926475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fad6092b1df4c88e89b597e81d0fefac2f2d75c80ccb72b8568ef4cfcc60d78`  
		Last Modified: Wed, 08 Oct 2025 23:38:25 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e99b1f89065123d11766026ed9b0d5a4a432302f861722d06b6e0b6336d903a`  
		Last Modified: Wed, 08 Oct 2025 23:38:26 GMT  
		Size: 1.5 MB (1493930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c332e00e89e1a6519f970796f145c0c3295bfb3fb24cc9b4c725c1c0ab01b826`  
		Last Modified: Wed, 08 Oct 2025 23:38:25 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ee9fe0c3413897e0e82404a21c14464223ced79c1a14a98921138a77a4d4d4`  
		Last Modified: Wed, 08 Oct 2025 23:38:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:44c03ff785c4abd36dd0e62f469464c68cd3b8aa13e791dde3dacc7871457790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470ade5e6c4e5efc01c54cdd69d2f92988b06f0b6fed3dc5b90ec5988d929c0a`

```dockerfile
```

-	Layers:
	-	`sha256:420794ff931b66a1f588d676f15552e7364d671939d998e4787c704848a0ea41`  
		Last Modified: Thu, 09 Oct 2025 01:14:09 GMT  
		Size: 2.2 MB (2173415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46b9bc78f2b6aee9e13b019bb0ff3219a5ae25f616cc3cd9b919bf541495a99a`  
		Last Modified: Thu, 09 Oct 2025 01:14:10 GMT  
		Size: 31.7 KB (31658 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v6

```console
$ docker pull composer@sha256:066dfe9368db60c15722653809215179f53cac794ba97cef6d487bb82dfe3ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73464661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150b2ae5648792c8d1a90962e1f1d10f9f5e42b021ac09d403149674f613a897`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:55907e0a0d97a2fff768eed8119a26c68c46291f0356b9f6ab5f15fe11271ebc`  
		Last Modified: Wed, 08 Oct 2025 23:01:24 GMT  
		Size: 33.8 MB (33785137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf44481a6a4a1aac1f5296d10701bdcc2237fcb40ff9425f0de42521c83f839`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c57d6da6f51151ceefa7e8854b8cc35a96ff7c22c0c6de2e86d259b25c9f46`  
		Last Modified: Wed, 08 Oct 2025 23:01:19 GMT  
		Size: 974.0 KB (974037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf78ceeb6dbde8bea48099903a49ed8724c508d216eb8645fc3886903d78efa`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64b1528a9bd520ff23f1ee943c82b6cf59e607a6c36efbcad71899bba19342a`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:ab35ff3471d6f3380d681c65ace2105523b82f138fda910b80b62c3aa181babd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bdf6b5f6ea337235e0adc51c29b36742904baca5d57ac631593b92a8f09604e`

```dockerfile
```

-	Layers:
	-	`sha256:bd9b70b7db28b1b594f5cfa9063ffda6bccaeb4d6ee0921954a02d963dee7573`  
		Last Modified: Thu, 09 Oct 2025 01:14:14 GMT  
		Size: 31.5 KB (31546 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v7

```console
$ docker pull composer@sha256:f41c01ccc01d54af8efc65b7cb9c60a563a6d75524452e6ef9f9c5747e37f51d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70699465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8853953912a39c4f8989eb4936d769995cc08387f0e61090ccc4e6203dc0abf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:1a4af95259bd581f451256ef02f27d6be391c232301f29ea529603ad3209f1f8`  
		Last Modified: Wed, 08 Oct 2025 23:18:11 GMT  
		Size: 32.1 MB (32064307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5218dbe1eddcee4c0851b467212efa963d76151fab105a661669a1e473252b6`  
		Last Modified: Wed, 08 Oct 2025 23:18:09 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fa5ae6c85d8e6af4f100ad64720ae2fd1887ee49e1361990a4813c044f7a5a`  
		Last Modified: Wed, 08 Oct 2025 23:18:09 GMT  
		Size: 1.4 MB (1410445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de89c304165cc7fd6eb4dadc1639306a17257d22ef64304b82f6a0cce143ac84`  
		Last Modified: Wed, 08 Oct 2025 23:18:09 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae5885f9e785d81ab2aa2b6f4a6dce2eb1077ae2da80c3d3b48c6bbf3f2bb16`  
		Last Modified: Wed, 08 Oct 2025 23:18:09 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:1e45776555ba2f3c429d83ffdd848f561c27999b8b2c4bc9813269c33919b9fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a60bf3cfebd70398e8685f8915c0ec275260be9ee167ede378ce12c11e337d7`

```dockerfile
```

-	Layers:
	-	`sha256:984a2a4532ab17eaec3230b94cc85da6a8ec12e3247a7860adc974a24acfb6da`  
		Last Modified: Thu, 09 Oct 2025 01:14:17 GMT  
		Size: 2.2 MB (2173739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa77d58ef12adc720694b933df0185e829a31f2f2f2860096ecf5c683470a86f`  
		Last Modified: Thu, 09 Oct 2025 01:14:18 GMT  
		Size: 31.8 KB (31764 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:231213badba64061194379e913485a9376a14c8753f4d84135e6c9c48ad8d7f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75797731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720bb2065653fbaa53ef45f166d9ae880e1d8eeaa01af447b63b069f661c9362`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:05be2f2fe0c6d3539b2824695cf4df7385787688403ea67197511f9ad0640164`  
		Last Modified: Wed, 08 Oct 2025 22:58:05 GMT  
		Size: 34.0 MB (34006042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e5ee166c845bc9ce53ceaed767d0a11dd333b51b991a682e9688df2e657b24`  
		Last Modified: Wed, 08 Oct 2025 22:58:02 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360bbfda074695914273a729635701189c213b7eb6953dcccfc9e6c7bf8f84a5`  
		Last Modified: Wed, 08 Oct 2025 22:58:02 GMT  
		Size: 973.7 KB (973687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887dadf5f97131ade60fafdb5d7f3eea6b1a69c8bc4f2f18af3fc51b7459e2df`  
		Last Modified: Wed, 08 Oct 2025 22:58:02 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c5722929998f97764e8d53d060ab6ac850d94e87c95696425f951da684a723`  
		Last Modified: Wed, 08 Oct 2025 22:58:02 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:96005ecb1b0ae7afd570fc18f2ae00d10c34ab5e9610f2a92f727131f7ea4436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2b5abb2a73ccc3ae0c6d16384a9f2b4b77c83e761228cf38cca359171a6ad2`

```dockerfile
```

-	Layers:
	-	`sha256:79036f99c9459174eb104dbe582b30aab5871a6d9d37ace423e02cb1530d37ec`  
		Last Modified: Thu, 09 Oct 2025 01:14:21 GMT  
		Size: 2.2 MB (2173567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d46bfe0c45127c0fbc3e70294648b6bd38c23c0c8cbb960f15ea10f0b852562a`  
		Last Modified: Thu, 09 Oct 2025 01:14:22 GMT  
		Size: 31.8 KB (31785 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; 386

```console
$ docker pull composer@sha256:6a3f59afde5da4f6b9391506fd900207e40da42032ccce4c3a7defc62b2462c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76763054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab3a848e4eb86c5bf794f27b4df607df07c420abaefb00cff3ab79b3e1670b6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:7c691ac10422996916b935f8d5d84a5c1ab8afbdf533b13d09eae9b03592b329`  
		Last Modified: Wed, 08 Oct 2025 22:20:22 GMT  
		Size: 34.4 MB (34438942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2545756380f549a9469fc9d4c18d7a997645d3a03b61f261a3fc4a6f9f752a3d`  
		Last Modified: Wed, 08 Oct 2025 22:20:19 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecac885c6f8db12081e32083bf44add84b16502729661d8e96118c0e93337e7`  
		Last Modified: Wed, 08 Oct 2025 22:20:19 GMT  
		Size: 988.0 KB (987992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85182bb7b0422e9ec0aa46ad6183a65962e34466d5ff40358928e6874b4187bc`  
		Last Modified: Wed, 08 Oct 2025 22:20:19 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165978b0065dd1a488f56ceedad46669c24393a8d1ae17c19d77fc28ee618546`  
		Last Modified: Wed, 08 Oct 2025 22:20:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:12faaabda51e751a6d02fa7dea31c5abf6fca15284ce889b619ff8799cdfe0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8881957ec1fd99edd6312721df54f2bb0a9c285c495a54d2f0499aba8bc5c5dc`

```dockerfile
```

-	Layers:
	-	`sha256:a6f1f72a228cb3ba026b803dbe8d58f1cf9fca624240f77fa1ea92c0dc5fe45b`  
		Last Modified: Thu, 09 Oct 2025 01:14:25 GMT  
		Size: 2.2 MB (2173198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c02c6ab31783a75024eee8c58c538d3c2b0825d407c25dbfc27cc45e4d51b30`  
		Last Modified: Thu, 09 Oct 2025 01:14:26 GMT  
		Size: 31.6 KB (31619 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; ppc64le

```console
$ docker pull composer@sha256:7ab8f18c7690e96c4b2c0f98ca57e42441737139252d67b4213aa405cfadaeac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78134372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf72e7a7216358538fcfc4866b29268353f4cb0bf3c5f8cd1e41b25e84f7ca00`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:fcc750c69d5845f08b366fcf588ae6020f2df3bb4a5bf650228778ed0a9fde88`  
		Last Modified: Thu, 09 Oct 2025 05:56:38 GMT  
		Size: 35.2 MB (35236113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0dfb7c3cec49e9a0f110d7243d5d9fcce6cda1e117d0fbaa88cf3efa29c872`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7069cbe03c650f9a782b558ea0c7b6eecf0b31471b705b90de9c985fc0584766`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 980.7 KB (980738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c9dfb2c75ab180a836d1a22b7399619b9d8544f6da246eac510b495b3be44b`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b721d4ea96a39181ad8693b4a8d88fb1845f909261dbf8a034cd63e16768dd99`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:11e9c625adf643934ca29589b3d294bb86103370ed72644386527ce5e5e3df3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05059bd123cffb6b560400732d38d0b86867c15100aba79c3223f2169599616d`

```dockerfile
```

-	Layers:
	-	`sha256:765e6400901500e644e76705796817786597f0dba11e9dca3548e9d777025dae`  
		Last Modified: Thu, 09 Oct 2025 07:13:45 GMT  
		Size: 2.2 MB (2171978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c016add85054c3cb7f2c16c4beb8f8dcc5bffc8fb5f7477d3a53ac2a593a2b85`  
		Last Modified: Thu, 09 Oct 2025 07:13:46 GMT  
		Size: 31.7 KB (31703 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; riscv64

```console
$ docker pull composer@sha256:1d531f6222655c15d072a9f6db8453e8a0bb032e4e4204b83817a74d2738c89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75573351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:926f7969346e4ee5064706f5c4b1f5e399bccdef23b37f9421219bf5d40ee091`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Mon, 13 Oct 2025 01:16:18 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c293b040c7a67eeac13c53a522990f19f36e1b39939bdc55cbe7dbeefa2c82`  
		Last Modified: Sat, 11 Oct 2025 17:48:45 GMT  
		Size: 3.6 MB (3594168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4153c5fef55d21621d3f69b9fd9a25c43bda1995413d8f4dcacf545b0d8d2a0b`  
		Last Modified: Sat, 11 Oct 2025 04:03:27 GMT  
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
	-	`sha256:8086d8efed09e7df388724484c2e24d189528f19da5afbedccd3e94622be6286`  
		Last Modified: Fri, 26 Sep 2025 22:46:25 GMT  
		Size: 31.1 MB (31111630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8335f4e7521dca07f16a62141ea1763295dac7280d3dd4e5fa1c649800e6a8`  
		Last Modified: Fri, 26 Sep 2025 22:46:22 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0ef6f0c64bcbebb0c9adeffe61d4e88a267775c3fca323f5008de3d0e3c947`  
		Last Modified: Fri, 26 Sep 2025 22:46:24 GMT  
		Size: 1.7 MB (1661695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c641845927f76b5160006d48115323bd484a02695abfee72587ac201bd713c0f`  
		Last Modified: Fri, 26 Sep 2025 22:46:21 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54910dead3ff72d407b9dc0093aeac9afbb0f4344d8a1d5419239b27d70dbed5`  
		Last Modified: Fri, 26 Sep 2025 22:41:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:97ec634f4b90008c36a551927bd082c289dfb90e0b33d13a9541c2bf7c2a5d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752d59df2b2f1b5806148eaf6c119d6d985be21308bb75140b4222f049c7e186`

```dockerfile
```

-	Layers:
	-	`sha256:d775e1e4f433aceb275670915f58d34c36f1c0f603c4614c4bca4298fe974ca7`  
		Last Modified: Sat, 27 Sep 2025 01:13:54 GMT  
		Size: 2.2 MB (2167632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4727df4b0fc0a73f9cdbcafaa18cc5beaba3f4d82f0d041afdbee85b219b2bf4`  
		Last Modified: Sat, 27 Sep 2025 01:13:54 GMT  
		Size: 31.7 KB (31706 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; s390x

```console
$ docker pull composer@sha256:05595a53f3002bbd2ba712d1885651be62400b12bd14119f40191f7ae3aef015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73841920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502f45c09a39566b91313513de05acd6f1490e3c336a2c7fd24cac084ddf44dc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:4e5219110d4f3e49ef43fca54c828f77476de52c08e27b490e23eb605777c4b8`  
		Last Modified: Thu, 09 Oct 2025 08:07:33 GMT  
		Size: 31.8 MB (31841368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b912ad325203381f087b9b20815b78a8a62274eb021560b83d0a130fdadc83`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b3763f27effcdcc686b244b630554f55656ad8f43c1abc3b8c8d516d707acd`  
		Last Modified: Thu, 09 Oct 2025 08:07:32 GMT  
		Size: 977.2 KB (977171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e53287954018bc60f63bea842b06e6a30715c50a10e7021e3bad0e4ea802725`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3888304b21042155b83dc5bbfb55b5a62ecaa2401bd061ba507b2c2bfd3fa7d`  
		Last Modified: Thu, 09 Oct 2025 08:07:32 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:a1dd369e5929c064afc2005875b7732ba60490562cbaf47c857940c7b8e6bc0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3ea6c568cc3c0b5074248845f5f93c92bb29da444b2c7be0d1529405b9ec94`

```dockerfile
```

-	Layers:
	-	`sha256:a19650be819af7eb6ff88e79275de8056eac5a7f961dda45b1832e83ffd71794`  
		Last Modified: Thu, 09 Oct 2025 10:14:06 GMT  
		Size: 2.2 MB (2170027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:136b3d48a9b0c3a1e679291b71cf94a1e413d4692a883077c8c2fd3fc32b15cc`  
		Last Modified: Thu, 09 Oct 2025 10:14:07 GMT  
		Size: 31.7 KB (31654 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8.12`

```console
$ docker pull composer@sha256:e4580e48611e8f22e3440b1334557c9e8e893f753b05c67237fdddc0ece7d582
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

### `composer:2.8.12` - linux; amd64

```console
$ docker pull composer@sha256:e6bb44785d7241c1aa8401c0c180f904995bebaadf6f9ab0bf668457a491b9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76352034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e3260f706ce27b3ab500c309575abca3892b04b5a07ceaafb9149f7d27aa41`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:7432aafef02307143bba29ffd243e3f04304b1807be61bf76435deabbb0758df`  
		Last Modified: Wed, 08 Oct 2025 23:38:28 GMT  
		Size: 33.9 MB (33926475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fad6092b1df4c88e89b597e81d0fefac2f2d75c80ccb72b8568ef4cfcc60d78`  
		Last Modified: Wed, 08 Oct 2025 23:38:25 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e99b1f89065123d11766026ed9b0d5a4a432302f861722d06b6e0b6336d903a`  
		Last Modified: Wed, 08 Oct 2025 23:38:26 GMT  
		Size: 1.5 MB (1493930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c332e00e89e1a6519f970796f145c0c3295bfb3fb24cc9b4c725c1c0ab01b826`  
		Last Modified: Wed, 08 Oct 2025 23:38:25 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ee9fe0c3413897e0e82404a21c14464223ced79c1a14a98921138a77a4d4d4`  
		Last Modified: Wed, 08 Oct 2025 23:38:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.12` - unknown; unknown

```console
$ docker pull composer@sha256:44c03ff785c4abd36dd0e62f469464c68cd3b8aa13e791dde3dacc7871457790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470ade5e6c4e5efc01c54cdd69d2f92988b06f0b6fed3dc5b90ec5988d929c0a`

```dockerfile
```

-	Layers:
	-	`sha256:420794ff931b66a1f588d676f15552e7364d671939d998e4787c704848a0ea41`  
		Last Modified: Thu, 09 Oct 2025 01:14:09 GMT  
		Size: 2.2 MB (2173415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46b9bc78f2b6aee9e13b019bb0ff3219a5ae25f616cc3cd9b919bf541495a99a`  
		Last Modified: Thu, 09 Oct 2025 01:14:10 GMT  
		Size: 31.7 KB (31658 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.12` - linux; arm variant v6

```console
$ docker pull composer@sha256:066dfe9368db60c15722653809215179f53cac794ba97cef6d487bb82dfe3ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73464661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150b2ae5648792c8d1a90962e1f1d10f9f5e42b021ac09d403149674f613a897`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:55907e0a0d97a2fff768eed8119a26c68c46291f0356b9f6ab5f15fe11271ebc`  
		Last Modified: Wed, 08 Oct 2025 23:01:24 GMT  
		Size: 33.8 MB (33785137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf44481a6a4a1aac1f5296d10701bdcc2237fcb40ff9425f0de42521c83f839`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c57d6da6f51151ceefa7e8854b8cc35a96ff7c22c0c6de2e86d259b25c9f46`  
		Last Modified: Wed, 08 Oct 2025 23:01:19 GMT  
		Size: 974.0 KB (974037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf78ceeb6dbde8bea48099903a49ed8724c508d216eb8645fc3886903d78efa`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64b1528a9bd520ff23f1ee943c82b6cf59e607a6c36efbcad71899bba19342a`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.12` - unknown; unknown

```console
$ docker pull composer@sha256:ab35ff3471d6f3380d681c65ace2105523b82f138fda910b80b62c3aa181babd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bdf6b5f6ea337235e0adc51c29b36742904baca5d57ac631593b92a8f09604e`

```dockerfile
```

-	Layers:
	-	`sha256:bd9b70b7db28b1b594f5cfa9063ffda6bccaeb4d6ee0921954a02d963dee7573`  
		Last Modified: Thu, 09 Oct 2025 01:14:14 GMT  
		Size: 31.5 KB (31546 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.12` - linux; arm variant v7

```console
$ docker pull composer@sha256:f41c01ccc01d54af8efc65b7cb9c60a563a6d75524452e6ef9f9c5747e37f51d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70699465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8853953912a39c4f8989eb4936d769995cc08387f0e61090ccc4e6203dc0abf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:1a4af95259bd581f451256ef02f27d6be391c232301f29ea529603ad3209f1f8`  
		Last Modified: Wed, 08 Oct 2025 23:18:11 GMT  
		Size: 32.1 MB (32064307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5218dbe1eddcee4c0851b467212efa963d76151fab105a661669a1e473252b6`  
		Last Modified: Wed, 08 Oct 2025 23:18:09 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fa5ae6c85d8e6af4f100ad64720ae2fd1887ee49e1361990a4813c044f7a5a`  
		Last Modified: Wed, 08 Oct 2025 23:18:09 GMT  
		Size: 1.4 MB (1410445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de89c304165cc7fd6eb4dadc1639306a17257d22ef64304b82f6a0cce143ac84`  
		Last Modified: Wed, 08 Oct 2025 23:18:09 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae5885f9e785d81ab2aa2b6f4a6dce2eb1077ae2da80c3d3b48c6bbf3f2bb16`  
		Last Modified: Wed, 08 Oct 2025 23:18:09 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.12` - unknown; unknown

```console
$ docker pull composer@sha256:1e45776555ba2f3c429d83ffdd848f561c27999b8b2c4bc9813269c33919b9fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a60bf3cfebd70398e8685f8915c0ec275260be9ee167ede378ce12c11e337d7`

```dockerfile
```

-	Layers:
	-	`sha256:984a2a4532ab17eaec3230b94cc85da6a8ec12e3247a7860adc974a24acfb6da`  
		Last Modified: Thu, 09 Oct 2025 01:14:17 GMT  
		Size: 2.2 MB (2173739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa77d58ef12adc720694b933df0185e829a31f2f2f2860096ecf5c683470a86f`  
		Last Modified: Thu, 09 Oct 2025 01:14:18 GMT  
		Size: 31.8 KB (31764 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.12` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:231213badba64061194379e913485a9376a14c8753f4d84135e6c9c48ad8d7f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75797731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720bb2065653fbaa53ef45f166d9ae880e1d8eeaa01af447b63b069f661c9362`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:05be2f2fe0c6d3539b2824695cf4df7385787688403ea67197511f9ad0640164`  
		Last Modified: Wed, 08 Oct 2025 22:58:05 GMT  
		Size: 34.0 MB (34006042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e5ee166c845bc9ce53ceaed767d0a11dd333b51b991a682e9688df2e657b24`  
		Last Modified: Wed, 08 Oct 2025 22:58:02 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360bbfda074695914273a729635701189c213b7eb6953dcccfc9e6c7bf8f84a5`  
		Last Modified: Wed, 08 Oct 2025 22:58:02 GMT  
		Size: 973.7 KB (973687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887dadf5f97131ade60fafdb5d7f3eea6b1a69c8bc4f2f18af3fc51b7459e2df`  
		Last Modified: Wed, 08 Oct 2025 22:58:02 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c5722929998f97764e8d53d060ab6ac850d94e87c95696425f951da684a723`  
		Last Modified: Wed, 08 Oct 2025 22:58:02 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.12` - unknown; unknown

```console
$ docker pull composer@sha256:96005ecb1b0ae7afd570fc18f2ae00d10c34ab5e9610f2a92f727131f7ea4436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2b5abb2a73ccc3ae0c6d16384a9f2b4b77c83e761228cf38cca359171a6ad2`

```dockerfile
```

-	Layers:
	-	`sha256:79036f99c9459174eb104dbe582b30aab5871a6d9d37ace423e02cb1530d37ec`  
		Last Modified: Thu, 09 Oct 2025 01:14:21 GMT  
		Size: 2.2 MB (2173567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d46bfe0c45127c0fbc3e70294648b6bd38c23c0c8cbb960f15ea10f0b852562a`  
		Last Modified: Thu, 09 Oct 2025 01:14:22 GMT  
		Size: 31.8 KB (31785 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.12` - linux; 386

```console
$ docker pull composer@sha256:6a3f59afde5da4f6b9391506fd900207e40da42032ccce4c3a7defc62b2462c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76763054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab3a848e4eb86c5bf794f27b4df607df07c420abaefb00cff3ab79b3e1670b6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:7c691ac10422996916b935f8d5d84a5c1ab8afbdf533b13d09eae9b03592b329`  
		Last Modified: Wed, 08 Oct 2025 22:20:22 GMT  
		Size: 34.4 MB (34438942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2545756380f549a9469fc9d4c18d7a997645d3a03b61f261a3fc4a6f9f752a3d`  
		Last Modified: Wed, 08 Oct 2025 22:20:19 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecac885c6f8db12081e32083bf44add84b16502729661d8e96118c0e93337e7`  
		Last Modified: Wed, 08 Oct 2025 22:20:19 GMT  
		Size: 988.0 KB (987992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85182bb7b0422e9ec0aa46ad6183a65962e34466d5ff40358928e6874b4187bc`  
		Last Modified: Wed, 08 Oct 2025 22:20:19 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165978b0065dd1a488f56ceedad46669c24393a8d1ae17c19d77fc28ee618546`  
		Last Modified: Wed, 08 Oct 2025 22:20:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.12` - unknown; unknown

```console
$ docker pull composer@sha256:12faaabda51e751a6d02fa7dea31c5abf6fca15284ce889b619ff8799cdfe0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8881957ec1fd99edd6312721df54f2bb0a9c285c495a54d2f0499aba8bc5c5dc`

```dockerfile
```

-	Layers:
	-	`sha256:a6f1f72a228cb3ba026b803dbe8d58f1cf9fca624240f77fa1ea92c0dc5fe45b`  
		Last Modified: Thu, 09 Oct 2025 01:14:25 GMT  
		Size: 2.2 MB (2173198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c02c6ab31783a75024eee8c58c538d3c2b0825d407c25dbfc27cc45e4d51b30`  
		Last Modified: Thu, 09 Oct 2025 01:14:26 GMT  
		Size: 31.6 KB (31619 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.12` - linux; ppc64le

```console
$ docker pull composer@sha256:7ab8f18c7690e96c4b2c0f98ca57e42441737139252d67b4213aa405cfadaeac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78134372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf72e7a7216358538fcfc4866b29268353f4cb0bf3c5f8cd1e41b25e84f7ca00`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:fcc750c69d5845f08b366fcf588ae6020f2df3bb4a5bf650228778ed0a9fde88`  
		Last Modified: Thu, 09 Oct 2025 05:56:38 GMT  
		Size: 35.2 MB (35236113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0dfb7c3cec49e9a0f110d7243d5d9fcce6cda1e117d0fbaa88cf3efa29c872`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7069cbe03c650f9a782b558ea0c7b6eecf0b31471b705b90de9c985fc0584766`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 980.7 KB (980738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c9dfb2c75ab180a836d1a22b7399619b9d8544f6da246eac510b495b3be44b`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b721d4ea96a39181ad8693b4a8d88fb1845f909261dbf8a034cd63e16768dd99`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.12` - unknown; unknown

```console
$ docker pull composer@sha256:11e9c625adf643934ca29589b3d294bb86103370ed72644386527ce5e5e3df3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05059bd123cffb6b560400732d38d0b86867c15100aba79c3223f2169599616d`

```dockerfile
```

-	Layers:
	-	`sha256:765e6400901500e644e76705796817786597f0dba11e9dca3548e9d777025dae`  
		Last Modified: Thu, 09 Oct 2025 07:13:45 GMT  
		Size: 2.2 MB (2171978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c016add85054c3cb7f2c16c4beb8f8dcc5bffc8fb5f7477d3a53ac2a593a2b85`  
		Last Modified: Thu, 09 Oct 2025 07:13:46 GMT  
		Size: 31.7 KB (31703 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.12` - linux; riscv64

```console
$ docker pull composer@sha256:1d531f6222655c15d072a9f6db8453e8a0bb032e4e4204b83817a74d2738c89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75573351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:926f7969346e4ee5064706f5c4b1f5e399bccdef23b37f9421219bf5d40ee091`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Mon, 13 Oct 2025 01:16:18 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c293b040c7a67eeac13c53a522990f19f36e1b39939bdc55cbe7dbeefa2c82`  
		Last Modified: Sat, 11 Oct 2025 17:48:45 GMT  
		Size: 3.6 MB (3594168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4153c5fef55d21621d3f69b9fd9a25c43bda1995413d8f4dcacf545b0d8d2a0b`  
		Last Modified: Sat, 11 Oct 2025 04:03:27 GMT  
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
	-	`sha256:8086d8efed09e7df388724484c2e24d189528f19da5afbedccd3e94622be6286`  
		Last Modified: Fri, 26 Sep 2025 22:46:25 GMT  
		Size: 31.1 MB (31111630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8335f4e7521dca07f16a62141ea1763295dac7280d3dd4e5fa1c649800e6a8`  
		Last Modified: Fri, 26 Sep 2025 22:46:22 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0ef6f0c64bcbebb0c9adeffe61d4e88a267775c3fca323f5008de3d0e3c947`  
		Last Modified: Fri, 26 Sep 2025 22:46:24 GMT  
		Size: 1.7 MB (1661695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c641845927f76b5160006d48115323bd484a02695abfee72587ac201bd713c0f`  
		Last Modified: Fri, 26 Sep 2025 22:46:21 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54910dead3ff72d407b9dc0093aeac9afbb0f4344d8a1d5419239b27d70dbed5`  
		Last Modified: Fri, 26 Sep 2025 22:41:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.12` - unknown; unknown

```console
$ docker pull composer@sha256:97ec634f4b90008c36a551927bd082c289dfb90e0b33d13a9541c2bf7c2a5d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752d59df2b2f1b5806148eaf6c119d6d985be21308bb75140b4222f049c7e186`

```dockerfile
```

-	Layers:
	-	`sha256:d775e1e4f433aceb275670915f58d34c36f1c0f603c4614c4bca4298fe974ca7`  
		Last Modified: Sat, 27 Sep 2025 01:13:54 GMT  
		Size: 2.2 MB (2167632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4727df4b0fc0a73f9cdbcafaa18cc5beaba3f4d82f0d041afdbee85b219b2bf4`  
		Last Modified: Sat, 27 Sep 2025 01:13:54 GMT  
		Size: 31.7 KB (31706 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.12` - linux; s390x

```console
$ docker pull composer@sha256:05595a53f3002bbd2ba712d1885651be62400b12bd14119f40191f7ae3aef015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73841920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502f45c09a39566b91313513de05acd6f1490e3c336a2c7fd24cac084ddf44dc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:4e5219110d4f3e49ef43fca54c828f77476de52c08e27b490e23eb605777c4b8`  
		Last Modified: Thu, 09 Oct 2025 08:07:33 GMT  
		Size: 31.8 MB (31841368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b912ad325203381f087b9b20815b78a8a62274eb021560b83d0a130fdadc83`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b3763f27effcdcc686b244b630554f55656ad8f43c1abc3b8c8d516d707acd`  
		Last Modified: Thu, 09 Oct 2025 08:07:32 GMT  
		Size: 977.2 KB (977171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e53287954018bc60f63bea842b06e6a30715c50a10e7021e3bad0e4ea802725`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3888304b21042155b83dc5bbfb55b5a62ecaa2401bd061ba507b2c2bfd3fa7d`  
		Last Modified: Thu, 09 Oct 2025 08:07:32 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.12` - unknown; unknown

```console
$ docker pull composer@sha256:a1dd369e5929c064afc2005875b7732ba60490562cbaf47c857940c7b8e6bc0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3ea6c568cc3c0b5074248845f5f93c92bb29da444b2c7be0d1529405b9ec94`

```dockerfile
```

-	Layers:
	-	`sha256:a19650be819af7eb6ff88e79275de8056eac5a7f961dda45b1832e83ffd71794`  
		Last Modified: Thu, 09 Oct 2025 10:14:06 GMT  
		Size: 2.2 MB (2170027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:136b3d48a9b0c3a1e679291b71cf94a1e413d4692a883077c8c2fd3fc32b15cc`  
		Last Modified: Thu, 09 Oct 2025 10:14:07 GMT  
		Size: 31.7 KB (31654 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:latest`

```console
$ docker pull composer@sha256:e4580e48611e8f22e3440b1334557c9e8e893f753b05c67237fdddc0ece7d582
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
$ docker pull composer@sha256:e6bb44785d7241c1aa8401c0c180f904995bebaadf6f9ab0bf668457a491b9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76352034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e3260f706ce27b3ab500c309575abca3892b04b5a07ceaafb9149f7d27aa41`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:7432aafef02307143bba29ffd243e3f04304b1807be61bf76435deabbb0758df`  
		Last Modified: Wed, 08 Oct 2025 23:38:28 GMT  
		Size: 33.9 MB (33926475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fad6092b1df4c88e89b597e81d0fefac2f2d75c80ccb72b8568ef4cfcc60d78`  
		Last Modified: Wed, 08 Oct 2025 23:38:25 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e99b1f89065123d11766026ed9b0d5a4a432302f861722d06b6e0b6336d903a`  
		Last Modified: Wed, 08 Oct 2025 23:38:26 GMT  
		Size: 1.5 MB (1493930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c332e00e89e1a6519f970796f145c0c3295bfb3fb24cc9b4c725c1c0ab01b826`  
		Last Modified: Wed, 08 Oct 2025 23:38:25 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ee9fe0c3413897e0e82404a21c14464223ced79c1a14a98921138a77a4d4d4`  
		Last Modified: Wed, 08 Oct 2025 23:38:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:44c03ff785c4abd36dd0e62f469464c68cd3b8aa13e791dde3dacc7871457790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470ade5e6c4e5efc01c54cdd69d2f92988b06f0b6fed3dc5b90ec5988d929c0a`

```dockerfile
```

-	Layers:
	-	`sha256:420794ff931b66a1f588d676f15552e7364d671939d998e4787c704848a0ea41`  
		Last Modified: Thu, 09 Oct 2025 01:14:09 GMT  
		Size: 2.2 MB (2173415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46b9bc78f2b6aee9e13b019bb0ff3219a5ae25f616cc3cd9b919bf541495a99a`  
		Last Modified: Thu, 09 Oct 2025 01:14:10 GMT  
		Size: 31.7 KB (31658 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:066dfe9368db60c15722653809215179f53cac794ba97cef6d487bb82dfe3ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73464661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150b2ae5648792c8d1a90962e1f1d10f9f5e42b021ac09d403149674f613a897`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:55907e0a0d97a2fff768eed8119a26c68c46291f0356b9f6ab5f15fe11271ebc`  
		Last Modified: Wed, 08 Oct 2025 23:01:24 GMT  
		Size: 33.8 MB (33785137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf44481a6a4a1aac1f5296d10701bdcc2237fcb40ff9425f0de42521c83f839`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c57d6da6f51151ceefa7e8854b8cc35a96ff7c22c0c6de2e86d259b25c9f46`  
		Last Modified: Wed, 08 Oct 2025 23:01:19 GMT  
		Size: 974.0 KB (974037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf78ceeb6dbde8bea48099903a49ed8724c508d216eb8645fc3886903d78efa`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64b1528a9bd520ff23f1ee943c82b6cf59e607a6c36efbcad71899bba19342a`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:ab35ff3471d6f3380d681c65ace2105523b82f138fda910b80b62c3aa181babd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bdf6b5f6ea337235e0adc51c29b36742904baca5d57ac631593b92a8f09604e`

```dockerfile
```

-	Layers:
	-	`sha256:bd9b70b7db28b1b594f5cfa9063ffda6bccaeb4d6ee0921954a02d963dee7573`  
		Last Modified: Thu, 09 Oct 2025 01:14:14 GMT  
		Size: 31.5 KB (31546 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:f41c01ccc01d54af8efc65b7cb9c60a563a6d75524452e6ef9f9c5747e37f51d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70699465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8853953912a39c4f8989eb4936d769995cc08387f0e61090ccc4e6203dc0abf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:1a4af95259bd581f451256ef02f27d6be391c232301f29ea529603ad3209f1f8`  
		Last Modified: Wed, 08 Oct 2025 23:18:11 GMT  
		Size: 32.1 MB (32064307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5218dbe1eddcee4c0851b467212efa963d76151fab105a661669a1e473252b6`  
		Last Modified: Wed, 08 Oct 2025 23:18:09 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fa5ae6c85d8e6af4f100ad64720ae2fd1887ee49e1361990a4813c044f7a5a`  
		Last Modified: Wed, 08 Oct 2025 23:18:09 GMT  
		Size: 1.4 MB (1410445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de89c304165cc7fd6eb4dadc1639306a17257d22ef64304b82f6a0cce143ac84`  
		Last Modified: Wed, 08 Oct 2025 23:18:09 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae5885f9e785d81ab2aa2b6f4a6dce2eb1077ae2da80c3d3b48c6bbf3f2bb16`  
		Last Modified: Wed, 08 Oct 2025 23:18:09 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:1e45776555ba2f3c429d83ffdd848f561c27999b8b2c4bc9813269c33919b9fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a60bf3cfebd70398e8685f8915c0ec275260be9ee167ede378ce12c11e337d7`

```dockerfile
```

-	Layers:
	-	`sha256:984a2a4532ab17eaec3230b94cc85da6a8ec12e3247a7860adc974a24acfb6da`  
		Last Modified: Thu, 09 Oct 2025 01:14:17 GMT  
		Size: 2.2 MB (2173739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa77d58ef12adc720694b933df0185e829a31f2f2f2860096ecf5c683470a86f`  
		Last Modified: Thu, 09 Oct 2025 01:14:18 GMT  
		Size: 31.8 KB (31764 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:231213badba64061194379e913485a9376a14c8753f4d84135e6c9c48ad8d7f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75797731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720bb2065653fbaa53ef45f166d9ae880e1d8eeaa01af447b63b069f661c9362`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:05be2f2fe0c6d3539b2824695cf4df7385787688403ea67197511f9ad0640164`  
		Last Modified: Wed, 08 Oct 2025 22:58:05 GMT  
		Size: 34.0 MB (34006042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e5ee166c845bc9ce53ceaed767d0a11dd333b51b991a682e9688df2e657b24`  
		Last Modified: Wed, 08 Oct 2025 22:58:02 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360bbfda074695914273a729635701189c213b7eb6953dcccfc9e6c7bf8f84a5`  
		Last Modified: Wed, 08 Oct 2025 22:58:02 GMT  
		Size: 973.7 KB (973687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887dadf5f97131ade60fafdb5d7f3eea6b1a69c8bc4f2f18af3fc51b7459e2df`  
		Last Modified: Wed, 08 Oct 2025 22:58:02 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c5722929998f97764e8d53d060ab6ac850d94e87c95696425f951da684a723`  
		Last Modified: Wed, 08 Oct 2025 22:58:02 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:96005ecb1b0ae7afd570fc18f2ae00d10c34ab5e9610f2a92f727131f7ea4436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2b5abb2a73ccc3ae0c6d16384a9f2b4b77c83e761228cf38cca359171a6ad2`

```dockerfile
```

-	Layers:
	-	`sha256:79036f99c9459174eb104dbe582b30aab5871a6d9d37ace423e02cb1530d37ec`  
		Last Modified: Thu, 09 Oct 2025 01:14:21 GMT  
		Size: 2.2 MB (2173567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d46bfe0c45127c0fbc3e70294648b6bd38c23c0c8cbb960f15ea10f0b852562a`  
		Last Modified: Thu, 09 Oct 2025 01:14:22 GMT  
		Size: 31.8 KB (31785 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; 386

```console
$ docker pull composer@sha256:6a3f59afde5da4f6b9391506fd900207e40da42032ccce4c3a7defc62b2462c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76763054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab3a848e4eb86c5bf794f27b4df607df07c420abaefb00cff3ab79b3e1670b6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:7c691ac10422996916b935f8d5d84a5c1ab8afbdf533b13d09eae9b03592b329`  
		Last Modified: Wed, 08 Oct 2025 22:20:22 GMT  
		Size: 34.4 MB (34438942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2545756380f549a9469fc9d4c18d7a997645d3a03b61f261a3fc4a6f9f752a3d`  
		Last Modified: Wed, 08 Oct 2025 22:20:19 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecac885c6f8db12081e32083bf44add84b16502729661d8e96118c0e93337e7`  
		Last Modified: Wed, 08 Oct 2025 22:20:19 GMT  
		Size: 988.0 KB (987992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85182bb7b0422e9ec0aa46ad6183a65962e34466d5ff40358928e6874b4187bc`  
		Last Modified: Wed, 08 Oct 2025 22:20:19 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165978b0065dd1a488f56ceedad46669c24393a8d1ae17c19d77fc28ee618546`  
		Last Modified: Wed, 08 Oct 2025 22:20:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:12faaabda51e751a6d02fa7dea31c5abf6fca15284ce889b619ff8799cdfe0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8881957ec1fd99edd6312721df54f2bb0a9c285c495a54d2f0499aba8bc5c5dc`

```dockerfile
```

-	Layers:
	-	`sha256:a6f1f72a228cb3ba026b803dbe8d58f1cf9fca624240f77fa1ea92c0dc5fe45b`  
		Last Modified: Thu, 09 Oct 2025 01:14:25 GMT  
		Size: 2.2 MB (2173198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c02c6ab31783a75024eee8c58c538d3c2b0825d407c25dbfc27cc45e4d51b30`  
		Last Modified: Thu, 09 Oct 2025 01:14:26 GMT  
		Size: 31.6 KB (31619 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; ppc64le

```console
$ docker pull composer@sha256:7ab8f18c7690e96c4b2c0f98ca57e42441737139252d67b4213aa405cfadaeac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78134372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf72e7a7216358538fcfc4866b29268353f4cb0bf3c5f8cd1e41b25e84f7ca00`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:fcc750c69d5845f08b366fcf588ae6020f2df3bb4a5bf650228778ed0a9fde88`  
		Last Modified: Thu, 09 Oct 2025 05:56:38 GMT  
		Size: 35.2 MB (35236113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0dfb7c3cec49e9a0f110d7243d5d9fcce6cda1e117d0fbaa88cf3efa29c872`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7069cbe03c650f9a782b558ea0c7b6eecf0b31471b705b90de9c985fc0584766`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 980.7 KB (980738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c9dfb2c75ab180a836d1a22b7399619b9d8544f6da246eac510b495b3be44b`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b721d4ea96a39181ad8693b4a8d88fb1845f909261dbf8a034cd63e16768dd99`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:11e9c625adf643934ca29589b3d294bb86103370ed72644386527ce5e5e3df3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05059bd123cffb6b560400732d38d0b86867c15100aba79c3223f2169599616d`

```dockerfile
```

-	Layers:
	-	`sha256:765e6400901500e644e76705796817786597f0dba11e9dca3548e9d777025dae`  
		Last Modified: Thu, 09 Oct 2025 07:13:45 GMT  
		Size: 2.2 MB (2171978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c016add85054c3cb7f2c16c4beb8f8dcc5bffc8fb5f7477d3a53ac2a593a2b85`  
		Last Modified: Thu, 09 Oct 2025 07:13:46 GMT  
		Size: 31.7 KB (31703 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; riscv64

```console
$ docker pull composer@sha256:1d531f6222655c15d072a9f6db8453e8a0bb032e4e4204b83817a74d2738c89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75573351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:926f7969346e4ee5064706f5c4b1f5e399bccdef23b37f9421219bf5d40ee091`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Mon, 13 Oct 2025 01:16:18 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c293b040c7a67eeac13c53a522990f19f36e1b39939bdc55cbe7dbeefa2c82`  
		Last Modified: Sat, 11 Oct 2025 17:48:45 GMT  
		Size: 3.6 MB (3594168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4153c5fef55d21621d3f69b9fd9a25c43bda1995413d8f4dcacf545b0d8d2a0b`  
		Last Modified: Sat, 11 Oct 2025 04:03:27 GMT  
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
	-	`sha256:8086d8efed09e7df388724484c2e24d189528f19da5afbedccd3e94622be6286`  
		Last Modified: Fri, 26 Sep 2025 22:46:25 GMT  
		Size: 31.1 MB (31111630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8335f4e7521dca07f16a62141ea1763295dac7280d3dd4e5fa1c649800e6a8`  
		Last Modified: Fri, 26 Sep 2025 22:46:22 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0ef6f0c64bcbebb0c9adeffe61d4e88a267775c3fca323f5008de3d0e3c947`  
		Last Modified: Fri, 26 Sep 2025 22:46:24 GMT  
		Size: 1.7 MB (1661695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c641845927f76b5160006d48115323bd484a02695abfee72587ac201bd713c0f`  
		Last Modified: Fri, 26 Sep 2025 22:46:21 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54910dead3ff72d407b9dc0093aeac9afbb0f4344d8a1d5419239b27d70dbed5`  
		Last Modified: Fri, 26 Sep 2025 22:41:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:97ec634f4b90008c36a551927bd082c289dfb90e0b33d13a9541c2bf7c2a5d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752d59df2b2f1b5806148eaf6c119d6d985be21308bb75140b4222f049c7e186`

```dockerfile
```

-	Layers:
	-	`sha256:d775e1e4f433aceb275670915f58d34c36f1c0f603c4614c4bca4298fe974ca7`  
		Last Modified: Sat, 27 Sep 2025 01:13:54 GMT  
		Size: 2.2 MB (2167632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4727df4b0fc0a73f9cdbcafaa18cc5beaba3f4d82f0d041afdbee85b219b2bf4`  
		Last Modified: Sat, 27 Sep 2025 01:13:54 GMT  
		Size: 31.7 KB (31706 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; s390x

```console
$ docker pull composer@sha256:05595a53f3002bbd2ba712d1885651be62400b12bd14119f40191f7ae3aef015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73841920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502f45c09a39566b91313513de05acd6f1490e3c336a2c7fd24cac084ddf44dc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["composer"]
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
	-	`sha256:4e5219110d4f3e49ef43fca54c828f77476de52c08e27b490e23eb605777c4b8`  
		Last Modified: Thu, 09 Oct 2025 08:07:33 GMT  
		Size: 31.8 MB (31841368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b912ad325203381f087b9b20815b78a8a62274eb021560b83d0a130fdadc83`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b3763f27effcdcc686b244b630554f55656ad8f43c1abc3b8c8d516d707acd`  
		Last Modified: Thu, 09 Oct 2025 08:07:32 GMT  
		Size: 977.2 KB (977171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e53287954018bc60f63bea842b06e6a30715c50a10e7021e3bad0e4ea802725`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3888304b21042155b83dc5bbfb55b5a62ecaa2401bd061ba507b2c2bfd3fa7d`  
		Last Modified: Thu, 09 Oct 2025 08:07:32 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:a1dd369e5929c064afc2005875b7732ba60490562cbaf47c857940c7b8e6bc0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3ea6c568cc3c0b5074248845f5f93c92bb29da444b2c7be0d1529405b9ec94`

```dockerfile
```

-	Layers:
	-	`sha256:a19650be819af7eb6ff88e79275de8056eac5a7f961dda45b1832e83ffd71794`  
		Last Modified: Thu, 09 Oct 2025 10:14:06 GMT  
		Size: 2.2 MB (2170027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:136b3d48a9b0c3a1e679291b71cf94a1e413d4692a883077c8c2fd3fc32b15cc`  
		Last Modified: Thu, 09 Oct 2025 10:14:07 GMT  
		Size: 31.7 KB (31654 bytes)  
		MIME: application/vnd.in-toto+json
