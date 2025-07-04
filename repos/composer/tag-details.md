<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `composer`

-	[`composer:1`](#composer1)
-	[`composer:1.10`](#composer110)
-	[`composer:1.10.27`](#composer11027)
-	[`composer:2`](#composer2)
-	[`composer:2.2`](#composer22)
-	[`composer:2.2.25`](#composer2225)
-	[`composer:2.8`](#composer28)
-	[`composer:2.8.9`](#composer289)
-	[`composer:latest`](#composerlatest)
-	[`composer:lts`](#composerlts)

## `composer:1`

```console
$ docker pull composer@sha256:e48b612b785dcb1f6fd5e34130da038bb745c0d3a570ec69c9d0b8a48b41b22e
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
$ docker pull composer@sha256:44ea0b30fd71ae7703321bd4e235db261ea62295cc5d4a547457ccb41e408a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79068992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b090bbb72095287470c965696b7b90b3a0c9e664287a78a2d6624ad1c0bd1c40`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b94662290ef2237915af922ad14ae2b406eccea26d9201aa949ea52f20b737f`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 5.9 MB (5944403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498a67832465ef6dae00170ccca088bdbc63d05a197e0ba1403442805169a06a`  
		Last Modified: Thu, 03 Jul 2025 23:04:16 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53785dc48fc021d1c3f9c46a776ead61a024377fb5e6ab592908501762d63a7`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c87a7802578b0a5aebb57ffea8e543a2d50cff1ec6ffb0941fe8ad61b3a9e6`  
		Last Modified: Thu, 03 Jul 2025 23:04:23 GMT  
		Size: 13.6 MB (13647262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5aa21d09531523ae5c279a8b0eb00236af3b192f428c934050c61f7e1611eaa`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fccbfd125531b00b24f5c4c9c182e17714478e55b96701b7e71d30f7f70f9b`  
		Last Modified: Thu, 03 Jul 2025 23:04:28 GMT  
		Size: 21.0 MB (20971251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481b52666b981ec99f99b98b64ef13ff6ce799950970b68817767c966318dc11`  
		Last Modified: Thu, 03 Jul 2025 23:04:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a3724a01f76e5128bdebeeb89d8f42b63b2e987403c91e1f1f5c084c63ffee`  
		Last Modified: Thu, 03 Jul 2025 23:04:22 GMT  
		Size: 20.2 KB (20205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755a5679cebfbcec196508684d58f3d3479a8923825702cea8057be9ea0509ea`  
		Last Modified: Thu, 03 Jul 2025 23:04:25 GMT  
		Size: 20.2 KB (20204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c702e8f6c7cead92f757244a0e08915ffffe43fbe74a0923d30c01f2d9c90c37`  
		Last Modified: Thu, 03 Jul 2025 23:13:14 GMT  
		Size: 33.9 MB (33928442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688d6535fcb8eb0d12463480f6752f4e9bb65bf9267be71c1587b3f945b1941d`  
		Last Modified: Thu, 03 Jul 2025 23:13:11 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c39dd4f0d2117bc5a02bbb5192170fe65e2f0c2302b01c95ef6adb829ef689a`  
		Last Modified: Thu, 03 Jul 2025 23:13:12 GMT  
		Size: 735.5 KB (735538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a74b619e9325ae8e5b5adb511075d9c35247e8de5593f5996184112a115ffd`  
		Last Modified: Thu, 03 Jul 2025 23:13:12 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78d5acf69b51a1fe4d9f67ce5f26c6f01d2cf6d3a8795c5edf5de1e03843b82`  
		Last Modified: Thu, 03 Jul 2025 23:13:12 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:a40b0954587af3d3cb6506954d3609818942e2626e2b484baf5ef32e2f758fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7630f9c336baad52d91c577df4c2b82980a9e7c11823385c876e62a4c3b82ec1`

```dockerfile
```

-	Layers:
	-	`sha256:68699c3048c4af9b4b3b9cd8448d2ecf4689d835321caf458ead0ae588cd8895`  
		Last Modified: Fri, 04 Jul 2025 01:13:29 GMT  
		Size: 2.2 MB (2173846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7afc7d1b68b82c353c58c33175613c1fcaa298adaa6a87175e82c63e7a485b0f`  
		Last Modified: Fri, 04 Jul 2025 01:13:30 GMT  
		Size: 31.4 KB (31362 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v6

```console
$ docker pull composer@sha256:c04f5f68a1cd6b21b39fa9629ec09c04ea7a0a61ab085c5a39c2bc78a0218b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77384933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b662652d26f29a2cf473a00d55c6e7d3a5daacd4df84871a99ded37edfb7ab9c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4a1a48d371204daac6d50cf0ade3fcbe953b7326556c347d0834eeb808b22f`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 13.6 MB (13647232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7209fb73f851518e0fbc85b54004a573116286207c48ee96ab37833cb8ea1353`  
		Last Modified: Thu, 03 Jul 2025 23:00:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7698dfdb6ae14586a077f81a7e7531ba3d394ab385475ff9c6573114a36ad047`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 22.2 MB (22216193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2822e518605b3410372bbcdb567b3220dcdbe3fc3a85d76aeeed7414a97ce84`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc23f56a1dfd1eb937c6d0d63cb116029d4ac6193e3b8e0487798f7859b09cf`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb672fb64a4977b38f156870ac6fd28ad3898b39594ead2e5d7a7a25cf62e07a`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f65dda0589cf68df6c1f7a31f2ed36448fe5ac89816b32bef12a62b39575a0`  
		Last Modified: Fri, 04 Jul 2025 01:07:05 GMT  
		Size: 33.8 MB (33807127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af16e8c9f29c59fdf9ae69e6ad7a7f42c68aea017b14dcf169ea15f538efb4e`  
		Last Modified: Fri, 04 Jul 2025 01:07:01 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20f59f717121556e8d36b7f829f149cee98a5b91765ac525ded0bbc2f721ac5`  
		Last Modified: Fri, 04 Jul 2025 01:07:34 GMT  
		Size: 736.1 KB (736137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276f90de6b971f3f9e70e3ba1696097f5f3def96560245a5aad168ded473ae4f`  
		Last Modified: Wed, 25 Jun 2025 20:17:19 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f70c5ea717866cfbf558c790e49f9d572116293d7a33ea61f0ecf50a0391f26`  
		Last Modified: Fri, 04 Jul 2025 01:07:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:7be3c423187b6b7aefe66fec3aa1feb1cb2834b67e171dacdf90f646ac45dd13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 KB (31241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e16759e5fd0716956d0ac4e0df53f77912ea2e6702e40264b52f53bad16fac`

```dockerfile
```

-	Layers:
	-	`sha256:5860ece640b4dd19d4fd863491c942d9b3221cea5db330975a98b7e33a0b6fc1`  
		Last Modified: Fri, 04 Jul 2025 04:13:36 GMT  
		Size: 31.2 KB (31241 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v7

```console
$ docker pull composer@sha256:5126dd2906ea0aa70d3b92f282b9deede06c5a2f35087affe12004567ef01623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73923641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7532ae5fa53b7e1a9011901a9ad57112442cb2d795d7d793ce9ab20c9e3d8aac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f4b8d7b2257f1a6ac3d6d3cc6bf9a4b64ab9fc5d2607c301f7de2c7d6c4f46`  
		Last Modified: Thu, 03 Jul 2025 23:46:20 GMT  
		Size: 13.6 MB (13647249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a41d3b4f0ee7936d37a29b00d6599e6c083cdd6c3c1e87cf67e60c78bed722f`  
		Last Modified: Thu, 03 Jul 2025 23:46:17 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f25659badae5bd6d735e7a8151332a7d70260be40b9bd15903ae5024c69186a`  
		Last Modified: Thu, 03 Jul 2025 23:46:20 GMT  
		Size: 21.0 MB (20968354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9020d050ffd80f0ec4539c880f71565ba7987609cedfc9dc9ff78af7fb53b62b`  
		Last Modified: Thu, 03 Jul 2025 23:46:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9a523c3a709bd62efada35a0a92295ac64b04640f1069b295c0d6889f2487`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210dbe376a53d9ebd8229f86a814b0d26ee3ca102f0e74c6dc09a10a9c343c58`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebcb76101e3ff8f5c34e57b65c480c0f53a9657085c1dd3571c570cc1908dec`  
		Last Modified: Fri, 04 Jul 2025 03:24:53 GMT  
		Size: 32.1 MB (32069935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7837ce17d23c46b208ed90e2deb598eb1aaed88b570cd6b34760d21674e702c`  
		Last Modified: Fri, 04 Jul 2025 03:24:49 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d785e9b0cf200ff1685ae55d7faa2405f9e64fb78a15f331451f93baaab17b9`  
		Last Modified: Fri, 04 Jul 2025 03:25:25 GMT  
		Size: 726.6 KB (726607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d692aeef38370bc31967291d9ffd1696ff481f5afbe739a8f163df32d95c75b1`  
		Last Modified: Fri, 04 Jul 2025 03:25:25 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee774b4619f4d3dd615d31e3f0504d1176c318ec6f1ecb7938d0dd6ab94ad82b`  
		Last Modified: Fri, 04 Jul 2025 03:25:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:131a147ddd7b567d6890fc9b800500b76c68e29409149eb716d8b3f434bf4c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac42b45cd5ce34b6b189a9cd88c0c1b04a7eff46694a1f119f8228ffcf31bf8`

```dockerfile
```

-	Layers:
	-	`sha256:a9c94fb0b84d765e1f9eb122c3a8ac5d1df14b248fa6962686e5162601877de8`  
		Last Modified: Fri, 04 Jul 2025 04:13:39 GMT  
		Size: 2.2 MB (2174162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f8572fb8bacd668720d79bb51ad002cedda8269000e5e3dab0c332dc554fe0e`  
		Last Modified: Fri, 04 Jul 2025 04:13:40 GMT  
		Size: 31.5 KB (31456 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:6f78a3f8c303c56a7be091143ff0db5599ce08ccd13cfd372e558abe7328a510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76557500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2f13a0ce48780f11e5201dd96d98ca037d139cc68b3a0f0487aa16f52ca969`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d74afa414d93be74315fb2fbbededff31189950343736eb9412b26b4f530d1a`  
		Last Modified: Fri, 20 Jun 2025 19:32:29 GMT  
		Size: 3.5 MB (3470712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91ea4522a211c5e50ab5b22083b52449e7ad38398a1f6e5dad24e4a62961906`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b695911010ae65b6cf4c4b5ac350b27932e3b4b29077f6094baa473db50fb5`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e2341d4b1828e7c29626f05458e9c7ac77b849f7fa211122c5e49f3db640c2`  
		Last Modified: Wed, 25 Jun 2025 19:58:30 GMT  
		Size: 13.6 MB (13640504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2214385dee2a6502125f514cfafec9ffbab10a83686ed1edebefbe13bb98e0df`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2192f9a8f7dc985e1b1534af7a423269d9525cd446882c0b66bc83bd73c1d`  
		Last Modified: Wed, 25 Jun 2025 19:58:29 GMT  
		Size: 20.5 MB (20519110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7813f4e30ce21280209e560b03ffd244261e042d03b4f926c87197d856e4d07a`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5659da52250b6def060ce2459caf69d028600439407c5609ffb01e17d290d0a`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 20.0 KB (19995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed11a0655a2eb0f0eae0b13f815d1385ec0d4bc0fc0d3e23f5c2e3aed8e1799`  
		Last Modified: Wed, 25 Jun 2025 19:58:28 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db90ec20dde1245e26657e9eeab7a68a4f381ea6442f98f105cfc54ce54e3a0b`  
		Last Modified: Thu, 26 Jun 2025 00:27:56 GMT  
		Size: 34.0 MB (34010879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb4fdb28ebd43bf90c0134d109bd7f9e79aa657ab4e9e040a42ac1d008e71aa`  
		Last Modified: Thu, 26 Jun 2025 00:27:53 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baee8ab4115a4d9d8133adbe90272c648703c8a12ab643ecd4122c342434c679`  
		Last Modified: Thu, 26 Jun 2025 00:28:29 GMT  
		Size: 735.5 KB (735527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf84df54744d3b2abb00debb5b2b31a7e8775e5254822572ec21991362ee974`  
		Last Modified: Thu, 26 Jun 2025 00:28:29 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8901fd70ed330b7c5a3bcdc084c75508be74b9581ee86c89a29bb6baf2cc0e1a`  
		Last Modified: Thu, 26 Jun 2025 00:28:29 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:5c76f497285a1f4fd7c967538065d759dac8153af07453d42c12e082ad79fb73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd48587e1c1188ba8b05675fb3ee60667ed00d2c13309d482d5a4b5dc4b86122`

```dockerfile
```

-	Layers:
	-	`sha256:06c6e79e79202258cba627965d98ff65c73706b27bada48699db9d93f30defdb`  
		Last Modified: Thu, 26 Jun 2025 01:13:33 GMT  
		Size: 2.2 MB (2173978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8034567f995258e01ffcb6dfc22497079ca859f1aa40cd36daf448fe6e682c7a`  
		Last Modified: Thu, 26 Jun 2025 01:13:33 GMT  
		Size: 31.5 KB (31475 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; 386

```console
$ docker pull composer@sha256:c834a677f11abc62dd604c47559feac6c53f14442634311bd0453c18454e3694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79800235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd09a313d040ee1722eb7d8f00b4dd0950c45d8b7ca4d8a9afdb8922ed7c0207`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4579a4802acae62f9995bc4ca35846cfa477f9a889ce0fb2017ac6630b78bd4a`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 5.8 MB (5806973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57074fe130dea7f1367879dc4bc435c31dce84ecd32b48ea0a63d35b4a08b836`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7e9cf52dab21b2f526412767a5e92e23eeb507ad11d31f9bf4391ad5eb6a66`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee47d22d22648a57b652a67b201fb0e169513c91be3eec67cb726ba70e375a83`  
		Last Modified: Thu, 03 Jul 2025 23:05:02 GMT  
		Size: 13.6 MB (13647238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ed9c7929ede2d39288b5cdc1a881693463f9694eab366fbb269e70c0d92a49`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63b1c24d7566d919e950b1eaf0a78b66a3bebc8b853f7dac99909776dbae0f1`  
		Last Modified: Thu, 03 Jul 2025 23:05:04 GMT  
		Size: 21.5 MB (21500663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f235298ca3bcb11577f52427a9e9abe5f5708168ce3e6f7a92e3516e12f33f6`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3069db4b5ea73d2b8c2f80770d98b1ecf8fc539f7fcb87b04c2a4d4c1d2747`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 20.2 KB (20195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af93b74a51d1b8b0d9adaa24d025147b9bbb65f3dea67b796f0959416093750`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 20.2 KB (20192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf453c1071c792beaa5267fdd052480889666839d63b36c3c72c8b405741dcb`  
		Last Modified: Thu, 03 Jul 2025 23:12:03 GMT  
		Size: 34.4 MB (34436750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbbd4849c630a412f4eaa507248cbc656e68a623f0cf27d61c333de4853bfc4`  
		Last Modified: Thu, 03 Jul 2025 23:12:01 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59574e203c63533c068a2d8001b555b8afde4d12b2620cef6c81b561971196a0`  
		Last Modified: Thu, 03 Jul 2025 23:12:01 GMT  
		Size: 747.4 KB (747353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db41c9e62300962a9037fc2e22ade4099ece56dccf7bdb54621bbd51da0e0ea`  
		Last Modified: Thu, 03 Jul 2025 23:12:00 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138472a9b76e193c0429098e29aea1bb89935127ce211bda33b07bc7ede3a9ea`  
		Last Modified: Thu, 03 Jul 2025 23:12:00 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:bf0ab8f634046057fda6d729e288a40f1b65a47e2b0c075f49319a649e1aabd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f1a214eb061abc166bd8fa85807028d873d081cae27e506444370ded39a6b9`

```dockerfile
```

-	Layers:
	-	`sha256:03bf3d77e2ad0c1e638f43456b3ed9aa74deef374191c89cfa9beebfacb757ca`  
		Last Modified: Fri, 04 Jul 2025 01:13:44 GMT  
		Size: 2.2 MB (2173634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:766db42ebc4acb8d84cd48ad3a8a7a38cb3805760dbd486132ef08d3e4f0854c`  
		Last Modified: Fri, 04 Jul 2025 01:13:45 GMT  
		Size: 31.3 KB (31331 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; ppc64le

```console
$ docker pull composer@sha256:d2860483ff6060e4f34718f3569976c580e55a019d321056c10b09aa7a2db417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81267874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc71c021dfae7f4d4c67e985475e3acdb6199aef0d087e89c012862399cb9d63`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7db3af28cc31124a8bce98c13cd1b2512963d13f437d0d67f9918df0d57d2b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 5.9 MB (5946924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ec39d79edfa484fac002ed8c640f17ae8077df4dce88811d8d186865593a6b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 939.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2995d4272705fc452f2b3ea9e2d118681efbad9f858c7743f6f69364d73a50`  
		Last Modified: Thu, 03 Jul 2025 23:15:35 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da4669ab0266f9dd895304e7c92d52e7df1b0acfdc30e6abf0d73fd20c6d09a`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 13.6 MB (13647243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdb584c1e59e66bf7047b954cfc1e41ae7df62560b963934f349b9bd0a11fed`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dff158c4fec087bdd22d80d469c14bd7f5e8a7d72d9a682db56d77c7977e55f`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 21.9 MB (21877134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa09d11c80e8896e162d36345eb3a1cf062f1ba207ed29c537b7783eb818f415`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09daff9fd7af3987bc24f46923dc89bca4e186069874ea11f88390e02dbca5a8`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1d9e25cff60aeed589359ca184c52454f63361a6309e3c363d0d97c227e006`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcefe2124ab8f2442794aaabac7f9422c8d266cee3bbfbb30c3cea3b0f0943f6`  
		Last Modified: Fri, 04 Jul 2025 02:29:48 GMT  
		Size: 35.3 MB (35279082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7315eb9406973e6ea300692e85a137454ee79d74bbb5b71ff352feab46e7c24`  
		Last Modified: Fri, 04 Jul 2025 02:29:46 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8b488c3c48b62f7ab37e985c2badc46f00121932cb154e4c6e36f76d40bfca`  
		Last Modified: Fri, 04 Jul 2025 02:31:05 GMT  
		Size: 742.5 KB (742455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a966f4fe56f65e15c55c3975d12cb9baf1b5c6893ba5bed2c3b5f6b74ddccd40`  
		Last Modified: Fri, 04 Jul 2025 02:31:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd6dfba27b8043e866d82286d5dab18f70e2226534b19ac2cce95405c87540f`  
		Last Modified: Fri, 04 Jul 2025 02:31:04 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:8a118c282313d5577c6373b17ef7c184cf27eb59f005a9a658ae088cc47f9548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f815fcffd01d9c4289ae0764dba6704ac9735b4f0280af9289068ce054e0818`

```dockerfile
```

-	Layers:
	-	`sha256:c4e95040e7a37340deb333374f4c71ca1bddc12735d7a81ad3ebc0caffe12181`  
		Last Modified: Fri, 04 Jul 2025 04:13:48 GMT  
		Size: 2.2 MB (2172403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ee97024ceab90c82bd9689466e8e666002355a9faf7b09be18680b02b1f80b`  
		Last Modified: Fri, 04 Jul 2025 04:13:49 GMT  
		Size: 31.4 KB (31404 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; riscv64

```console
$ docker pull composer@sha256:30fb2195c5a22c9ccafe97ba65907700f5c297078b2243383db0957e71db6017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73032087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31f73171ecf1f713aeb4422a5fd753725f8e97ed92f049c8512adf0094deb36`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d0224769088850e26eb3ba2638a8a3febc4b65991ac8cc63dc3f29cf199070`  
		Last Modified: Wed, 11 Jun 2025 05:05:11 GMT  
		Size: 13.6 MB (13640513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a45f979f3844cfaf9ad9f1a00668b3bb56bc478c711f2d939a7dba0c2ed6e1`  
		Last Modified: Wed, 11 Jun 2025 02:39:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b864e2d5fb63463e7b594794f1b0077ef70793371e80280a29b09008bb9771a`  
		Last Modified: Wed, 11 Jun 2025 05:05:14 GMT  
		Size: 20.4 MB (20388593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91ae988832dcf22e179ec800eee279369b0d1b8a4129c2bd761a392671d8d32`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5d276f1eb8afbe6e12101788a8d8d2c68f0875a801fca945c95b68b009ee44`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033c69f0ad5808ebac07aefd6d1a9c0933c09e134334a8bd72a2f49fb7ed2297`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 20.0 KB (19999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7d4367f9b25dba1c9057a363403805d1f3ffce81d401bb89eaa3652ee82d83`  
		Last Modified: Thu, 26 Jun 2025 08:33:02 GMT  
		Size: 31.1 MB (31107678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a85da3fdbf5b1c41e6f68043dc7ff3cb2ef316082fa092b6f23657dffda19a1`  
		Last Modified: Thu, 26 Jun 2025 08:32:59 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18adcae7f1301b51ee2fc7abe3a5ce5b41d0acd2549ba9fe655330926b23f83c`  
		Last Modified: Thu, 26 Jun 2025 08:38:00 GMT  
		Size: 733.3 KB (733287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419c8793715002635b6ef09089a9180fb4f05a4ee2870a69fbd1c886d3ed7d69`  
		Last Modified: Thu, 26 Jun 2025 08:37:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca1d976b231d6201f5a449befa42f9bdd9c97f36514186c9c4abe8b008411fb`  
		Last Modified: Thu, 26 Jun 2025 08:37:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:7a4a7a6ebb740b9d07f2583f86c75629d5c5746d3ff061a727a55bda778933e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559ec2767071294375a43ba468a5bf5f3efd68fbe1ec44023e13e3bbcf42004b`

```dockerfile
```

-	Layers:
	-	`sha256:fe0803650cefb94ad050ee3b4f9db347ce916801dda1460eec5a7de38d5007b2`  
		Last Modified: Thu, 26 Jun 2025 10:13:41 GMT  
		Size: 2.2 MB (2170662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74d8acc9b7a1210df34ca548487e8756be0cdb63077782f3fe64a13a23fea002`  
		Last Modified: Thu, 26 Jun 2025 10:13:42 GMT  
		Size: 31.4 KB (31395 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; s390x

```console
$ docker pull composer@sha256:1f23418422d093e8f10d6041dec54961710565294dc08c939ce976614a3109e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77300564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0014ddd15a5086ca882213cb209e9aac9133d438d03d1fd4b97e1406732f9764`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abd3e67b018bcd8c0aa4d0434d7ec04dcdb3a3cfbf444a313e2be49d0524ec2`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 5.9 MB (5932552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f41e4866617495859c5133b898f769b3867a6a3ae061aa9561da765981c5ad`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9335ac6e22dd0c0b2e07f4a5406c437168067a987662ebd8bcd3b269496018`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da3506587d8ded424a7c5730d972ae6f1735f6afc1a325c7e9f83474f399fde`  
		Last Modified: Thu, 03 Jul 2025 23:16:27 GMT  
		Size: 13.6 MB (13647264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671a375a1790dbb9b0d83c7dd0560e7f6e75fb5b06afbc76019557052c897e5a`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dc301a9ae8a743478269ed0a476a3abb5ea1e3f156da87ce855397d9ddef91`  
		Last Modified: Thu, 03 Jul 2025 23:16:26 GMT  
		Size: 21.5 MB (21450357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1074498264e134b44d0edcde237cf3cfadba39197115581cfd4b9a9c5ba0fa`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1658861fe310f53081a1e605b2427a938ceddc66bacb97178d77404b333d65a1`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105bedc3ea3fb0ab6591d908f480b2bb3c119411d1ba9dc0c0e9fd62b45f2a39`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb11fbf2308810b649dff18139a7f4e9d809ae768cc36f3d15ec258497a33363`  
		Last Modified: Fri, 04 Jul 2025 02:05:49 GMT  
		Size: 31.8 MB (31839057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb18554f4af212841fd6225002512ce8150b2738e7c8d62528fee75319d8df8`  
		Last Modified: Fri, 04 Jul 2025 02:05:34 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e98fe8743070c639f8eb2ee4894e447b51c5fc9dae60c1e8a14c66697980da1`  
		Last Modified: Fri, 04 Jul 2025 02:06:20 GMT  
		Size: 739.0 KB (738958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c01d00f55b0e2dfa94ad1229e9a69a8a4fe4d4ea6ae5350e1a2227a5689d5f8`  
		Last Modified: Fri, 04 Jul 2025 02:12:39 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7894d22dfb6f29a3a6244074426e8a44f24ce03291d76f60267d87fd135970ad`  
		Last Modified: Fri, 04 Jul 2025 02:06:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:0d29e14172dd031e7e6b8e41b50e5f147b836d09e21a3a13be04fa8f2d95b170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195f0233b1e45e2ea78e00f2b80ad2e8458288518f4e002b1375cd29157e2471`

```dockerfile
```

-	Layers:
	-	`sha256:c66ffdf527f5d5849190b5cbf71d176f2c1d1b63f83f5624d7cc1fa06167864b`  
		Last Modified: Fri, 04 Jul 2025 04:13:55 GMT  
		Size: 2.2 MB (2170458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e6e936165c4495ba9d28088542473a1a3bcaddbf4e09d4267f77f963e223044`  
		Last Modified: Fri, 04 Jul 2025 04:13:56 GMT  
		Size: 31.4 KB (31361 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10`

```console
$ docker pull composer@sha256:e48b612b785dcb1f6fd5e34130da038bb745c0d3a570ec69c9d0b8a48b41b22e
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
$ docker pull composer@sha256:44ea0b30fd71ae7703321bd4e235db261ea62295cc5d4a547457ccb41e408a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79068992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b090bbb72095287470c965696b7b90b3a0c9e664287a78a2d6624ad1c0bd1c40`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b94662290ef2237915af922ad14ae2b406eccea26d9201aa949ea52f20b737f`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 5.9 MB (5944403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498a67832465ef6dae00170ccca088bdbc63d05a197e0ba1403442805169a06a`  
		Last Modified: Thu, 03 Jul 2025 23:04:16 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53785dc48fc021d1c3f9c46a776ead61a024377fb5e6ab592908501762d63a7`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c87a7802578b0a5aebb57ffea8e543a2d50cff1ec6ffb0941fe8ad61b3a9e6`  
		Last Modified: Thu, 03 Jul 2025 23:04:23 GMT  
		Size: 13.6 MB (13647262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5aa21d09531523ae5c279a8b0eb00236af3b192f428c934050c61f7e1611eaa`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fccbfd125531b00b24f5c4c9c182e17714478e55b96701b7e71d30f7f70f9b`  
		Last Modified: Thu, 03 Jul 2025 23:04:28 GMT  
		Size: 21.0 MB (20971251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481b52666b981ec99f99b98b64ef13ff6ce799950970b68817767c966318dc11`  
		Last Modified: Thu, 03 Jul 2025 23:04:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a3724a01f76e5128bdebeeb89d8f42b63b2e987403c91e1f1f5c084c63ffee`  
		Last Modified: Thu, 03 Jul 2025 23:04:22 GMT  
		Size: 20.2 KB (20205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755a5679cebfbcec196508684d58f3d3479a8923825702cea8057be9ea0509ea`  
		Last Modified: Thu, 03 Jul 2025 23:04:25 GMT  
		Size: 20.2 KB (20204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c702e8f6c7cead92f757244a0e08915ffffe43fbe74a0923d30c01f2d9c90c37`  
		Last Modified: Thu, 03 Jul 2025 23:13:14 GMT  
		Size: 33.9 MB (33928442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688d6535fcb8eb0d12463480f6752f4e9bb65bf9267be71c1587b3f945b1941d`  
		Last Modified: Thu, 03 Jul 2025 23:13:11 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c39dd4f0d2117bc5a02bbb5192170fe65e2f0c2302b01c95ef6adb829ef689a`  
		Last Modified: Thu, 03 Jul 2025 23:13:12 GMT  
		Size: 735.5 KB (735538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a74b619e9325ae8e5b5adb511075d9c35247e8de5593f5996184112a115ffd`  
		Last Modified: Thu, 03 Jul 2025 23:13:12 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78d5acf69b51a1fe4d9f67ce5f26c6f01d2cf6d3a8795c5edf5de1e03843b82`  
		Last Modified: Thu, 03 Jul 2025 23:13:12 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:a40b0954587af3d3cb6506954d3609818942e2626e2b484baf5ef32e2f758fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7630f9c336baad52d91c577df4c2b82980a9e7c11823385c876e62a4c3b82ec1`

```dockerfile
```

-	Layers:
	-	`sha256:68699c3048c4af9b4b3b9cd8448d2ecf4689d835321caf458ead0ae588cd8895`  
		Last Modified: Fri, 04 Jul 2025 01:13:29 GMT  
		Size: 2.2 MB (2173846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7afc7d1b68b82c353c58c33175613c1fcaa298adaa6a87175e82c63e7a485b0f`  
		Last Modified: Fri, 04 Jul 2025 01:13:30 GMT  
		Size: 31.4 KB (31362 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v6

```console
$ docker pull composer@sha256:c04f5f68a1cd6b21b39fa9629ec09c04ea7a0a61ab085c5a39c2bc78a0218b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77384933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b662652d26f29a2cf473a00d55c6e7d3a5daacd4df84871a99ded37edfb7ab9c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4a1a48d371204daac6d50cf0ade3fcbe953b7326556c347d0834eeb808b22f`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 13.6 MB (13647232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7209fb73f851518e0fbc85b54004a573116286207c48ee96ab37833cb8ea1353`  
		Last Modified: Thu, 03 Jul 2025 23:00:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7698dfdb6ae14586a077f81a7e7531ba3d394ab385475ff9c6573114a36ad047`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 22.2 MB (22216193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2822e518605b3410372bbcdb567b3220dcdbe3fc3a85d76aeeed7414a97ce84`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc23f56a1dfd1eb937c6d0d63cb116029d4ac6193e3b8e0487798f7859b09cf`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb672fb64a4977b38f156870ac6fd28ad3898b39594ead2e5d7a7a25cf62e07a`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f65dda0589cf68df6c1f7a31f2ed36448fe5ac89816b32bef12a62b39575a0`  
		Last Modified: Fri, 04 Jul 2025 01:07:05 GMT  
		Size: 33.8 MB (33807127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af16e8c9f29c59fdf9ae69e6ad7a7f42c68aea017b14dcf169ea15f538efb4e`  
		Last Modified: Fri, 04 Jul 2025 01:07:01 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20f59f717121556e8d36b7f829f149cee98a5b91765ac525ded0bbc2f721ac5`  
		Last Modified: Fri, 04 Jul 2025 01:07:34 GMT  
		Size: 736.1 KB (736137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276f90de6b971f3f9e70e3ba1696097f5f3def96560245a5aad168ded473ae4f`  
		Last Modified: Wed, 25 Jun 2025 20:17:19 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f70c5ea717866cfbf558c790e49f9d572116293d7a33ea61f0ecf50a0391f26`  
		Last Modified: Fri, 04 Jul 2025 01:07:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:7be3c423187b6b7aefe66fec3aa1feb1cb2834b67e171dacdf90f646ac45dd13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 KB (31241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e16759e5fd0716956d0ac4e0df53f77912ea2e6702e40264b52f53bad16fac`

```dockerfile
```

-	Layers:
	-	`sha256:5860ece640b4dd19d4fd863491c942d9b3221cea5db330975a98b7e33a0b6fc1`  
		Last Modified: Fri, 04 Jul 2025 04:13:36 GMT  
		Size: 31.2 KB (31241 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v7

```console
$ docker pull composer@sha256:5126dd2906ea0aa70d3b92f282b9deede06c5a2f35087affe12004567ef01623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73923641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7532ae5fa53b7e1a9011901a9ad57112442cb2d795d7d793ce9ab20c9e3d8aac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f4b8d7b2257f1a6ac3d6d3cc6bf9a4b64ab9fc5d2607c301f7de2c7d6c4f46`  
		Last Modified: Thu, 03 Jul 2025 23:46:20 GMT  
		Size: 13.6 MB (13647249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a41d3b4f0ee7936d37a29b00d6599e6c083cdd6c3c1e87cf67e60c78bed722f`  
		Last Modified: Thu, 03 Jul 2025 23:46:17 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f25659badae5bd6d735e7a8151332a7d70260be40b9bd15903ae5024c69186a`  
		Last Modified: Thu, 03 Jul 2025 23:46:20 GMT  
		Size: 21.0 MB (20968354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9020d050ffd80f0ec4539c880f71565ba7987609cedfc9dc9ff78af7fb53b62b`  
		Last Modified: Thu, 03 Jul 2025 23:46:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9a523c3a709bd62efada35a0a92295ac64b04640f1069b295c0d6889f2487`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210dbe376a53d9ebd8229f86a814b0d26ee3ca102f0e74c6dc09a10a9c343c58`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebcb76101e3ff8f5c34e57b65c480c0f53a9657085c1dd3571c570cc1908dec`  
		Last Modified: Fri, 04 Jul 2025 03:24:53 GMT  
		Size: 32.1 MB (32069935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7837ce17d23c46b208ed90e2deb598eb1aaed88b570cd6b34760d21674e702c`  
		Last Modified: Fri, 04 Jul 2025 03:24:49 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d785e9b0cf200ff1685ae55d7faa2405f9e64fb78a15f331451f93baaab17b9`  
		Last Modified: Fri, 04 Jul 2025 03:25:25 GMT  
		Size: 726.6 KB (726607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d692aeef38370bc31967291d9ffd1696ff481f5afbe739a8f163df32d95c75b1`  
		Last Modified: Fri, 04 Jul 2025 03:25:25 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee774b4619f4d3dd615d31e3f0504d1176c318ec6f1ecb7938d0dd6ab94ad82b`  
		Last Modified: Fri, 04 Jul 2025 03:25:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:131a147ddd7b567d6890fc9b800500b76c68e29409149eb716d8b3f434bf4c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac42b45cd5ce34b6b189a9cd88c0c1b04a7eff46694a1f119f8228ffcf31bf8`

```dockerfile
```

-	Layers:
	-	`sha256:a9c94fb0b84d765e1f9eb122c3a8ac5d1df14b248fa6962686e5162601877de8`  
		Last Modified: Fri, 04 Jul 2025 04:13:39 GMT  
		Size: 2.2 MB (2174162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f8572fb8bacd668720d79bb51ad002cedda8269000e5e3dab0c332dc554fe0e`  
		Last Modified: Fri, 04 Jul 2025 04:13:40 GMT  
		Size: 31.5 KB (31456 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:6f78a3f8c303c56a7be091143ff0db5599ce08ccd13cfd372e558abe7328a510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76557500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2f13a0ce48780f11e5201dd96d98ca037d139cc68b3a0f0487aa16f52ca969`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d74afa414d93be74315fb2fbbededff31189950343736eb9412b26b4f530d1a`  
		Last Modified: Fri, 20 Jun 2025 19:32:29 GMT  
		Size: 3.5 MB (3470712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91ea4522a211c5e50ab5b22083b52449e7ad38398a1f6e5dad24e4a62961906`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b695911010ae65b6cf4c4b5ac350b27932e3b4b29077f6094baa473db50fb5`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e2341d4b1828e7c29626f05458e9c7ac77b849f7fa211122c5e49f3db640c2`  
		Last Modified: Wed, 25 Jun 2025 19:58:30 GMT  
		Size: 13.6 MB (13640504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2214385dee2a6502125f514cfafec9ffbab10a83686ed1edebefbe13bb98e0df`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2192f9a8f7dc985e1b1534af7a423269d9525cd446882c0b66bc83bd73c1d`  
		Last Modified: Wed, 25 Jun 2025 19:58:29 GMT  
		Size: 20.5 MB (20519110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7813f4e30ce21280209e560b03ffd244261e042d03b4f926c87197d856e4d07a`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5659da52250b6def060ce2459caf69d028600439407c5609ffb01e17d290d0a`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 20.0 KB (19995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed11a0655a2eb0f0eae0b13f815d1385ec0d4bc0fc0d3e23f5c2e3aed8e1799`  
		Last Modified: Wed, 25 Jun 2025 19:58:28 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db90ec20dde1245e26657e9eeab7a68a4f381ea6442f98f105cfc54ce54e3a0b`  
		Last Modified: Thu, 26 Jun 2025 00:27:56 GMT  
		Size: 34.0 MB (34010879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb4fdb28ebd43bf90c0134d109bd7f9e79aa657ab4e9e040a42ac1d008e71aa`  
		Last Modified: Thu, 26 Jun 2025 00:27:53 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baee8ab4115a4d9d8133adbe90272c648703c8a12ab643ecd4122c342434c679`  
		Last Modified: Thu, 26 Jun 2025 00:28:29 GMT  
		Size: 735.5 KB (735527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf84df54744d3b2abb00debb5b2b31a7e8775e5254822572ec21991362ee974`  
		Last Modified: Thu, 26 Jun 2025 00:28:29 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8901fd70ed330b7c5a3bcdc084c75508be74b9581ee86c89a29bb6baf2cc0e1a`  
		Last Modified: Thu, 26 Jun 2025 00:28:29 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:5c76f497285a1f4fd7c967538065d759dac8153af07453d42c12e082ad79fb73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd48587e1c1188ba8b05675fb3ee60667ed00d2c13309d482d5a4b5dc4b86122`

```dockerfile
```

-	Layers:
	-	`sha256:06c6e79e79202258cba627965d98ff65c73706b27bada48699db9d93f30defdb`  
		Last Modified: Thu, 26 Jun 2025 01:13:33 GMT  
		Size: 2.2 MB (2173978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8034567f995258e01ffcb6dfc22497079ca859f1aa40cd36daf448fe6e682c7a`  
		Last Modified: Thu, 26 Jun 2025 01:13:33 GMT  
		Size: 31.5 KB (31475 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; 386

```console
$ docker pull composer@sha256:c834a677f11abc62dd604c47559feac6c53f14442634311bd0453c18454e3694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79800235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd09a313d040ee1722eb7d8f00b4dd0950c45d8b7ca4d8a9afdb8922ed7c0207`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4579a4802acae62f9995bc4ca35846cfa477f9a889ce0fb2017ac6630b78bd4a`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 5.8 MB (5806973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57074fe130dea7f1367879dc4bc435c31dce84ecd32b48ea0a63d35b4a08b836`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7e9cf52dab21b2f526412767a5e92e23eeb507ad11d31f9bf4391ad5eb6a66`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee47d22d22648a57b652a67b201fb0e169513c91be3eec67cb726ba70e375a83`  
		Last Modified: Thu, 03 Jul 2025 23:05:02 GMT  
		Size: 13.6 MB (13647238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ed9c7929ede2d39288b5cdc1a881693463f9694eab366fbb269e70c0d92a49`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63b1c24d7566d919e950b1eaf0a78b66a3bebc8b853f7dac99909776dbae0f1`  
		Last Modified: Thu, 03 Jul 2025 23:05:04 GMT  
		Size: 21.5 MB (21500663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f235298ca3bcb11577f52427a9e9abe5f5708168ce3e6f7a92e3516e12f33f6`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3069db4b5ea73d2b8c2f80770d98b1ecf8fc539f7fcb87b04c2a4d4c1d2747`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 20.2 KB (20195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af93b74a51d1b8b0d9adaa24d025147b9bbb65f3dea67b796f0959416093750`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 20.2 KB (20192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf453c1071c792beaa5267fdd052480889666839d63b36c3c72c8b405741dcb`  
		Last Modified: Thu, 03 Jul 2025 23:12:03 GMT  
		Size: 34.4 MB (34436750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbbd4849c630a412f4eaa507248cbc656e68a623f0cf27d61c333de4853bfc4`  
		Last Modified: Thu, 03 Jul 2025 23:12:01 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59574e203c63533c068a2d8001b555b8afde4d12b2620cef6c81b561971196a0`  
		Last Modified: Thu, 03 Jul 2025 23:12:01 GMT  
		Size: 747.4 KB (747353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db41c9e62300962a9037fc2e22ade4099ece56dccf7bdb54621bbd51da0e0ea`  
		Last Modified: Thu, 03 Jul 2025 23:12:00 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138472a9b76e193c0429098e29aea1bb89935127ce211bda33b07bc7ede3a9ea`  
		Last Modified: Thu, 03 Jul 2025 23:12:00 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:bf0ab8f634046057fda6d729e288a40f1b65a47e2b0c075f49319a649e1aabd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f1a214eb061abc166bd8fa85807028d873d081cae27e506444370ded39a6b9`

```dockerfile
```

-	Layers:
	-	`sha256:03bf3d77e2ad0c1e638f43456b3ed9aa74deef374191c89cfa9beebfacb757ca`  
		Last Modified: Fri, 04 Jul 2025 01:13:44 GMT  
		Size: 2.2 MB (2173634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:766db42ebc4acb8d84cd48ad3a8a7a38cb3805760dbd486132ef08d3e4f0854c`  
		Last Modified: Fri, 04 Jul 2025 01:13:45 GMT  
		Size: 31.3 KB (31331 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; ppc64le

```console
$ docker pull composer@sha256:d2860483ff6060e4f34718f3569976c580e55a019d321056c10b09aa7a2db417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81267874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc71c021dfae7f4d4c67e985475e3acdb6199aef0d087e89c012862399cb9d63`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7db3af28cc31124a8bce98c13cd1b2512963d13f437d0d67f9918df0d57d2b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 5.9 MB (5946924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ec39d79edfa484fac002ed8c640f17ae8077df4dce88811d8d186865593a6b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 939.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2995d4272705fc452f2b3ea9e2d118681efbad9f858c7743f6f69364d73a50`  
		Last Modified: Thu, 03 Jul 2025 23:15:35 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da4669ab0266f9dd895304e7c92d52e7df1b0acfdc30e6abf0d73fd20c6d09a`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 13.6 MB (13647243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdb584c1e59e66bf7047b954cfc1e41ae7df62560b963934f349b9bd0a11fed`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dff158c4fec087bdd22d80d469c14bd7f5e8a7d72d9a682db56d77c7977e55f`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 21.9 MB (21877134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa09d11c80e8896e162d36345eb3a1cf062f1ba207ed29c537b7783eb818f415`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09daff9fd7af3987bc24f46923dc89bca4e186069874ea11f88390e02dbca5a8`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1d9e25cff60aeed589359ca184c52454f63361a6309e3c363d0d97c227e006`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcefe2124ab8f2442794aaabac7f9422c8d266cee3bbfbb30c3cea3b0f0943f6`  
		Last Modified: Fri, 04 Jul 2025 02:29:48 GMT  
		Size: 35.3 MB (35279082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7315eb9406973e6ea300692e85a137454ee79d74bbb5b71ff352feab46e7c24`  
		Last Modified: Fri, 04 Jul 2025 02:29:46 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8b488c3c48b62f7ab37e985c2badc46f00121932cb154e4c6e36f76d40bfca`  
		Last Modified: Fri, 04 Jul 2025 02:31:05 GMT  
		Size: 742.5 KB (742455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a966f4fe56f65e15c55c3975d12cb9baf1b5c6893ba5bed2c3b5f6b74ddccd40`  
		Last Modified: Fri, 04 Jul 2025 02:31:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd6dfba27b8043e866d82286d5dab18f70e2226534b19ac2cce95405c87540f`  
		Last Modified: Fri, 04 Jul 2025 02:31:04 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:8a118c282313d5577c6373b17ef7c184cf27eb59f005a9a658ae088cc47f9548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f815fcffd01d9c4289ae0764dba6704ac9735b4f0280af9289068ce054e0818`

```dockerfile
```

-	Layers:
	-	`sha256:c4e95040e7a37340deb333374f4c71ca1bddc12735d7a81ad3ebc0caffe12181`  
		Last Modified: Fri, 04 Jul 2025 04:13:48 GMT  
		Size: 2.2 MB (2172403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ee97024ceab90c82bd9689466e8e666002355a9faf7b09be18680b02b1f80b`  
		Last Modified: Fri, 04 Jul 2025 04:13:49 GMT  
		Size: 31.4 KB (31404 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; riscv64

```console
$ docker pull composer@sha256:30fb2195c5a22c9ccafe97ba65907700f5c297078b2243383db0957e71db6017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73032087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31f73171ecf1f713aeb4422a5fd753725f8e97ed92f049c8512adf0094deb36`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d0224769088850e26eb3ba2638a8a3febc4b65991ac8cc63dc3f29cf199070`  
		Last Modified: Wed, 11 Jun 2025 05:05:11 GMT  
		Size: 13.6 MB (13640513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a45f979f3844cfaf9ad9f1a00668b3bb56bc478c711f2d939a7dba0c2ed6e1`  
		Last Modified: Wed, 11 Jun 2025 02:39:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b864e2d5fb63463e7b594794f1b0077ef70793371e80280a29b09008bb9771a`  
		Last Modified: Wed, 11 Jun 2025 05:05:14 GMT  
		Size: 20.4 MB (20388593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91ae988832dcf22e179ec800eee279369b0d1b8a4129c2bd761a392671d8d32`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5d276f1eb8afbe6e12101788a8d8d2c68f0875a801fca945c95b68b009ee44`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033c69f0ad5808ebac07aefd6d1a9c0933c09e134334a8bd72a2f49fb7ed2297`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 20.0 KB (19999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7d4367f9b25dba1c9057a363403805d1f3ffce81d401bb89eaa3652ee82d83`  
		Last Modified: Thu, 26 Jun 2025 08:33:02 GMT  
		Size: 31.1 MB (31107678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a85da3fdbf5b1c41e6f68043dc7ff3cb2ef316082fa092b6f23657dffda19a1`  
		Last Modified: Thu, 26 Jun 2025 08:32:59 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18adcae7f1301b51ee2fc7abe3a5ce5b41d0acd2549ba9fe655330926b23f83c`  
		Last Modified: Thu, 26 Jun 2025 08:38:00 GMT  
		Size: 733.3 KB (733287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419c8793715002635b6ef09089a9180fb4f05a4ee2870a69fbd1c886d3ed7d69`  
		Last Modified: Thu, 26 Jun 2025 08:37:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca1d976b231d6201f5a449befa42f9bdd9c97f36514186c9c4abe8b008411fb`  
		Last Modified: Thu, 26 Jun 2025 08:37:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:7a4a7a6ebb740b9d07f2583f86c75629d5c5746d3ff061a727a55bda778933e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559ec2767071294375a43ba468a5bf5f3efd68fbe1ec44023e13e3bbcf42004b`

```dockerfile
```

-	Layers:
	-	`sha256:fe0803650cefb94ad050ee3b4f9db347ce916801dda1460eec5a7de38d5007b2`  
		Last Modified: Thu, 26 Jun 2025 10:13:41 GMT  
		Size: 2.2 MB (2170662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74d8acc9b7a1210df34ca548487e8756be0cdb63077782f3fe64a13a23fea002`  
		Last Modified: Thu, 26 Jun 2025 10:13:42 GMT  
		Size: 31.4 KB (31395 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; s390x

```console
$ docker pull composer@sha256:1f23418422d093e8f10d6041dec54961710565294dc08c939ce976614a3109e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77300564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0014ddd15a5086ca882213cb209e9aac9133d438d03d1fd4b97e1406732f9764`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abd3e67b018bcd8c0aa4d0434d7ec04dcdb3a3cfbf444a313e2be49d0524ec2`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 5.9 MB (5932552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f41e4866617495859c5133b898f769b3867a6a3ae061aa9561da765981c5ad`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9335ac6e22dd0c0b2e07f4a5406c437168067a987662ebd8bcd3b269496018`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da3506587d8ded424a7c5730d972ae6f1735f6afc1a325c7e9f83474f399fde`  
		Last Modified: Thu, 03 Jul 2025 23:16:27 GMT  
		Size: 13.6 MB (13647264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671a375a1790dbb9b0d83c7dd0560e7f6e75fb5b06afbc76019557052c897e5a`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dc301a9ae8a743478269ed0a476a3abb5ea1e3f156da87ce855397d9ddef91`  
		Last Modified: Thu, 03 Jul 2025 23:16:26 GMT  
		Size: 21.5 MB (21450357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1074498264e134b44d0edcde237cf3cfadba39197115581cfd4b9a9c5ba0fa`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1658861fe310f53081a1e605b2427a938ceddc66bacb97178d77404b333d65a1`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105bedc3ea3fb0ab6591d908f480b2bb3c119411d1ba9dc0c0e9fd62b45f2a39`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb11fbf2308810b649dff18139a7f4e9d809ae768cc36f3d15ec258497a33363`  
		Last Modified: Fri, 04 Jul 2025 02:05:49 GMT  
		Size: 31.8 MB (31839057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb18554f4af212841fd6225002512ce8150b2738e7c8d62528fee75319d8df8`  
		Last Modified: Fri, 04 Jul 2025 02:05:34 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e98fe8743070c639f8eb2ee4894e447b51c5fc9dae60c1e8a14c66697980da1`  
		Last Modified: Fri, 04 Jul 2025 02:06:20 GMT  
		Size: 739.0 KB (738958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c01d00f55b0e2dfa94ad1229e9a69a8a4fe4d4ea6ae5350e1a2227a5689d5f8`  
		Last Modified: Fri, 04 Jul 2025 02:12:39 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7894d22dfb6f29a3a6244074426e8a44f24ce03291d76f60267d87fd135970ad`  
		Last Modified: Fri, 04 Jul 2025 02:06:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:0d29e14172dd031e7e6b8e41b50e5f147b836d09e21a3a13be04fa8f2d95b170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195f0233b1e45e2ea78e00f2b80ad2e8458288518f4e002b1375cd29157e2471`

```dockerfile
```

-	Layers:
	-	`sha256:c66ffdf527f5d5849190b5cbf71d176f2c1d1b63f83f5624d7cc1fa06167864b`  
		Last Modified: Fri, 04 Jul 2025 04:13:55 GMT  
		Size: 2.2 MB (2170458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e6e936165c4495ba9d28088542473a1a3bcaddbf4e09d4267f77f963e223044`  
		Last Modified: Fri, 04 Jul 2025 04:13:56 GMT  
		Size: 31.4 KB (31361 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10.27`

```console
$ docker pull composer@sha256:e48b612b785dcb1f6fd5e34130da038bb745c0d3a570ec69c9d0b8a48b41b22e
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
$ docker pull composer@sha256:44ea0b30fd71ae7703321bd4e235db261ea62295cc5d4a547457ccb41e408a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79068992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b090bbb72095287470c965696b7b90b3a0c9e664287a78a2d6624ad1c0bd1c40`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b94662290ef2237915af922ad14ae2b406eccea26d9201aa949ea52f20b737f`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 5.9 MB (5944403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498a67832465ef6dae00170ccca088bdbc63d05a197e0ba1403442805169a06a`  
		Last Modified: Thu, 03 Jul 2025 23:04:16 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53785dc48fc021d1c3f9c46a776ead61a024377fb5e6ab592908501762d63a7`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c87a7802578b0a5aebb57ffea8e543a2d50cff1ec6ffb0941fe8ad61b3a9e6`  
		Last Modified: Thu, 03 Jul 2025 23:04:23 GMT  
		Size: 13.6 MB (13647262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5aa21d09531523ae5c279a8b0eb00236af3b192f428c934050c61f7e1611eaa`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fccbfd125531b00b24f5c4c9c182e17714478e55b96701b7e71d30f7f70f9b`  
		Last Modified: Thu, 03 Jul 2025 23:04:28 GMT  
		Size: 21.0 MB (20971251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481b52666b981ec99f99b98b64ef13ff6ce799950970b68817767c966318dc11`  
		Last Modified: Thu, 03 Jul 2025 23:04:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a3724a01f76e5128bdebeeb89d8f42b63b2e987403c91e1f1f5c084c63ffee`  
		Last Modified: Thu, 03 Jul 2025 23:04:22 GMT  
		Size: 20.2 KB (20205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755a5679cebfbcec196508684d58f3d3479a8923825702cea8057be9ea0509ea`  
		Last Modified: Thu, 03 Jul 2025 23:04:25 GMT  
		Size: 20.2 KB (20204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c702e8f6c7cead92f757244a0e08915ffffe43fbe74a0923d30c01f2d9c90c37`  
		Last Modified: Thu, 03 Jul 2025 23:13:14 GMT  
		Size: 33.9 MB (33928442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688d6535fcb8eb0d12463480f6752f4e9bb65bf9267be71c1587b3f945b1941d`  
		Last Modified: Thu, 03 Jul 2025 23:13:11 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c39dd4f0d2117bc5a02bbb5192170fe65e2f0c2302b01c95ef6adb829ef689a`  
		Last Modified: Thu, 03 Jul 2025 23:13:12 GMT  
		Size: 735.5 KB (735538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a74b619e9325ae8e5b5adb511075d9c35247e8de5593f5996184112a115ffd`  
		Last Modified: Thu, 03 Jul 2025 23:13:12 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78d5acf69b51a1fe4d9f67ce5f26c6f01d2cf6d3a8795c5edf5de1e03843b82`  
		Last Modified: Thu, 03 Jul 2025 23:13:12 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:a40b0954587af3d3cb6506954d3609818942e2626e2b484baf5ef32e2f758fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7630f9c336baad52d91c577df4c2b82980a9e7c11823385c876e62a4c3b82ec1`

```dockerfile
```

-	Layers:
	-	`sha256:68699c3048c4af9b4b3b9cd8448d2ecf4689d835321caf458ead0ae588cd8895`  
		Last Modified: Fri, 04 Jul 2025 01:13:29 GMT  
		Size: 2.2 MB (2173846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7afc7d1b68b82c353c58c33175613c1fcaa298adaa6a87175e82c63e7a485b0f`  
		Last Modified: Fri, 04 Jul 2025 01:13:30 GMT  
		Size: 31.4 KB (31362 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v6

```console
$ docker pull composer@sha256:c04f5f68a1cd6b21b39fa9629ec09c04ea7a0a61ab085c5a39c2bc78a0218b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77384933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b662652d26f29a2cf473a00d55c6e7d3a5daacd4df84871a99ded37edfb7ab9c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4a1a48d371204daac6d50cf0ade3fcbe953b7326556c347d0834eeb808b22f`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 13.6 MB (13647232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7209fb73f851518e0fbc85b54004a573116286207c48ee96ab37833cb8ea1353`  
		Last Modified: Thu, 03 Jul 2025 23:00:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7698dfdb6ae14586a077f81a7e7531ba3d394ab385475ff9c6573114a36ad047`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 22.2 MB (22216193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2822e518605b3410372bbcdb567b3220dcdbe3fc3a85d76aeeed7414a97ce84`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc23f56a1dfd1eb937c6d0d63cb116029d4ac6193e3b8e0487798f7859b09cf`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb672fb64a4977b38f156870ac6fd28ad3898b39594ead2e5d7a7a25cf62e07a`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f65dda0589cf68df6c1f7a31f2ed36448fe5ac89816b32bef12a62b39575a0`  
		Last Modified: Fri, 04 Jul 2025 01:07:05 GMT  
		Size: 33.8 MB (33807127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af16e8c9f29c59fdf9ae69e6ad7a7f42c68aea017b14dcf169ea15f538efb4e`  
		Last Modified: Fri, 04 Jul 2025 01:07:01 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20f59f717121556e8d36b7f829f149cee98a5b91765ac525ded0bbc2f721ac5`  
		Last Modified: Fri, 04 Jul 2025 01:07:34 GMT  
		Size: 736.1 KB (736137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276f90de6b971f3f9e70e3ba1696097f5f3def96560245a5aad168ded473ae4f`  
		Last Modified: Wed, 25 Jun 2025 20:17:19 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f70c5ea717866cfbf558c790e49f9d572116293d7a33ea61f0ecf50a0391f26`  
		Last Modified: Fri, 04 Jul 2025 01:07:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:7be3c423187b6b7aefe66fec3aa1feb1cb2834b67e171dacdf90f646ac45dd13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 KB (31241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e16759e5fd0716956d0ac4e0df53f77912ea2e6702e40264b52f53bad16fac`

```dockerfile
```

-	Layers:
	-	`sha256:5860ece640b4dd19d4fd863491c942d9b3221cea5db330975a98b7e33a0b6fc1`  
		Last Modified: Fri, 04 Jul 2025 04:13:36 GMT  
		Size: 31.2 KB (31241 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v7

```console
$ docker pull composer@sha256:5126dd2906ea0aa70d3b92f282b9deede06c5a2f35087affe12004567ef01623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73923641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7532ae5fa53b7e1a9011901a9ad57112442cb2d795d7d793ce9ab20c9e3d8aac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f4b8d7b2257f1a6ac3d6d3cc6bf9a4b64ab9fc5d2607c301f7de2c7d6c4f46`  
		Last Modified: Thu, 03 Jul 2025 23:46:20 GMT  
		Size: 13.6 MB (13647249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a41d3b4f0ee7936d37a29b00d6599e6c083cdd6c3c1e87cf67e60c78bed722f`  
		Last Modified: Thu, 03 Jul 2025 23:46:17 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f25659badae5bd6d735e7a8151332a7d70260be40b9bd15903ae5024c69186a`  
		Last Modified: Thu, 03 Jul 2025 23:46:20 GMT  
		Size: 21.0 MB (20968354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9020d050ffd80f0ec4539c880f71565ba7987609cedfc9dc9ff78af7fb53b62b`  
		Last Modified: Thu, 03 Jul 2025 23:46:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9a523c3a709bd62efada35a0a92295ac64b04640f1069b295c0d6889f2487`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210dbe376a53d9ebd8229f86a814b0d26ee3ca102f0e74c6dc09a10a9c343c58`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebcb76101e3ff8f5c34e57b65c480c0f53a9657085c1dd3571c570cc1908dec`  
		Last Modified: Fri, 04 Jul 2025 03:24:53 GMT  
		Size: 32.1 MB (32069935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7837ce17d23c46b208ed90e2deb598eb1aaed88b570cd6b34760d21674e702c`  
		Last Modified: Fri, 04 Jul 2025 03:24:49 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d785e9b0cf200ff1685ae55d7faa2405f9e64fb78a15f331451f93baaab17b9`  
		Last Modified: Fri, 04 Jul 2025 03:25:25 GMT  
		Size: 726.6 KB (726607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d692aeef38370bc31967291d9ffd1696ff481f5afbe739a8f163df32d95c75b1`  
		Last Modified: Fri, 04 Jul 2025 03:25:25 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee774b4619f4d3dd615d31e3f0504d1176c318ec6f1ecb7938d0dd6ab94ad82b`  
		Last Modified: Fri, 04 Jul 2025 03:25:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:131a147ddd7b567d6890fc9b800500b76c68e29409149eb716d8b3f434bf4c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac42b45cd5ce34b6b189a9cd88c0c1b04a7eff46694a1f119f8228ffcf31bf8`

```dockerfile
```

-	Layers:
	-	`sha256:a9c94fb0b84d765e1f9eb122c3a8ac5d1df14b248fa6962686e5162601877de8`  
		Last Modified: Fri, 04 Jul 2025 04:13:39 GMT  
		Size: 2.2 MB (2174162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f8572fb8bacd668720d79bb51ad002cedda8269000e5e3dab0c332dc554fe0e`  
		Last Modified: Fri, 04 Jul 2025 04:13:40 GMT  
		Size: 31.5 KB (31456 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:6f78a3f8c303c56a7be091143ff0db5599ce08ccd13cfd372e558abe7328a510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76557500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2f13a0ce48780f11e5201dd96d98ca037d139cc68b3a0f0487aa16f52ca969`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d74afa414d93be74315fb2fbbededff31189950343736eb9412b26b4f530d1a`  
		Last Modified: Fri, 20 Jun 2025 19:32:29 GMT  
		Size: 3.5 MB (3470712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91ea4522a211c5e50ab5b22083b52449e7ad38398a1f6e5dad24e4a62961906`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b695911010ae65b6cf4c4b5ac350b27932e3b4b29077f6094baa473db50fb5`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e2341d4b1828e7c29626f05458e9c7ac77b849f7fa211122c5e49f3db640c2`  
		Last Modified: Wed, 25 Jun 2025 19:58:30 GMT  
		Size: 13.6 MB (13640504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2214385dee2a6502125f514cfafec9ffbab10a83686ed1edebefbe13bb98e0df`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2192f9a8f7dc985e1b1534af7a423269d9525cd446882c0b66bc83bd73c1d`  
		Last Modified: Wed, 25 Jun 2025 19:58:29 GMT  
		Size: 20.5 MB (20519110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7813f4e30ce21280209e560b03ffd244261e042d03b4f926c87197d856e4d07a`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5659da52250b6def060ce2459caf69d028600439407c5609ffb01e17d290d0a`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 20.0 KB (19995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed11a0655a2eb0f0eae0b13f815d1385ec0d4bc0fc0d3e23f5c2e3aed8e1799`  
		Last Modified: Wed, 25 Jun 2025 19:58:28 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db90ec20dde1245e26657e9eeab7a68a4f381ea6442f98f105cfc54ce54e3a0b`  
		Last Modified: Thu, 26 Jun 2025 00:27:56 GMT  
		Size: 34.0 MB (34010879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb4fdb28ebd43bf90c0134d109bd7f9e79aa657ab4e9e040a42ac1d008e71aa`  
		Last Modified: Thu, 26 Jun 2025 00:27:53 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baee8ab4115a4d9d8133adbe90272c648703c8a12ab643ecd4122c342434c679`  
		Last Modified: Thu, 26 Jun 2025 00:28:29 GMT  
		Size: 735.5 KB (735527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf84df54744d3b2abb00debb5b2b31a7e8775e5254822572ec21991362ee974`  
		Last Modified: Thu, 26 Jun 2025 00:28:29 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8901fd70ed330b7c5a3bcdc084c75508be74b9581ee86c89a29bb6baf2cc0e1a`  
		Last Modified: Thu, 26 Jun 2025 00:28:29 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:5c76f497285a1f4fd7c967538065d759dac8153af07453d42c12e082ad79fb73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd48587e1c1188ba8b05675fb3ee60667ed00d2c13309d482d5a4b5dc4b86122`

```dockerfile
```

-	Layers:
	-	`sha256:06c6e79e79202258cba627965d98ff65c73706b27bada48699db9d93f30defdb`  
		Last Modified: Thu, 26 Jun 2025 01:13:33 GMT  
		Size: 2.2 MB (2173978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8034567f995258e01ffcb6dfc22497079ca859f1aa40cd36daf448fe6e682c7a`  
		Last Modified: Thu, 26 Jun 2025 01:13:33 GMT  
		Size: 31.5 KB (31475 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; 386

```console
$ docker pull composer@sha256:c834a677f11abc62dd604c47559feac6c53f14442634311bd0453c18454e3694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79800235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd09a313d040ee1722eb7d8f00b4dd0950c45d8b7ca4d8a9afdb8922ed7c0207`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4579a4802acae62f9995bc4ca35846cfa477f9a889ce0fb2017ac6630b78bd4a`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 5.8 MB (5806973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57074fe130dea7f1367879dc4bc435c31dce84ecd32b48ea0a63d35b4a08b836`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7e9cf52dab21b2f526412767a5e92e23eeb507ad11d31f9bf4391ad5eb6a66`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee47d22d22648a57b652a67b201fb0e169513c91be3eec67cb726ba70e375a83`  
		Last Modified: Thu, 03 Jul 2025 23:05:02 GMT  
		Size: 13.6 MB (13647238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ed9c7929ede2d39288b5cdc1a881693463f9694eab366fbb269e70c0d92a49`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63b1c24d7566d919e950b1eaf0a78b66a3bebc8b853f7dac99909776dbae0f1`  
		Last Modified: Thu, 03 Jul 2025 23:05:04 GMT  
		Size: 21.5 MB (21500663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f235298ca3bcb11577f52427a9e9abe5f5708168ce3e6f7a92e3516e12f33f6`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3069db4b5ea73d2b8c2f80770d98b1ecf8fc539f7fcb87b04c2a4d4c1d2747`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 20.2 KB (20195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af93b74a51d1b8b0d9adaa24d025147b9bbb65f3dea67b796f0959416093750`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 20.2 KB (20192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf453c1071c792beaa5267fdd052480889666839d63b36c3c72c8b405741dcb`  
		Last Modified: Thu, 03 Jul 2025 23:12:03 GMT  
		Size: 34.4 MB (34436750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbbd4849c630a412f4eaa507248cbc656e68a623f0cf27d61c333de4853bfc4`  
		Last Modified: Thu, 03 Jul 2025 23:12:01 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59574e203c63533c068a2d8001b555b8afde4d12b2620cef6c81b561971196a0`  
		Last Modified: Thu, 03 Jul 2025 23:12:01 GMT  
		Size: 747.4 KB (747353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db41c9e62300962a9037fc2e22ade4099ece56dccf7bdb54621bbd51da0e0ea`  
		Last Modified: Thu, 03 Jul 2025 23:12:00 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138472a9b76e193c0429098e29aea1bb89935127ce211bda33b07bc7ede3a9ea`  
		Last Modified: Thu, 03 Jul 2025 23:12:00 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:bf0ab8f634046057fda6d729e288a40f1b65a47e2b0c075f49319a649e1aabd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f1a214eb061abc166bd8fa85807028d873d081cae27e506444370ded39a6b9`

```dockerfile
```

-	Layers:
	-	`sha256:03bf3d77e2ad0c1e638f43456b3ed9aa74deef374191c89cfa9beebfacb757ca`  
		Last Modified: Fri, 04 Jul 2025 01:13:44 GMT  
		Size: 2.2 MB (2173634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:766db42ebc4acb8d84cd48ad3a8a7a38cb3805760dbd486132ef08d3e4f0854c`  
		Last Modified: Fri, 04 Jul 2025 01:13:45 GMT  
		Size: 31.3 KB (31331 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; ppc64le

```console
$ docker pull composer@sha256:d2860483ff6060e4f34718f3569976c580e55a019d321056c10b09aa7a2db417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81267874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc71c021dfae7f4d4c67e985475e3acdb6199aef0d087e89c012862399cb9d63`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7db3af28cc31124a8bce98c13cd1b2512963d13f437d0d67f9918df0d57d2b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 5.9 MB (5946924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ec39d79edfa484fac002ed8c640f17ae8077df4dce88811d8d186865593a6b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 939.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2995d4272705fc452f2b3ea9e2d118681efbad9f858c7743f6f69364d73a50`  
		Last Modified: Thu, 03 Jul 2025 23:15:35 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da4669ab0266f9dd895304e7c92d52e7df1b0acfdc30e6abf0d73fd20c6d09a`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 13.6 MB (13647243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdb584c1e59e66bf7047b954cfc1e41ae7df62560b963934f349b9bd0a11fed`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dff158c4fec087bdd22d80d469c14bd7f5e8a7d72d9a682db56d77c7977e55f`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 21.9 MB (21877134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa09d11c80e8896e162d36345eb3a1cf062f1ba207ed29c537b7783eb818f415`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09daff9fd7af3987bc24f46923dc89bca4e186069874ea11f88390e02dbca5a8`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1d9e25cff60aeed589359ca184c52454f63361a6309e3c363d0d97c227e006`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcefe2124ab8f2442794aaabac7f9422c8d266cee3bbfbb30c3cea3b0f0943f6`  
		Last Modified: Fri, 04 Jul 2025 02:29:48 GMT  
		Size: 35.3 MB (35279082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7315eb9406973e6ea300692e85a137454ee79d74bbb5b71ff352feab46e7c24`  
		Last Modified: Fri, 04 Jul 2025 02:29:46 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8b488c3c48b62f7ab37e985c2badc46f00121932cb154e4c6e36f76d40bfca`  
		Last Modified: Fri, 04 Jul 2025 02:31:05 GMT  
		Size: 742.5 KB (742455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a966f4fe56f65e15c55c3975d12cb9baf1b5c6893ba5bed2c3b5f6b74ddccd40`  
		Last Modified: Fri, 04 Jul 2025 02:31:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd6dfba27b8043e866d82286d5dab18f70e2226534b19ac2cce95405c87540f`  
		Last Modified: Fri, 04 Jul 2025 02:31:04 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:8a118c282313d5577c6373b17ef7c184cf27eb59f005a9a658ae088cc47f9548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f815fcffd01d9c4289ae0764dba6704ac9735b4f0280af9289068ce054e0818`

```dockerfile
```

-	Layers:
	-	`sha256:c4e95040e7a37340deb333374f4c71ca1bddc12735d7a81ad3ebc0caffe12181`  
		Last Modified: Fri, 04 Jul 2025 04:13:48 GMT  
		Size: 2.2 MB (2172403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ee97024ceab90c82bd9689466e8e666002355a9faf7b09be18680b02b1f80b`  
		Last Modified: Fri, 04 Jul 2025 04:13:49 GMT  
		Size: 31.4 KB (31404 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; riscv64

```console
$ docker pull composer@sha256:30fb2195c5a22c9ccafe97ba65907700f5c297078b2243383db0957e71db6017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73032087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31f73171ecf1f713aeb4422a5fd753725f8e97ed92f049c8512adf0094deb36`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d0224769088850e26eb3ba2638a8a3febc4b65991ac8cc63dc3f29cf199070`  
		Last Modified: Wed, 11 Jun 2025 05:05:11 GMT  
		Size: 13.6 MB (13640513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a45f979f3844cfaf9ad9f1a00668b3bb56bc478c711f2d939a7dba0c2ed6e1`  
		Last Modified: Wed, 11 Jun 2025 02:39:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b864e2d5fb63463e7b594794f1b0077ef70793371e80280a29b09008bb9771a`  
		Last Modified: Wed, 11 Jun 2025 05:05:14 GMT  
		Size: 20.4 MB (20388593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91ae988832dcf22e179ec800eee279369b0d1b8a4129c2bd761a392671d8d32`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5d276f1eb8afbe6e12101788a8d8d2c68f0875a801fca945c95b68b009ee44`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033c69f0ad5808ebac07aefd6d1a9c0933c09e134334a8bd72a2f49fb7ed2297`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 20.0 KB (19999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7d4367f9b25dba1c9057a363403805d1f3ffce81d401bb89eaa3652ee82d83`  
		Last Modified: Thu, 26 Jun 2025 08:33:02 GMT  
		Size: 31.1 MB (31107678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a85da3fdbf5b1c41e6f68043dc7ff3cb2ef316082fa092b6f23657dffda19a1`  
		Last Modified: Thu, 26 Jun 2025 08:32:59 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18adcae7f1301b51ee2fc7abe3a5ce5b41d0acd2549ba9fe655330926b23f83c`  
		Last Modified: Thu, 26 Jun 2025 08:38:00 GMT  
		Size: 733.3 KB (733287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419c8793715002635b6ef09089a9180fb4f05a4ee2870a69fbd1c886d3ed7d69`  
		Last Modified: Thu, 26 Jun 2025 08:37:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca1d976b231d6201f5a449befa42f9bdd9c97f36514186c9c4abe8b008411fb`  
		Last Modified: Thu, 26 Jun 2025 08:37:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:7a4a7a6ebb740b9d07f2583f86c75629d5c5746d3ff061a727a55bda778933e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559ec2767071294375a43ba468a5bf5f3efd68fbe1ec44023e13e3bbcf42004b`

```dockerfile
```

-	Layers:
	-	`sha256:fe0803650cefb94ad050ee3b4f9db347ce916801dda1460eec5a7de38d5007b2`  
		Last Modified: Thu, 26 Jun 2025 10:13:41 GMT  
		Size: 2.2 MB (2170662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74d8acc9b7a1210df34ca548487e8756be0cdb63077782f3fe64a13a23fea002`  
		Last Modified: Thu, 26 Jun 2025 10:13:42 GMT  
		Size: 31.4 KB (31395 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; s390x

```console
$ docker pull composer@sha256:1f23418422d093e8f10d6041dec54961710565294dc08c939ce976614a3109e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77300564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0014ddd15a5086ca882213cb209e9aac9133d438d03d1fd4b97e1406732f9764`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abd3e67b018bcd8c0aa4d0434d7ec04dcdb3a3cfbf444a313e2be49d0524ec2`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 5.9 MB (5932552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f41e4866617495859c5133b898f769b3867a6a3ae061aa9561da765981c5ad`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9335ac6e22dd0c0b2e07f4a5406c437168067a987662ebd8bcd3b269496018`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da3506587d8ded424a7c5730d972ae6f1735f6afc1a325c7e9f83474f399fde`  
		Last Modified: Thu, 03 Jul 2025 23:16:27 GMT  
		Size: 13.6 MB (13647264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671a375a1790dbb9b0d83c7dd0560e7f6e75fb5b06afbc76019557052c897e5a`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dc301a9ae8a743478269ed0a476a3abb5ea1e3f156da87ce855397d9ddef91`  
		Last Modified: Thu, 03 Jul 2025 23:16:26 GMT  
		Size: 21.5 MB (21450357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1074498264e134b44d0edcde237cf3cfadba39197115581cfd4b9a9c5ba0fa`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1658861fe310f53081a1e605b2427a938ceddc66bacb97178d77404b333d65a1`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105bedc3ea3fb0ab6591d908f480b2bb3c119411d1ba9dc0c0e9fd62b45f2a39`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb11fbf2308810b649dff18139a7f4e9d809ae768cc36f3d15ec258497a33363`  
		Last Modified: Fri, 04 Jul 2025 02:05:49 GMT  
		Size: 31.8 MB (31839057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb18554f4af212841fd6225002512ce8150b2738e7c8d62528fee75319d8df8`  
		Last Modified: Fri, 04 Jul 2025 02:05:34 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e98fe8743070c639f8eb2ee4894e447b51c5fc9dae60c1e8a14c66697980da1`  
		Last Modified: Fri, 04 Jul 2025 02:06:20 GMT  
		Size: 739.0 KB (738958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c01d00f55b0e2dfa94ad1229e9a69a8a4fe4d4ea6ae5350e1a2227a5689d5f8`  
		Last Modified: Fri, 04 Jul 2025 02:12:39 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7894d22dfb6f29a3a6244074426e8a44f24ce03291d76f60267d87fd135970ad`  
		Last Modified: Fri, 04 Jul 2025 02:06:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:0d29e14172dd031e7e6b8e41b50e5f147b836d09e21a3a13be04fa8f2d95b170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195f0233b1e45e2ea78e00f2b80ad2e8458288518f4e002b1375cd29157e2471`

```dockerfile
```

-	Layers:
	-	`sha256:c66ffdf527f5d5849190b5cbf71d176f2c1d1b63f83f5624d7cc1fa06167864b`  
		Last Modified: Fri, 04 Jul 2025 04:13:55 GMT  
		Size: 2.2 MB (2170458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e6e936165c4495ba9d28088542473a1a3bcaddbf4e09d4267f77f963e223044`  
		Last Modified: Fri, 04 Jul 2025 04:13:56 GMT  
		Size: 31.4 KB (31361 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2`

```console
$ docker pull composer@sha256:0eed6733d75c35f13c4794990f22aa04654addc135bc575cd5692572bb3c8935
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
$ docker pull composer@sha256:864a61db30e6203c4a20b777493bc17f9c361303fd6a5e6db2cbbd4c56d5faa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79309733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21295413e1bc8c2201f98d084a45091bf7d8ee2b6514e9bec81c411a8e172682`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.10
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b94662290ef2237915af922ad14ae2b406eccea26d9201aa949ea52f20b737f`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 5.9 MB (5944403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498a67832465ef6dae00170ccca088bdbc63d05a197e0ba1403442805169a06a`  
		Last Modified: Thu, 03 Jul 2025 23:04:16 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53785dc48fc021d1c3f9c46a776ead61a024377fb5e6ab592908501762d63a7`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c87a7802578b0a5aebb57ffea8e543a2d50cff1ec6ffb0941fe8ad61b3a9e6`  
		Last Modified: Thu, 03 Jul 2025 23:04:23 GMT  
		Size: 13.6 MB (13647262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5aa21d09531523ae5c279a8b0eb00236af3b192f428c934050c61f7e1611eaa`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fccbfd125531b00b24f5c4c9c182e17714478e55b96701b7e71d30f7f70f9b`  
		Last Modified: Thu, 03 Jul 2025 23:04:28 GMT  
		Size: 21.0 MB (20971251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481b52666b981ec99f99b98b64ef13ff6ce799950970b68817767c966318dc11`  
		Last Modified: Thu, 03 Jul 2025 23:04:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a3724a01f76e5128bdebeeb89d8f42b63b2e987403c91e1f1f5c084c63ffee`  
		Last Modified: Thu, 03 Jul 2025 23:04:22 GMT  
		Size: 20.2 KB (20205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755a5679cebfbcec196508684d58f3d3479a8923825702cea8057be9ea0509ea`  
		Last Modified: Thu, 03 Jul 2025 23:04:25 GMT  
		Size: 20.2 KB (20204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c852688dfb4eb3338fa2b359258f4def968d8542cb467086d1eeea1f28905a74`  
		Last Modified: Thu, 03 Jul 2025 23:13:02 GMT  
		Size: 33.9 MB (33928299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c622ee0a80d81cfef14283072f36dba68467de22ad3d6eb6da4af6de1560b45`  
		Last Modified: Thu, 03 Jul 2025 23:13:00 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218c0a682557e725de4b4ae1b3d83acabd53d9ce5f23a45ef3e1b3721fea1262`  
		Last Modified: Thu, 03 Jul 2025 23:13:00 GMT  
		Size: 976.4 KB (976411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cc4579c8bd93cd33c1b651f3f52e56ca67655b23b2fc99ae1954c25cfc8630`  
		Last Modified: Thu, 03 Jul 2025 23:13:01 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e141382acfb75c4a31d782c5f0837bb164ef89d645af35d1c815bcdfcf5cac`  
		Last Modified: Thu, 03 Jul 2025 23:13:00 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:d4d4b49e2553833f43684f3a5905521881e8a9dfa954fc06225be2cce9d466bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbf3553c4657aa72f0ba321ebc291fa348abef46a3a72f6d93550521428759f`

```dockerfile
```

-	Layers:
	-	`sha256:3ad72884d89234dbd14e825e71a080c543f84beceb8ee170a45eb4e9be474b08`  
		Last Modified: Fri, 04 Jul 2025 01:13:40 GMT  
		Size: 2.2 MB (2175340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c65c76faf5625b204b8a6440bd9d80740b5757a5f019373204445f59774974eb`  
		Last Modified: Fri, 04 Jul 2025 01:13:41 GMT  
		Size: 31.7 KB (31652 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v6

```console
$ docker pull composer@sha256:648b0bf94ac42dff7872cea189a81b4e25e8be6ae5015b1da330a9c8c31b704f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77625569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0576b47e03b1a0e8e65bd259e7af5895948140096c3afc93f9a0dab0e88a2f48`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.10
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4a1a48d371204daac6d50cf0ade3fcbe953b7326556c347d0834eeb808b22f`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 13.6 MB (13647232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7209fb73f851518e0fbc85b54004a573116286207c48ee96ab37833cb8ea1353`  
		Last Modified: Thu, 03 Jul 2025 23:00:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7698dfdb6ae14586a077f81a7e7531ba3d394ab385475ff9c6573114a36ad047`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 22.2 MB (22216193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2822e518605b3410372bbcdb567b3220dcdbe3fc3a85d76aeeed7414a97ce84`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc23f56a1dfd1eb937c6d0d63cb116029d4ac6193e3b8e0487798f7859b09cf`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb672fb64a4977b38f156870ac6fd28ad3898b39594ead2e5d7a7a25cf62e07a`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f65dda0589cf68df6c1f7a31f2ed36448fe5ac89816b32bef12a62b39575a0`  
		Last Modified: Fri, 04 Jul 2025 01:07:05 GMT  
		Size: 33.8 MB (33807127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af16e8c9f29c59fdf9ae69e6ad7a7f42c68aea017b14dcf169ea15f538efb4e`  
		Last Modified: Fri, 04 Jul 2025 01:07:01 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d70107b5aba54d8f31fb97e22d592810074a1b8f05392fc1093eb44ac667ff8`  
		Last Modified: Fri, 04 Jul 2025 01:08:05 GMT  
		Size: 976.8 KB (976765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb15dc78f78d103edcc744c17908609b087a11d0c10548c3f9d791e07ccbca86`  
		Last Modified: Wed, 25 Jun 2025 20:29:47 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224953665089fda926db4dea1b86110c646109a8a62e68cb13246f46d3d4b95e`  
		Last Modified: Fri, 04 Jul 2025 01:08:04 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:cc5374cca047b9c29c17b890515ce54d573a889881ed1a840b780509ee1a35c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edcc52d9671e580042a8af83c87912d079d008f561c600822f9a3c9d52ccea5b`

```dockerfile
```

-	Layers:
	-	`sha256:70fb45703ae28fcbe74dc9795f343a8920c7c71d06a958b9c23a34a6eb3bfa5d`  
		Last Modified: Fri, 04 Jul 2025 04:13:56 GMT  
		Size: 31.5 KB (31539 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v7

```console
$ docker pull composer@sha256:5c2811e58deda112f1b19ea2a429444944c8ad179727b126774b90672e8e66d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74164142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c019e9b06442cd09ddf2e4b7eb65cdab0d41f4df9e0d782fec975e072b48e76d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.10
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f4b8d7b2257f1a6ac3d6d3cc6bf9a4b64ab9fc5d2607c301f7de2c7d6c4f46`  
		Last Modified: Thu, 03 Jul 2025 23:46:20 GMT  
		Size: 13.6 MB (13647249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a41d3b4f0ee7936d37a29b00d6599e6c083cdd6c3c1e87cf67e60c78bed722f`  
		Last Modified: Thu, 03 Jul 2025 23:46:17 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f25659badae5bd6d735e7a8151332a7d70260be40b9bd15903ae5024c69186a`  
		Last Modified: Thu, 03 Jul 2025 23:46:20 GMT  
		Size: 21.0 MB (20968354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9020d050ffd80f0ec4539c880f71565ba7987609cedfc9dc9ff78af7fb53b62b`  
		Last Modified: Thu, 03 Jul 2025 23:46:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9a523c3a709bd62efada35a0a92295ac64b04640f1069b295c0d6889f2487`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210dbe376a53d9ebd8229f86a814b0d26ee3ca102f0e74c6dc09a10a9c343c58`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebcb76101e3ff8f5c34e57b65c480c0f53a9657085c1dd3571c570cc1908dec`  
		Last Modified: Fri, 04 Jul 2025 03:24:53 GMT  
		Size: 32.1 MB (32069935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7837ce17d23c46b208ed90e2deb598eb1aaed88b570cd6b34760d21674e702c`  
		Last Modified: Fri, 04 Jul 2025 03:24:49 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ad676d7ee639bd12778210b726ccd10b9eead85271834e2b2c6bf311e7240a`  
		Last Modified: Fri, 04 Jul 2025 03:26:21 GMT  
		Size: 967.1 KB (967097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3b74b2060ffea794587392d8e37fc22baa87dbd5c3bee7b016a864f1aea241`  
		Last Modified: Fri, 04 Jul 2025 03:26:20 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb4cff2df01ba4618678e4f893513145e63282a0ad4f1bffe3e362bf8706220`  
		Last Modified: Fri, 04 Jul 2025 03:26:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:3578e71f433b37866bf7a4a743e8b077af4f522455beef6e247b8d02a8e137a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27499b4da1ed9b3f5ac42b35ea64b62305426f552bc2c1c6d49da8d1a84defb`

```dockerfile
```

-	Layers:
	-	`sha256:5f8a22eb1d359ca353b20fa10f9ceb96545b85653ea907d8d75b260e52891e2e`  
		Last Modified: Fri, 04 Jul 2025 04:14:00 GMT  
		Size: 2.2 MB (2175664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e26ba3a9482b3a935d3eb85feaf385751e9d4f79763ed43ff63f893b27554d5d`  
		Last Modified: Fri, 04 Jul 2025 04:14:01 GMT  
		Size: 31.8 KB (31754 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:d2dadc0c40a3554177b591599fb4d6a672330089c735772da89e0220add47f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76798022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d43140056d0abec9110d9e36cc98a921b48be8aac07425b3be37eced18794a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d74afa414d93be74315fb2fbbededff31189950343736eb9412b26b4f530d1a`  
		Last Modified: Fri, 20 Jun 2025 19:32:29 GMT  
		Size: 3.5 MB (3470712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91ea4522a211c5e50ab5b22083b52449e7ad38398a1f6e5dad24e4a62961906`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b695911010ae65b6cf4c4b5ac350b27932e3b4b29077f6094baa473db50fb5`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e2341d4b1828e7c29626f05458e9c7ac77b849f7fa211122c5e49f3db640c2`  
		Last Modified: Wed, 25 Jun 2025 19:58:30 GMT  
		Size: 13.6 MB (13640504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2214385dee2a6502125f514cfafec9ffbab10a83686ed1edebefbe13bb98e0df`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2192f9a8f7dc985e1b1534af7a423269d9525cd446882c0b66bc83bd73c1d`  
		Last Modified: Wed, 25 Jun 2025 19:58:29 GMT  
		Size: 20.5 MB (20519110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7813f4e30ce21280209e560b03ffd244261e042d03b4f926c87197d856e4d07a`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5659da52250b6def060ce2459caf69d028600439407c5609ffb01e17d290d0a`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 20.0 KB (19995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed11a0655a2eb0f0eae0b13f815d1385ec0d4bc0fc0d3e23f5c2e3aed8e1799`  
		Last Modified: Wed, 25 Jun 2025 19:58:28 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db90ec20dde1245e26657e9eeab7a68a4f381ea6442f98f105cfc54ce54e3a0b`  
		Last Modified: Thu, 26 Jun 2025 00:27:56 GMT  
		Size: 34.0 MB (34010879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb4fdb28ebd43bf90c0134d109bd7f9e79aa657ab4e9e040a42ac1d008e71aa`  
		Last Modified: Thu, 26 Jun 2025 00:27:53 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ddf66bb9ba56337081b692d4129b361f983e7f9abd1d5e349d28c1c7eade483`  
		Last Modified: Thu, 26 Jun 2025 00:28:57 GMT  
		Size: 976.0 KB (976041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b24a8ffa2909a504d9bbfc6df46cc2b56d610d921e33e9974ffc838c62bdd1d`  
		Last Modified: Thu, 26 Jun 2025 00:28:57 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821b9dea24a435946ecb336cb8278f7297bed4a94795980b99f141347beab268`  
		Last Modified: Thu, 26 Jun 2025 00:28:57 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:df1144ec9680bd760c06c95a7bfff7150690d287e025712cc341c4a5ffe356df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640d11c5a6cebe938b2fd6fab0e883dbce3befa0419a62d2c446198798adf567`

```dockerfile
```

-	Layers:
	-	`sha256:a7b2a0fdfcdccff2b7138ac64502f1f2fb239077a7b59fa7e206bf3e6f124b5c`  
		Last Modified: Thu, 26 Jun 2025 01:13:48 GMT  
		Size: 2.2 MB (2175484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91b5ec1ac58d000c75aaad3474d0386b5646668bc3b2685875bd6ce02e925b2b`  
		Last Modified: Thu, 26 Jun 2025 01:13:49 GMT  
		Size: 31.8 KB (31777 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; 386

```console
$ docker pull composer@sha256:7ea3337a73dfe929bb2a4e849d7413a67d2f8bece13a67bb7cd0b77e112e54e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80042550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5691a9cad94ac3356a7d1f58071b048add1584758c6ed163996f041ab04e4a8d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.10
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4579a4802acae62f9995bc4ca35846cfa477f9a889ce0fb2017ac6630b78bd4a`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 5.8 MB (5806973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57074fe130dea7f1367879dc4bc435c31dce84ecd32b48ea0a63d35b4a08b836`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7e9cf52dab21b2f526412767a5e92e23eeb507ad11d31f9bf4391ad5eb6a66`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee47d22d22648a57b652a67b201fb0e169513c91be3eec67cb726ba70e375a83`  
		Last Modified: Thu, 03 Jul 2025 23:05:02 GMT  
		Size: 13.6 MB (13647238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ed9c7929ede2d39288b5cdc1a881693463f9694eab366fbb269e70c0d92a49`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63b1c24d7566d919e950b1eaf0a78b66a3bebc8b853f7dac99909776dbae0f1`  
		Last Modified: Thu, 03 Jul 2025 23:05:04 GMT  
		Size: 21.5 MB (21500663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f235298ca3bcb11577f52427a9e9abe5f5708168ce3e6f7a92e3516e12f33f6`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3069db4b5ea73d2b8c2f80770d98b1ecf8fc539f7fcb87b04c2a4d4c1d2747`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 20.2 KB (20195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af93b74a51d1b8b0d9adaa24d025147b9bbb65f3dea67b796f0959416093750`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 20.2 KB (20192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c8ee1962b1a764f17623a97c88eac6b4bcd6264d017309e15662ca58ba4328`  
		Last Modified: Thu, 03 Jul 2025 23:13:04 GMT  
		Size: 34.4 MB (34436697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62967b08a91543e22a6b21fc96ea01449936ec8716111d503430bebb27b9b1cb`  
		Last Modified: Thu, 03 Jul 2025 23:13:00 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30acb5fcf8b4c6c26895514cffa50f5f9943af2422b56fb2d081f516ceedb84a`  
		Last Modified: Thu, 03 Jul 2025 23:13:01 GMT  
		Size: 989.7 KB (989711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431bf78845ea7be375b442b6d6e0b94a886a77fe6982ccd2cae5e6fba720130b`  
		Last Modified: Thu, 03 Jul 2025 23:13:01 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44a7383365beb5c7a1faf0ae044a570043a5793a4b4007761b2d0751cd244da`  
		Last Modified: Thu, 03 Jul 2025 23:13:01 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:fe8fc42c5d819f1d34f4ce945cfdf317de4a0cbb50d3aeddca71d79022c98741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b3db9f01b13546692b4ad51bad36e7e3165c293f4bf1fc24d927922991439d`

```dockerfile
```

-	Layers:
	-	`sha256:40add4385980bb9b06d7a8f0bea17a1228b127a11af5d741d0259be4e26f4bcb`  
		Last Modified: Fri, 04 Jul 2025 01:13:54 GMT  
		Size: 2.2 MB (2175123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fe1485dca730e6cd0aa0fdbb3d1bd1ee70141e35977cd5fdd159ec4fc558945`  
		Last Modified: Fri, 04 Jul 2025 01:13:55 GMT  
		Size: 31.6 KB (31616 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; ppc64le

```console
$ docker pull composer@sha256:78db100203a59f9ca077a0ea16741ec93e078dbb2a52df6ab977a16a05b666ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81508478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60ff07f83bdd829ca9ac347bcd7a91042f0c838a7658f717395cce85d77408c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.10
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7db3af28cc31124a8bce98c13cd1b2512963d13f437d0d67f9918df0d57d2b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 5.9 MB (5946924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ec39d79edfa484fac002ed8c640f17ae8077df4dce88811d8d186865593a6b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 939.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2995d4272705fc452f2b3ea9e2d118681efbad9f858c7743f6f69364d73a50`  
		Last Modified: Thu, 03 Jul 2025 23:15:35 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da4669ab0266f9dd895304e7c92d52e7df1b0acfdc30e6abf0d73fd20c6d09a`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 13.6 MB (13647243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdb584c1e59e66bf7047b954cfc1e41ae7df62560b963934f349b9bd0a11fed`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dff158c4fec087bdd22d80d469c14bd7f5e8a7d72d9a682db56d77c7977e55f`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 21.9 MB (21877134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa09d11c80e8896e162d36345eb3a1cf062f1ba207ed29c537b7783eb818f415`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09daff9fd7af3987bc24f46923dc89bca4e186069874ea11f88390e02dbca5a8`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1d9e25cff60aeed589359ca184c52454f63361a6309e3c363d0d97c227e006`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcefe2124ab8f2442794aaabac7f9422c8d266cee3bbfbb30c3cea3b0f0943f6`  
		Last Modified: Fri, 04 Jul 2025 02:29:48 GMT  
		Size: 35.3 MB (35279082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7315eb9406973e6ea300692e85a137454ee79d74bbb5b71ff352feab46e7c24`  
		Last Modified: Fri, 04 Jul 2025 02:29:46 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4508639e74c9c28c3fb419e0c8c6a031d7291e9393341921ee0f03bd59ecca`  
		Last Modified: Fri, 04 Jul 2025 02:32:05 GMT  
		Size: 983.0 KB (983049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bba142070b7380628289f45cb7efe63e1078c2dee92be982602232fb09fbb5`  
		Last Modified: Fri, 04 Jul 2025 02:32:04 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e42909435644cf68037aa4d86a52d59c7e2e1c9692af7fb3134a361b663960`  
		Last Modified: Fri, 04 Jul 2025 02:32:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:083aa2658271704da9e81255bb7d746de750303a00e3fe499cd00ea99740da16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1895718fc0cd8fbe5ed7357dbf119863fa5506eeb3a93c2a47d7e06a9a0aa085`

```dockerfile
```

-	Layers:
	-	`sha256:0e467847564c6b363f7e9023b8c2aa5c0114ffbbeeb42e175703b015ea07f2c4`  
		Last Modified: Fri, 04 Jul 2025 04:14:10 GMT  
		Size: 2.2 MB (2173903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38a725e262847343f44ce5121a7e45c8b8f973d0ab72ad75bf55dceba889c8d3`  
		Last Modified: Fri, 04 Jul 2025 04:14:11 GMT  
		Size: 31.7 KB (31700 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; riscv64

```console
$ docker pull composer@sha256:e9cf69d00e0485cfc79bbd74de2fcf971c8c0625b61f55964388187353e58dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73273033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387850bcac483e7be49354dc64c55c9837cc316862477690206f7484a1a3972e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d0224769088850e26eb3ba2638a8a3febc4b65991ac8cc63dc3f29cf199070`  
		Last Modified: Wed, 11 Jun 2025 05:05:11 GMT  
		Size: 13.6 MB (13640513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a45f979f3844cfaf9ad9f1a00668b3bb56bc478c711f2d939a7dba0c2ed6e1`  
		Last Modified: Wed, 11 Jun 2025 02:39:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b864e2d5fb63463e7b594794f1b0077ef70793371e80280a29b09008bb9771a`  
		Last Modified: Wed, 11 Jun 2025 05:05:14 GMT  
		Size: 20.4 MB (20388593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91ae988832dcf22e179ec800eee279369b0d1b8a4129c2bd761a392671d8d32`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5d276f1eb8afbe6e12101788a8d8d2c68f0875a801fca945c95b68b009ee44`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033c69f0ad5808ebac07aefd6d1a9c0933c09e134334a8bd72a2f49fb7ed2297`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 20.0 KB (19999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7d4367f9b25dba1c9057a363403805d1f3ffce81d401bb89eaa3652ee82d83`  
		Last Modified: Thu, 26 Jun 2025 08:33:02 GMT  
		Size: 31.1 MB (31107678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a85da3fdbf5b1c41e6f68043dc7ff3cb2ef316082fa092b6f23657dffda19a1`  
		Last Modified: Thu, 26 Jun 2025 08:32:59 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e85546fd2798c3532f47d4372f9fad38a6865cf751f31473179d3d7f11577b`  
		Last Modified: Thu, 26 Jun 2025 08:42:35 GMT  
		Size: 974.2 KB (974222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927f3ec758e29742e7c999ad98dd80206921dfaacd901ad5845dcb2031cda04c`  
		Last Modified: Thu, 26 Jun 2025 08:42:35 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51c338a41ea99d423dd984770a1b2961733013923d88ef9c8487dbe71b53db6`  
		Last Modified: Thu, 26 Jun 2025 08:42:35 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:04bbe23facb3ca2c4a571e15bda01bf0f877d59d3b27c3095a07e13d9629325f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94fc7603e5df6be47d63f45b110d94d3d5fb2768a684d5e4300ce3fe4240da97`

```dockerfile
```

-	Layers:
	-	`sha256:8e4a210b7c1e4a94078dafd17aeea8d7e36e455a45c72480100ddf9d731304ca`  
		Last Modified: Thu, 26 Jun 2025 10:13:47 GMT  
		Size: 2.2 MB (2172162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d93a114259e1d4e445c628108c4d73d72ff7aa9a7638c8c1b5110149716aa3`  
		Last Modified: Thu, 26 Jun 2025 10:13:48 GMT  
		Size: 31.7 KB (31691 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; s390x

```console
$ docker pull composer@sha256:76586dba6bcaf104bf78a2e926157d3ecb2162db2a90333c32b021cbba2835fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77541209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffb961ffd5347aa88d54d9bdbd0dcc69ac5ff667d532b9406faf7a02c73ef0b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.10
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abd3e67b018bcd8c0aa4d0434d7ec04dcdb3a3cfbf444a313e2be49d0524ec2`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 5.9 MB (5932552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f41e4866617495859c5133b898f769b3867a6a3ae061aa9561da765981c5ad`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9335ac6e22dd0c0b2e07f4a5406c437168067a987662ebd8bcd3b269496018`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da3506587d8ded424a7c5730d972ae6f1735f6afc1a325c7e9f83474f399fde`  
		Last Modified: Thu, 03 Jul 2025 23:16:27 GMT  
		Size: 13.6 MB (13647264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671a375a1790dbb9b0d83c7dd0560e7f6e75fb5b06afbc76019557052c897e5a`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dc301a9ae8a743478269ed0a476a3abb5ea1e3f156da87ce855397d9ddef91`  
		Last Modified: Thu, 03 Jul 2025 23:16:26 GMT  
		Size: 21.5 MB (21450357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1074498264e134b44d0edcde237cf3cfadba39197115581cfd4b9a9c5ba0fa`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1658861fe310f53081a1e605b2427a938ceddc66bacb97178d77404b333d65a1`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105bedc3ea3fb0ab6591d908f480b2bb3c119411d1ba9dc0c0e9fd62b45f2a39`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb11fbf2308810b649dff18139a7f4e9d809ae768cc36f3d15ec258497a33363`  
		Last Modified: Fri, 04 Jul 2025 02:05:49 GMT  
		Size: 31.8 MB (31839057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb18554f4af212841fd6225002512ce8150b2738e7c8d62528fee75319d8df8`  
		Last Modified: Fri, 04 Jul 2025 02:05:34 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931a141d3b8edb6ab1e8e3aeb1e9a4b3a912f88003675e89dc46803a6ca8252b`  
		Last Modified: Fri, 04 Jul 2025 02:07:05 GMT  
		Size: 979.6 KB (979593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535010aa718560098f0e81a5f45d58691a627aecca27eca3da2635e48f1c76a0`  
		Last Modified: Fri, 04 Jul 2025 02:07:04 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c75f4f8a0c4c5fdb0702183067fcc807bdd1b7d933a89e4379dc62f7a607ae`  
		Last Modified: Fri, 04 Jul 2025 02:07:04 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:ed1ab93ff8d9690acbeec0b736388e307d82a0f6bd3f3bccade5eb1aad6edf31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfadad1ce6d357c73689ef92670a2f57061dcdb641b7ffc571f0540c543ec49`

```dockerfile
```

-	Layers:
	-	`sha256:28deab63effa2f8e9b986d8fa8c5b7cd8ed330836a898ecb8793003b2a076805`  
		Last Modified: Fri, 04 Jul 2025 04:14:18 GMT  
		Size: 2.2 MB (2171952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac38573486931e331c1ddd2734691ca96fd9af6c2e2a0e1a5ed3b03be09fd97c`  
		Last Modified: Fri, 04 Jul 2025 04:14:18 GMT  
		Size: 31.7 KB (31652 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2`

```console
$ docker pull composer@sha256:d3851732b404b46cc3079f0ba6a2f54fb112f05d652cfb88bcd329f6f1922762
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
$ docker pull composer@sha256:c55bbcc0b5116f3ada5b2b794253e8d642d534800f5d711ec781a0631a511b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79153683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bfb9c90c0dd2a8370857b01de5e68a396844fc9b3eb4036bcee5238053fcd1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b94662290ef2237915af922ad14ae2b406eccea26d9201aa949ea52f20b737f`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 5.9 MB (5944403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498a67832465ef6dae00170ccca088bdbc63d05a197e0ba1403442805169a06a`  
		Last Modified: Thu, 03 Jul 2025 23:04:16 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53785dc48fc021d1c3f9c46a776ead61a024377fb5e6ab592908501762d63a7`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c87a7802578b0a5aebb57ffea8e543a2d50cff1ec6ffb0941fe8ad61b3a9e6`  
		Last Modified: Thu, 03 Jul 2025 23:04:23 GMT  
		Size: 13.6 MB (13647262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5aa21d09531523ae5c279a8b0eb00236af3b192f428c934050c61f7e1611eaa`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fccbfd125531b00b24f5c4c9c182e17714478e55b96701b7e71d30f7f70f9b`  
		Last Modified: Thu, 03 Jul 2025 23:04:28 GMT  
		Size: 21.0 MB (20971251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481b52666b981ec99f99b98b64ef13ff6ce799950970b68817767c966318dc11`  
		Last Modified: Thu, 03 Jul 2025 23:04:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a3724a01f76e5128bdebeeb89d8f42b63b2e987403c91e1f1f5c084c63ffee`  
		Last Modified: Thu, 03 Jul 2025 23:04:22 GMT  
		Size: 20.2 KB (20205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755a5679cebfbcec196508684d58f3d3479a8923825702cea8057be9ea0509ea`  
		Last Modified: Thu, 03 Jul 2025 23:04:25 GMT  
		Size: 20.2 KB (20204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c852688dfb4eb3338fa2b359258f4def968d8542cb467086d1eeea1f28905a74`  
		Last Modified: Thu, 03 Jul 2025 23:13:02 GMT  
		Size: 33.9 MB (33928299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c622ee0a80d81cfef14283072f36dba68467de22ad3d6eb6da4af6de1560b45`  
		Last Modified: Thu, 03 Jul 2025 23:13:00 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e46b6d68b19d40cae9d582d523d29cb5445750042c67b4dcd85a60dfeed7b1d`  
		Last Modified: Thu, 03 Jul 2025 23:13:02 GMT  
		Size: 820.4 KB (820361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a977cbab4acac7e284670ad25a082da694101e85439356ae5286a8f42f5f31dc`  
		Last Modified: Thu, 03 Jul 2025 23:13:01 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86faa8ac4003596a871ab1662361aac1e1c5201c5cfc449f82586191cc1255f5`  
		Last Modified: Thu, 03 Jul 2025 23:13:01 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:c559a7d2440eea7f5c9fb090622a49108e7ce577a37fd104b2a86b33e73d37b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6da2df0aa7c1b16267d729ffc7881169798d1c7d7c0d658c344b4e2eb72c10e`

```dockerfile
```

-	Layers:
	-	`sha256:9f3f5251f9a561a4d427ff51a3736e50496fc6f56a1a01f7892baa753af2a16a`  
		Last Modified: Fri, 04 Jul 2025 01:13:55 GMT  
		Size: 2.2 MB (2175046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1f9403682c82b56933aafbf66ffbb44b9473316fa9703c0243d322d72269fab`  
		Last Modified: Fri, 04 Jul 2025 01:13:55 GMT  
		Size: 31.3 KB (31348 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v6

```console
$ docker pull composer@sha256:e2b50196a498bf516318301d17e1754812c652b1cb1b4aef8bf98a89bd1bd148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77469333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1bad0aebd938e64f2f9d6c7ccaf6c85d7415bb322ec240b81eabfeb48d741c3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4a1a48d371204daac6d50cf0ade3fcbe953b7326556c347d0834eeb808b22f`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 13.6 MB (13647232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7209fb73f851518e0fbc85b54004a573116286207c48ee96ab37833cb8ea1353`  
		Last Modified: Thu, 03 Jul 2025 23:00:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7698dfdb6ae14586a077f81a7e7531ba3d394ab385475ff9c6573114a36ad047`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 22.2 MB (22216193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2822e518605b3410372bbcdb567b3220dcdbe3fc3a85d76aeeed7414a97ce84`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc23f56a1dfd1eb937c6d0d63cb116029d4ac6193e3b8e0487798f7859b09cf`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb672fb64a4977b38f156870ac6fd28ad3898b39594ead2e5d7a7a25cf62e07a`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f65dda0589cf68df6c1f7a31f2ed36448fe5ac89816b32bef12a62b39575a0`  
		Last Modified: Fri, 04 Jul 2025 01:07:05 GMT  
		Size: 33.8 MB (33807127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af16e8c9f29c59fdf9ae69e6ad7a7f42c68aea017b14dcf169ea15f538efb4e`  
		Last Modified: Fri, 04 Jul 2025 01:07:01 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a14a438fbcc90ca30c5c0ec991fd8be0c7b0045bcb84a8024e31659a0d3b48`  
		Last Modified: Fri, 04 Jul 2025 01:07:01 GMT  
		Size: 820.5 KB (820527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b158de7fb3568a394e48de871c0ea3498efb3301159509001ed1fd223c54d4`  
		Last Modified: Wed, 25 Jun 2025 22:15:59 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae54c6b7690f712d9ed6c572e55edda2a4f98703d5ccf8231cdcc9464c367027`  
		Last Modified: Fri, 04 Jul 2025 01:07:01 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:e685378f23766e35af132e6630f24e30d2bf9d499dd7eddc7137591a01ed6753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 KB (31227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4222e1dceb530beb0faf6358b42874b5eb34aa6b58bf897d879f22afcd42c1a`

```dockerfile
```

-	Layers:
	-	`sha256:bc7ebbfd707900fd28ec922eab6305413e75e3662224a563f21ae914c3e88644`  
		Last Modified: Fri, 04 Jul 2025 01:13:59 GMT  
		Size: 31.2 KB (31227 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v7

```console
$ docker pull composer@sha256:f3949d6210c4853d4e70c327eb54d77fb4008a7d4185c65e455b4f67f54e1a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74007856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5949582ae4b3af19fee7236ce4e6124d3674852ff8d9c1d4e279b6c52aa22467`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f4b8d7b2257f1a6ac3d6d3cc6bf9a4b64ab9fc5d2607c301f7de2c7d6c4f46`  
		Last Modified: Thu, 03 Jul 2025 23:46:20 GMT  
		Size: 13.6 MB (13647249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a41d3b4f0ee7936d37a29b00d6599e6c083cdd6c3c1e87cf67e60c78bed722f`  
		Last Modified: Thu, 03 Jul 2025 23:46:17 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f25659badae5bd6d735e7a8151332a7d70260be40b9bd15903ae5024c69186a`  
		Last Modified: Thu, 03 Jul 2025 23:46:20 GMT  
		Size: 21.0 MB (20968354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9020d050ffd80f0ec4539c880f71565ba7987609cedfc9dc9ff78af7fb53b62b`  
		Last Modified: Thu, 03 Jul 2025 23:46:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9a523c3a709bd62efada35a0a92295ac64b04640f1069b295c0d6889f2487`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210dbe376a53d9ebd8229f86a814b0d26ee3ca102f0e74c6dc09a10a9c343c58`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebcb76101e3ff8f5c34e57b65c480c0f53a9657085c1dd3571c570cc1908dec`  
		Last Modified: Fri, 04 Jul 2025 03:24:53 GMT  
		Size: 32.1 MB (32069935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7837ce17d23c46b208ed90e2deb598eb1aaed88b570cd6b34760d21674e702c`  
		Last Modified: Fri, 04 Jul 2025 03:24:49 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96945c09f40b176ab77a7871c4d0245fc17200393e11f0a86cb15276ffffebe9`  
		Last Modified: Fri, 04 Jul 2025 03:24:49 GMT  
		Size: 810.8 KB (810811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9bea4b503a13b84e2efeffaf50b9aa643a7ac9bbec2d0a88af5e10a9c63041`  
		Last Modified: Fri, 04 Jul 2025 03:24:50 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aace2bbaa356b1919a453abdc3f1926c1872e041d872c73ff36900d640c8a5a2`  
		Last Modified: Fri, 04 Jul 2025 03:24:50 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:1aeece1929aa0c9636b78b6db45b66360f6661dbf8dada85537311bb2e130359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2320e765b2631037672fda62c7b5c948ece89bb914689ebade1b9ee8ea1672a8`

```dockerfile
```

-	Layers:
	-	`sha256:804e6aeffccb78ffebb3871f7fcad9d6e4d21cbf66924b669c8bbbcef3453148`  
		Last Modified: Fri, 04 Jul 2025 04:14:11 GMT  
		Size: 2.2 MB (2175362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2db0ddd6dd1e92805aebf376641b8014a696bf31cef4a90f47df81d601769657`  
		Last Modified: Fri, 04 Jul 2025 04:14:11 GMT  
		Size: 31.4 KB (31442 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:8f286e6030c88da3ebf654805893416ce91c0ff0b6c587922c758719addd7866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76642077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7fc2bfa74eb8329a653fbc48ce981ae1b47ba41c1dfbdf3bdc798f246890e0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d74afa414d93be74315fb2fbbededff31189950343736eb9412b26b4f530d1a`  
		Last Modified: Fri, 20 Jun 2025 19:32:29 GMT  
		Size: 3.5 MB (3470712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91ea4522a211c5e50ab5b22083b52449e7ad38398a1f6e5dad24e4a62961906`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b695911010ae65b6cf4c4b5ac350b27932e3b4b29077f6094baa473db50fb5`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e2341d4b1828e7c29626f05458e9c7ac77b849f7fa211122c5e49f3db640c2`  
		Last Modified: Wed, 25 Jun 2025 19:58:30 GMT  
		Size: 13.6 MB (13640504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2214385dee2a6502125f514cfafec9ffbab10a83686ed1edebefbe13bb98e0df`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2192f9a8f7dc985e1b1534af7a423269d9525cd446882c0b66bc83bd73c1d`  
		Last Modified: Wed, 25 Jun 2025 19:58:29 GMT  
		Size: 20.5 MB (20519110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7813f4e30ce21280209e560b03ffd244261e042d03b4f926c87197d856e4d07a`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5659da52250b6def060ce2459caf69d028600439407c5609ffb01e17d290d0a`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 20.0 KB (19995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed11a0655a2eb0f0eae0b13f815d1385ec0d4bc0fc0d3e23f5c2e3aed8e1799`  
		Last Modified: Wed, 25 Jun 2025 19:58:28 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db90ec20dde1245e26657e9eeab7a68a4f381ea6442f98f105cfc54ce54e3a0b`  
		Last Modified: Thu, 26 Jun 2025 00:27:56 GMT  
		Size: 34.0 MB (34010879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb4fdb28ebd43bf90c0134d109bd7f9e79aa657ab4e9e040a42ac1d008e71aa`  
		Last Modified: Thu, 26 Jun 2025 00:27:53 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6ec42a724f2aeefbcb1a20585daef187b07891cf75207c6c8db8117c63f9dc`  
		Last Modified: Thu, 26 Jun 2025 00:27:53 GMT  
		Size: 820.1 KB (820096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c471c3b23b3d1c864515b5a0b7cb90ce65eeeab79a4a63f4124a62b97d0a47`  
		Last Modified: Thu, 26 Jun 2025 00:27:54 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86049f63a03e6d1fc9d7a24051761f819a9295c93f7a01b04a0aa6399c11a3f`  
		Last Modified: Thu, 26 Jun 2025 00:27:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:cc3d9242f043df599446e6c0b5e5f1a301af00ffedac8d01124c669a5f4fbc83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7786c5b0b76b9606b04ac037989fe51ed5022aa69503163ea017ac00f4988cc7`

```dockerfile
```

-	Layers:
	-	`sha256:0a7c6843ff21da43780c0935db32f4b4a9f1781127257f6fbca18f55263c549d`  
		Last Modified: Thu, 26 Jun 2025 01:13:57 GMT  
		Size: 2.2 MB (2175178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75d88db614b9377920d6ef117f33d1dc25945865090eb46f2ebed565a1843b39`  
		Last Modified: Thu, 26 Jun 2025 01:13:58 GMT  
		Size: 31.5 KB (31461 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; 386

```console
$ docker pull composer@sha256:3549d1950413df9cf9ec5dc3cba56b8a4003b398f6aaa586dabe82fe4561687e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79886978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f414549109ad3eaf016596d8b177151fdd48b457782dd8dd896c90ef88a8d3e3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4579a4802acae62f9995bc4ca35846cfa477f9a889ce0fb2017ac6630b78bd4a`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 5.8 MB (5806973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57074fe130dea7f1367879dc4bc435c31dce84ecd32b48ea0a63d35b4a08b836`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7e9cf52dab21b2f526412767a5e92e23eeb507ad11d31f9bf4391ad5eb6a66`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee47d22d22648a57b652a67b201fb0e169513c91be3eec67cb726ba70e375a83`  
		Last Modified: Thu, 03 Jul 2025 23:05:02 GMT  
		Size: 13.6 MB (13647238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ed9c7929ede2d39288b5cdc1a881693463f9694eab366fbb269e70c0d92a49`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63b1c24d7566d919e950b1eaf0a78b66a3bebc8b853f7dac99909776dbae0f1`  
		Last Modified: Thu, 03 Jul 2025 23:05:04 GMT  
		Size: 21.5 MB (21500663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f235298ca3bcb11577f52427a9e9abe5f5708168ce3e6f7a92e3516e12f33f6`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3069db4b5ea73d2b8c2f80770d98b1ecf8fc539f7fcb87b04c2a4d4c1d2747`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 20.2 KB (20195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af93b74a51d1b8b0d9adaa24d025147b9bbb65f3dea67b796f0959416093750`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 20.2 KB (20192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8afe5fb2921fe882cd785fafb8a340bc48fa984eaeb95084167790e1303e977`  
		Last Modified: Thu, 03 Jul 2025 23:12:10 GMT  
		Size: 34.4 MB (34436630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f1c0fa4f5c61d324236c0742a29d9c95bfd3957e20bf4b0b2737ca6d553db7`  
		Last Modified: Thu, 03 Jul 2025 23:12:08 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a0f472aa74942d9a4ee3c0864e5be87ebfd153fe0626ec341f9e4bf8532dd8`  
		Last Modified: Thu, 03 Jul 2025 23:12:08 GMT  
		Size: 834.2 KB (834207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4accc71185fa51ed185fc3226e03f27c8bf432a8af67578471b49317a5d6f501`  
		Last Modified: Thu, 03 Jul 2025 23:12:07 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d8365033a3cd146c7ce81b6969d385bc6830b8b0e7b79f9b8178fe789738e0`  
		Last Modified: Thu, 03 Jul 2025 23:12:07 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:78d5e6ade889c8d8ab29ae66c8b2c10b66b6e8ff4c2d587f7b6c704c44bbf784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b7cdd657a2cd5660845907325e60ef43285c10450db487f79e4f039bec77e1`

```dockerfile
```

-	Layers:
	-	`sha256:fa6faf45644f32be1508f47e007d90b37c699e54e366da94d5110b2450da5b12`  
		Last Modified: Fri, 04 Jul 2025 01:14:11 GMT  
		Size: 2.2 MB (2174834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3844137036bf9a81ac64e5bd8df05c0abf34b7d05ae60974c75f020d99ff72e9`  
		Last Modified: Fri, 04 Jul 2025 01:14:12 GMT  
		Size: 31.3 KB (31316 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; ppc64le

```console
$ docker pull composer@sha256:cb811f7a53815aaff13d20e33272b43032a9870c7545cf239a2b7d78d015c859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81352455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70c2739af288fd915ffad2abad92a531272beeca8ee264dfc05bae5210a568f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7db3af28cc31124a8bce98c13cd1b2512963d13f437d0d67f9918df0d57d2b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 5.9 MB (5946924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ec39d79edfa484fac002ed8c640f17ae8077df4dce88811d8d186865593a6b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 939.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2995d4272705fc452f2b3ea9e2d118681efbad9f858c7743f6f69364d73a50`  
		Last Modified: Thu, 03 Jul 2025 23:15:35 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da4669ab0266f9dd895304e7c92d52e7df1b0acfdc30e6abf0d73fd20c6d09a`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 13.6 MB (13647243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdb584c1e59e66bf7047b954cfc1e41ae7df62560b963934f349b9bd0a11fed`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dff158c4fec087bdd22d80d469c14bd7f5e8a7d72d9a682db56d77c7977e55f`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 21.9 MB (21877134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa09d11c80e8896e162d36345eb3a1cf062f1ba207ed29c537b7783eb818f415`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09daff9fd7af3987bc24f46923dc89bca4e186069874ea11f88390e02dbca5a8`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1d9e25cff60aeed589359ca184c52454f63361a6309e3c363d0d97c227e006`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcefe2124ab8f2442794aaabac7f9422c8d266cee3bbfbb30c3cea3b0f0943f6`  
		Last Modified: Fri, 04 Jul 2025 02:29:48 GMT  
		Size: 35.3 MB (35279082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7315eb9406973e6ea300692e85a137454ee79d74bbb5b71ff352feab46e7c24`  
		Last Modified: Fri, 04 Jul 2025 02:29:46 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25eec6677352d68955b0c10e8094221f23fc06aef202fbc10253c6c4e08f771c`  
		Last Modified: Fri, 04 Jul 2025 02:29:46 GMT  
		Size: 827.0 KB (827027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad00320a6985a0b0a5499c7098e1eb623468009265828215ae95bfb5e45752e2`  
		Last Modified: Fri, 04 Jul 2025 02:29:46 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12ce73e32b7af06aeddeb151281962f8ffd52453e3d47450a02a290baa00a6a`  
		Last Modified: Fri, 04 Jul 2025 02:29:45 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:019b8c31fae7edd2a39df33dd433d1b9dd96ccaafb9d6241bd32758eb9bc8f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f6a30a1405b7d0430cd2b2fbe71c24ee6b41cdd1d100cd0484effeeceb427b`

```dockerfile
```

-	Layers:
	-	`sha256:5008b24787427934003444e4aa7353b81254b5e480b7e94064d7c0ef7caab0d2`  
		Last Modified: Fri, 04 Jul 2025 04:14:21 GMT  
		Size: 2.2 MB (2173603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2effc5836e4c06454a9dd7f3af58faef337b470d29c16e4837f8c37097d65c22`  
		Last Modified: Fri, 04 Jul 2025 04:14:22 GMT  
		Size: 31.4 KB (31390 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; riscv64

```console
$ docker pull composer@sha256:9860f66c267457248e2763c6a09e85eb82ceb877f6d62a9e676ba6c8ae4187ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73116976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8966d79120c2abe2947477d17e117a3104862944b5f4e13ef23367ead908a2c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d0224769088850e26eb3ba2638a8a3febc4b65991ac8cc63dc3f29cf199070`  
		Last Modified: Wed, 11 Jun 2025 05:05:11 GMT  
		Size: 13.6 MB (13640513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a45f979f3844cfaf9ad9f1a00668b3bb56bc478c711f2d939a7dba0c2ed6e1`  
		Last Modified: Wed, 11 Jun 2025 02:39:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b864e2d5fb63463e7b594794f1b0077ef70793371e80280a29b09008bb9771a`  
		Last Modified: Wed, 11 Jun 2025 05:05:14 GMT  
		Size: 20.4 MB (20388593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91ae988832dcf22e179ec800eee279369b0d1b8a4129c2bd761a392671d8d32`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5d276f1eb8afbe6e12101788a8d8d2c68f0875a801fca945c95b68b009ee44`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033c69f0ad5808ebac07aefd6d1a9c0933c09e134334a8bd72a2f49fb7ed2297`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 20.0 KB (19999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7d4367f9b25dba1c9057a363403805d1f3ffce81d401bb89eaa3652ee82d83`  
		Last Modified: Thu, 26 Jun 2025 08:33:02 GMT  
		Size: 31.1 MB (31107678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a85da3fdbf5b1c41e6f68043dc7ff3cb2ef316082fa092b6f23657dffda19a1`  
		Last Modified: Thu, 26 Jun 2025 08:32:59 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7494a442b1a2a3710ab64d55620187bf77c0d16ae5055db9f579c4613fc818`  
		Last Modified: Thu, 26 Jun 2025 08:32:59 GMT  
		Size: 818.2 KB (818166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb79f82b329094c3615c093e293350ba5ba421f1a9af75f3edfda9333a8544ce`  
		Last Modified: Thu, 26 Jun 2025 08:32:59 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9e9900ee8d756b449b4fd43c55d64c8e8395d9abf19cefb38fa404c3b7bfa2`  
		Last Modified: Thu, 26 Jun 2025 08:33:00 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:d4dcc48985653e30399123cfa46b169aa591904b480bc2df5ba88df19e87917c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4124f1fb2e0f031c7b2758e04efcd50a6e073195d783b727ba466240a5c7408e`

```dockerfile
```

-	Layers:
	-	`sha256:cc65df97003e1fdf43a52d8ff3ea55f84dfa01ea4c263ceb697e09918c64f9e7`  
		Last Modified: Thu, 26 Jun 2025 10:13:52 GMT  
		Size: 2.2 MB (2171862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f19f57694101dadef618bbb4001a3dda36cac3b1d2a49238a8e065cb866f0390`  
		Last Modified: Thu, 26 Jun 2025 10:13:52 GMT  
		Size: 31.4 KB (31381 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; s390x

```console
$ docker pull composer@sha256:bfafe9ebf051d29ab62425bddadc2d0c29cb2ad8d1ad6b9ee5292fe8ebaaf5aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77385107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e072172fb388d232784b4da30e57c08bb49213b6dbe3c7b548c142ab3229d8e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abd3e67b018bcd8c0aa4d0434d7ec04dcdb3a3cfbf444a313e2be49d0524ec2`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 5.9 MB (5932552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f41e4866617495859c5133b898f769b3867a6a3ae061aa9561da765981c5ad`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9335ac6e22dd0c0b2e07f4a5406c437168067a987662ebd8bcd3b269496018`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da3506587d8ded424a7c5730d972ae6f1735f6afc1a325c7e9f83474f399fde`  
		Last Modified: Thu, 03 Jul 2025 23:16:27 GMT  
		Size: 13.6 MB (13647264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671a375a1790dbb9b0d83c7dd0560e7f6e75fb5b06afbc76019557052c897e5a`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dc301a9ae8a743478269ed0a476a3abb5ea1e3f156da87ce855397d9ddef91`  
		Last Modified: Thu, 03 Jul 2025 23:16:26 GMT  
		Size: 21.5 MB (21450357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1074498264e134b44d0edcde237cf3cfadba39197115581cfd4b9a9c5ba0fa`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1658861fe310f53081a1e605b2427a938ceddc66bacb97178d77404b333d65a1`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105bedc3ea3fb0ab6591d908f480b2bb3c119411d1ba9dc0c0e9fd62b45f2a39`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb11fbf2308810b649dff18139a7f4e9d809ae768cc36f3d15ec258497a33363`  
		Last Modified: Fri, 04 Jul 2025 02:05:49 GMT  
		Size: 31.8 MB (31839057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb18554f4af212841fd6225002512ce8150b2738e7c8d62528fee75319d8df8`  
		Last Modified: Fri, 04 Jul 2025 02:05:34 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284f923b57510b467a904df0763fb094a786ca5d5efb9dee33c4ff2797f13c8e`  
		Last Modified: Fri, 04 Jul 2025 02:05:34 GMT  
		Size: 823.5 KB (823492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfdf27edf84b4552716698c0cd4a8bbfaf9958d22ae949cfb348d8b50039650`  
		Last Modified: Fri, 04 Jul 2025 02:05:35 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d7d8932667431a132d5dede93fa60ca30f5b39341f1d7072d41f69664e76d2`  
		Last Modified: Fri, 04 Jul 2025 02:05:35 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:fb7faf5cf8175892348a10dcccdc3788d55b475053ce50aeeb7baaee7c5cee98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7232a4fe93a4a4091b9b05b21f019324afcc9c77070a0989f74e7c2670939b4`

```dockerfile
```

-	Layers:
	-	`sha256:b4efb1ad9741df2550ba69fd17eb7147daf5a58b8466e93bdfda30213fdaa5d6`  
		Last Modified: Fri, 04 Jul 2025 04:14:28 GMT  
		Size: 2.2 MB (2171658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef5f689fa4321525c672850bf67bd7494047ab6efa85d99218ec401a6141c94`  
		Last Modified: Fri, 04 Jul 2025 04:14:29 GMT  
		Size: 31.3 KB (31348 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2.25`

```console
$ docker pull composer@sha256:d3851732b404b46cc3079f0ba6a2f54fb112f05d652cfb88bcd329f6f1922762
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
$ docker pull composer@sha256:c55bbcc0b5116f3ada5b2b794253e8d642d534800f5d711ec781a0631a511b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79153683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bfb9c90c0dd2a8370857b01de5e68a396844fc9b3eb4036bcee5238053fcd1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b94662290ef2237915af922ad14ae2b406eccea26d9201aa949ea52f20b737f`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 5.9 MB (5944403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498a67832465ef6dae00170ccca088bdbc63d05a197e0ba1403442805169a06a`  
		Last Modified: Thu, 03 Jul 2025 23:04:16 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53785dc48fc021d1c3f9c46a776ead61a024377fb5e6ab592908501762d63a7`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c87a7802578b0a5aebb57ffea8e543a2d50cff1ec6ffb0941fe8ad61b3a9e6`  
		Last Modified: Thu, 03 Jul 2025 23:04:23 GMT  
		Size: 13.6 MB (13647262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5aa21d09531523ae5c279a8b0eb00236af3b192f428c934050c61f7e1611eaa`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fccbfd125531b00b24f5c4c9c182e17714478e55b96701b7e71d30f7f70f9b`  
		Last Modified: Thu, 03 Jul 2025 23:04:28 GMT  
		Size: 21.0 MB (20971251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481b52666b981ec99f99b98b64ef13ff6ce799950970b68817767c966318dc11`  
		Last Modified: Thu, 03 Jul 2025 23:04:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a3724a01f76e5128bdebeeb89d8f42b63b2e987403c91e1f1f5c084c63ffee`  
		Last Modified: Thu, 03 Jul 2025 23:04:22 GMT  
		Size: 20.2 KB (20205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755a5679cebfbcec196508684d58f3d3479a8923825702cea8057be9ea0509ea`  
		Last Modified: Thu, 03 Jul 2025 23:04:25 GMT  
		Size: 20.2 KB (20204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c852688dfb4eb3338fa2b359258f4def968d8542cb467086d1eeea1f28905a74`  
		Last Modified: Thu, 03 Jul 2025 23:13:02 GMT  
		Size: 33.9 MB (33928299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c622ee0a80d81cfef14283072f36dba68467de22ad3d6eb6da4af6de1560b45`  
		Last Modified: Thu, 03 Jul 2025 23:13:00 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e46b6d68b19d40cae9d582d523d29cb5445750042c67b4dcd85a60dfeed7b1d`  
		Last Modified: Thu, 03 Jul 2025 23:13:02 GMT  
		Size: 820.4 KB (820361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a977cbab4acac7e284670ad25a082da694101e85439356ae5286a8f42f5f31dc`  
		Last Modified: Thu, 03 Jul 2025 23:13:01 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86faa8ac4003596a871ab1662361aac1e1c5201c5cfc449f82586191cc1255f5`  
		Last Modified: Thu, 03 Jul 2025 23:13:01 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:c559a7d2440eea7f5c9fb090622a49108e7ce577a37fd104b2a86b33e73d37b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6da2df0aa7c1b16267d729ffc7881169798d1c7d7c0d658c344b4e2eb72c10e`

```dockerfile
```

-	Layers:
	-	`sha256:9f3f5251f9a561a4d427ff51a3736e50496fc6f56a1a01f7892baa753af2a16a`  
		Last Modified: Fri, 04 Jul 2025 01:13:55 GMT  
		Size: 2.2 MB (2175046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1f9403682c82b56933aafbf66ffbb44b9473316fa9703c0243d322d72269fab`  
		Last Modified: Fri, 04 Jul 2025 01:13:55 GMT  
		Size: 31.3 KB (31348 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm variant v6

```console
$ docker pull composer@sha256:e2b50196a498bf516318301d17e1754812c652b1cb1b4aef8bf98a89bd1bd148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77469333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1bad0aebd938e64f2f9d6c7ccaf6c85d7415bb322ec240b81eabfeb48d741c3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4a1a48d371204daac6d50cf0ade3fcbe953b7326556c347d0834eeb808b22f`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 13.6 MB (13647232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7209fb73f851518e0fbc85b54004a573116286207c48ee96ab37833cb8ea1353`  
		Last Modified: Thu, 03 Jul 2025 23:00:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7698dfdb6ae14586a077f81a7e7531ba3d394ab385475ff9c6573114a36ad047`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 22.2 MB (22216193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2822e518605b3410372bbcdb567b3220dcdbe3fc3a85d76aeeed7414a97ce84`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc23f56a1dfd1eb937c6d0d63cb116029d4ac6193e3b8e0487798f7859b09cf`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb672fb64a4977b38f156870ac6fd28ad3898b39594ead2e5d7a7a25cf62e07a`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f65dda0589cf68df6c1f7a31f2ed36448fe5ac89816b32bef12a62b39575a0`  
		Last Modified: Fri, 04 Jul 2025 01:07:05 GMT  
		Size: 33.8 MB (33807127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af16e8c9f29c59fdf9ae69e6ad7a7f42c68aea017b14dcf169ea15f538efb4e`  
		Last Modified: Fri, 04 Jul 2025 01:07:01 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a14a438fbcc90ca30c5c0ec991fd8be0c7b0045bcb84a8024e31659a0d3b48`  
		Last Modified: Fri, 04 Jul 2025 01:07:01 GMT  
		Size: 820.5 KB (820527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b158de7fb3568a394e48de871c0ea3498efb3301159509001ed1fd223c54d4`  
		Last Modified: Wed, 25 Jun 2025 22:15:59 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae54c6b7690f712d9ed6c572e55edda2a4f98703d5ccf8231cdcc9464c367027`  
		Last Modified: Fri, 04 Jul 2025 01:07:01 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:e685378f23766e35af132e6630f24e30d2bf9d499dd7eddc7137591a01ed6753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 KB (31227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4222e1dceb530beb0faf6358b42874b5eb34aa6b58bf897d879f22afcd42c1a`

```dockerfile
```

-	Layers:
	-	`sha256:bc7ebbfd707900fd28ec922eab6305413e75e3662224a563f21ae914c3e88644`  
		Last Modified: Fri, 04 Jul 2025 01:13:59 GMT  
		Size: 31.2 KB (31227 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm variant v7

```console
$ docker pull composer@sha256:f3949d6210c4853d4e70c327eb54d77fb4008a7d4185c65e455b4f67f54e1a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74007856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5949582ae4b3af19fee7236ce4e6124d3674852ff8d9c1d4e279b6c52aa22467`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f4b8d7b2257f1a6ac3d6d3cc6bf9a4b64ab9fc5d2607c301f7de2c7d6c4f46`  
		Last Modified: Thu, 03 Jul 2025 23:46:20 GMT  
		Size: 13.6 MB (13647249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a41d3b4f0ee7936d37a29b00d6599e6c083cdd6c3c1e87cf67e60c78bed722f`  
		Last Modified: Thu, 03 Jul 2025 23:46:17 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f25659badae5bd6d735e7a8151332a7d70260be40b9bd15903ae5024c69186a`  
		Last Modified: Thu, 03 Jul 2025 23:46:20 GMT  
		Size: 21.0 MB (20968354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9020d050ffd80f0ec4539c880f71565ba7987609cedfc9dc9ff78af7fb53b62b`  
		Last Modified: Thu, 03 Jul 2025 23:46:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9a523c3a709bd62efada35a0a92295ac64b04640f1069b295c0d6889f2487`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210dbe376a53d9ebd8229f86a814b0d26ee3ca102f0e74c6dc09a10a9c343c58`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebcb76101e3ff8f5c34e57b65c480c0f53a9657085c1dd3571c570cc1908dec`  
		Last Modified: Fri, 04 Jul 2025 03:24:53 GMT  
		Size: 32.1 MB (32069935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7837ce17d23c46b208ed90e2deb598eb1aaed88b570cd6b34760d21674e702c`  
		Last Modified: Fri, 04 Jul 2025 03:24:49 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96945c09f40b176ab77a7871c4d0245fc17200393e11f0a86cb15276ffffebe9`  
		Last Modified: Fri, 04 Jul 2025 03:24:49 GMT  
		Size: 810.8 KB (810811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9bea4b503a13b84e2efeffaf50b9aa643a7ac9bbec2d0a88af5e10a9c63041`  
		Last Modified: Fri, 04 Jul 2025 03:24:50 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aace2bbaa356b1919a453abdc3f1926c1872e041d872c73ff36900d640c8a5a2`  
		Last Modified: Fri, 04 Jul 2025 03:24:50 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:1aeece1929aa0c9636b78b6db45b66360f6661dbf8dada85537311bb2e130359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2320e765b2631037672fda62c7b5c948ece89bb914689ebade1b9ee8ea1672a8`

```dockerfile
```

-	Layers:
	-	`sha256:804e6aeffccb78ffebb3871f7fcad9d6e4d21cbf66924b669c8bbbcef3453148`  
		Last Modified: Fri, 04 Jul 2025 04:14:11 GMT  
		Size: 2.2 MB (2175362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2db0ddd6dd1e92805aebf376641b8014a696bf31cef4a90f47df81d601769657`  
		Last Modified: Fri, 04 Jul 2025 04:14:11 GMT  
		Size: 31.4 KB (31442 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:8f286e6030c88da3ebf654805893416ce91c0ff0b6c587922c758719addd7866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76642077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7fc2bfa74eb8329a653fbc48ce981ae1b47ba41c1dfbdf3bdc798f246890e0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d74afa414d93be74315fb2fbbededff31189950343736eb9412b26b4f530d1a`  
		Last Modified: Fri, 20 Jun 2025 19:32:29 GMT  
		Size: 3.5 MB (3470712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91ea4522a211c5e50ab5b22083b52449e7ad38398a1f6e5dad24e4a62961906`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b695911010ae65b6cf4c4b5ac350b27932e3b4b29077f6094baa473db50fb5`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e2341d4b1828e7c29626f05458e9c7ac77b849f7fa211122c5e49f3db640c2`  
		Last Modified: Wed, 25 Jun 2025 19:58:30 GMT  
		Size: 13.6 MB (13640504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2214385dee2a6502125f514cfafec9ffbab10a83686ed1edebefbe13bb98e0df`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2192f9a8f7dc985e1b1534af7a423269d9525cd446882c0b66bc83bd73c1d`  
		Last Modified: Wed, 25 Jun 2025 19:58:29 GMT  
		Size: 20.5 MB (20519110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7813f4e30ce21280209e560b03ffd244261e042d03b4f926c87197d856e4d07a`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5659da52250b6def060ce2459caf69d028600439407c5609ffb01e17d290d0a`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 20.0 KB (19995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed11a0655a2eb0f0eae0b13f815d1385ec0d4bc0fc0d3e23f5c2e3aed8e1799`  
		Last Modified: Wed, 25 Jun 2025 19:58:28 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db90ec20dde1245e26657e9eeab7a68a4f381ea6442f98f105cfc54ce54e3a0b`  
		Last Modified: Thu, 26 Jun 2025 00:27:56 GMT  
		Size: 34.0 MB (34010879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb4fdb28ebd43bf90c0134d109bd7f9e79aa657ab4e9e040a42ac1d008e71aa`  
		Last Modified: Thu, 26 Jun 2025 00:27:53 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6ec42a724f2aeefbcb1a20585daef187b07891cf75207c6c8db8117c63f9dc`  
		Last Modified: Thu, 26 Jun 2025 00:27:53 GMT  
		Size: 820.1 KB (820096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c471c3b23b3d1c864515b5a0b7cb90ce65eeeab79a4a63f4124a62b97d0a47`  
		Last Modified: Thu, 26 Jun 2025 00:27:54 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86049f63a03e6d1fc9d7a24051761f819a9295c93f7a01b04a0aa6399c11a3f`  
		Last Modified: Thu, 26 Jun 2025 00:27:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:cc3d9242f043df599446e6c0b5e5f1a301af00ffedac8d01124c669a5f4fbc83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7786c5b0b76b9606b04ac037989fe51ed5022aa69503163ea017ac00f4988cc7`

```dockerfile
```

-	Layers:
	-	`sha256:0a7c6843ff21da43780c0935db32f4b4a9f1781127257f6fbca18f55263c549d`  
		Last Modified: Thu, 26 Jun 2025 01:13:57 GMT  
		Size: 2.2 MB (2175178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75d88db614b9377920d6ef117f33d1dc25945865090eb46f2ebed565a1843b39`  
		Last Modified: Thu, 26 Jun 2025 01:13:58 GMT  
		Size: 31.5 KB (31461 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; 386

```console
$ docker pull composer@sha256:3549d1950413df9cf9ec5dc3cba56b8a4003b398f6aaa586dabe82fe4561687e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79886978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f414549109ad3eaf016596d8b177151fdd48b457782dd8dd896c90ef88a8d3e3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4579a4802acae62f9995bc4ca35846cfa477f9a889ce0fb2017ac6630b78bd4a`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 5.8 MB (5806973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57074fe130dea7f1367879dc4bc435c31dce84ecd32b48ea0a63d35b4a08b836`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7e9cf52dab21b2f526412767a5e92e23eeb507ad11d31f9bf4391ad5eb6a66`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee47d22d22648a57b652a67b201fb0e169513c91be3eec67cb726ba70e375a83`  
		Last Modified: Thu, 03 Jul 2025 23:05:02 GMT  
		Size: 13.6 MB (13647238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ed9c7929ede2d39288b5cdc1a881693463f9694eab366fbb269e70c0d92a49`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63b1c24d7566d919e950b1eaf0a78b66a3bebc8b853f7dac99909776dbae0f1`  
		Last Modified: Thu, 03 Jul 2025 23:05:04 GMT  
		Size: 21.5 MB (21500663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f235298ca3bcb11577f52427a9e9abe5f5708168ce3e6f7a92e3516e12f33f6`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3069db4b5ea73d2b8c2f80770d98b1ecf8fc539f7fcb87b04c2a4d4c1d2747`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 20.2 KB (20195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af93b74a51d1b8b0d9adaa24d025147b9bbb65f3dea67b796f0959416093750`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 20.2 KB (20192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8afe5fb2921fe882cd785fafb8a340bc48fa984eaeb95084167790e1303e977`  
		Last Modified: Thu, 03 Jul 2025 23:12:10 GMT  
		Size: 34.4 MB (34436630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f1c0fa4f5c61d324236c0742a29d9c95bfd3957e20bf4b0b2737ca6d553db7`  
		Last Modified: Thu, 03 Jul 2025 23:12:08 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a0f472aa74942d9a4ee3c0864e5be87ebfd153fe0626ec341f9e4bf8532dd8`  
		Last Modified: Thu, 03 Jul 2025 23:12:08 GMT  
		Size: 834.2 KB (834207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4accc71185fa51ed185fc3226e03f27c8bf432a8af67578471b49317a5d6f501`  
		Last Modified: Thu, 03 Jul 2025 23:12:07 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d8365033a3cd146c7ce81b6969d385bc6830b8b0e7b79f9b8178fe789738e0`  
		Last Modified: Thu, 03 Jul 2025 23:12:07 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:78d5e6ade889c8d8ab29ae66c8b2c10b66b6e8ff4c2d587f7b6c704c44bbf784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b7cdd657a2cd5660845907325e60ef43285c10450db487f79e4f039bec77e1`

```dockerfile
```

-	Layers:
	-	`sha256:fa6faf45644f32be1508f47e007d90b37c699e54e366da94d5110b2450da5b12`  
		Last Modified: Fri, 04 Jul 2025 01:14:11 GMT  
		Size: 2.2 MB (2174834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3844137036bf9a81ac64e5bd8df05c0abf34b7d05ae60974c75f020d99ff72e9`  
		Last Modified: Fri, 04 Jul 2025 01:14:12 GMT  
		Size: 31.3 KB (31316 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; ppc64le

```console
$ docker pull composer@sha256:cb811f7a53815aaff13d20e33272b43032a9870c7545cf239a2b7d78d015c859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81352455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70c2739af288fd915ffad2abad92a531272beeca8ee264dfc05bae5210a568f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7db3af28cc31124a8bce98c13cd1b2512963d13f437d0d67f9918df0d57d2b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 5.9 MB (5946924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ec39d79edfa484fac002ed8c640f17ae8077df4dce88811d8d186865593a6b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 939.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2995d4272705fc452f2b3ea9e2d118681efbad9f858c7743f6f69364d73a50`  
		Last Modified: Thu, 03 Jul 2025 23:15:35 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da4669ab0266f9dd895304e7c92d52e7df1b0acfdc30e6abf0d73fd20c6d09a`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 13.6 MB (13647243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdb584c1e59e66bf7047b954cfc1e41ae7df62560b963934f349b9bd0a11fed`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dff158c4fec087bdd22d80d469c14bd7f5e8a7d72d9a682db56d77c7977e55f`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 21.9 MB (21877134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa09d11c80e8896e162d36345eb3a1cf062f1ba207ed29c537b7783eb818f415`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09daff9fd7af3987bc24f46923dc89bca4e186069874ea11f88390e02dbca5a8`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1d9e25cff60aeed589359ca184c52454f63361a6309e3c363d0d97c227e006`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcefe2124ab8f2442794aaabac7f9422c8d266cee3bbfbb30c3cea3b0f0943f6`  
		Last Modified: Fri, 04 Jul 2025 02:29:48 GMT  
		Size: 35.3 MB (35279082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7315eb9406973e6ea300692e85a137454ee79d74bbb5b71ff352feab46e7c24`  
		Last Modified: Fri, 04 Jul 2025 02:29:46 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25eec6677352d68955b0c10e8094221f23fc06aef202fbc10253c6c4e08f771c`  
		Last Modified: Fri, 04 Jul 2025 02:29:46 GMT  
		Size: 827.0 KB (827027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad00320a6985a0b0a5499c7098e1eb623468009265828215ae95bfb5e45752e2`  
		Last Modified: Fri, 04 Jul 2025 02:29:46 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12ce73e32b7af06aeddeb151281962f8ffd52453e3d47450a02a290baa00a6a`  
		Last Modified: Fri, 04 Jul 2025 02:29:45 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:019b8c31fae7edd2a39df33dd433d1b9dd96ccaafb9d6241bd32758eb9bc8f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f6a30a1405b7d0430cd2b2fbe71c24ee6b41cdd1d100cd0484effeeceb427b`

```dockerfile
```

-	Layers:
	-	`sha256:5008b24787427934003444e4aa7353b81254b5e480b7e94064d7c0ef7caab0d2`  
		Last Modified: Fri, 04 Jul 2025 04:14:21 GMT  
		Size: 2.2 MB (2173603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2effc5836e4c06454a9dd7f3af58faef337b470d29c16e4837f8c37097d65c22`  
		Last Modified: Fri, 04 Jul 2025 04:14:22 GMT  
		Size: 31.4 KB (31390 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; riscv64

```console
$ docker pull composer@sha256:9860f66c267457248e2763c6a09e85eb82ceb877f6d62a9e676ba6c8ae4187ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73116976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8966d79120c2abe2947477d17e117a3104862944b5f4e13ef23367ead908a2c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d0224769088850e26eb3ba2638a8a3febc4b65991ac8cc63dc3f29cf199070`  
		Last Modified: Wed, 11 Jun 2025 05:05:11 GMT  
		Size: 13.6 MB (13640513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a45f979f3844cfaf9ad9f1a00668b3bb56bc478c711f2d939a7dba0c2ed6e1`  
		Last Modified: Wed, 11 Jun 2025 02:39:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b864e2d5fb63463e7b594794f1b0077ef70793371e80280a29b09008bb9771a`  
		Last Modified: Wed, 11 Jun 2025 05:05:14 GMT  
		Size: 20.4 MB (20388593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91ae988832dcf22e179ec800eee279369b0d1b8a4129c2bd761a392671d8d32`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5d276f1eb8afbe6e12101788a8d8d2c68f0875a801fca945c95b68b009ee44`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033c69f0ad5808ebac07aefd6d1a9c0933c09e134334a8bd72a2f49fb7ed2297`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 20.0 KB (19999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7d4367f9b25dba1c9057a363403805d1f3ffce81d401bb89eaa3652ee82d83`  
		Last Modified: Thu, 26 Jun 2025 08:33:02 GMT  
		Size: 31.1 MB (31107678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a85da3fdbf5b1c41e6f68043dc7ff3cb2ef316082fa092b6f23657dffda19a1`  
		Last Modified: Thu, 26 Jun 2025 08:32:59 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7494a442b1a2a3710ab64d55620187bf77c0d16ae5055db9f579c4613fc818`  
		Last Modified: Thu, 26 Jun 2025 08:32:59 GMT  
		Size: 818.2 KB (818166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb79f82b329094c3615c093e293350ba5ba421f1a9af75f3edfda9333a8544ce`  
		Last Modified: Thu, 26 Jun 2025 08:32:59 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9e9900ee8d756b449b4fd43c55d64c8e8395d9abf19cefb38fa404c3b7bfa2`  
		Last Modified: Thu, 26 Jun 2025 08:33:00 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:d4dcc48985653e30399123cfa46b169aa591904b480bc2df5ba88df19e87917c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4124f1fb2e0f031c7b2758e04efcd50a6e073195d783b727ba466240a5c7408e`

```dockerfile
```

-	Layers:
	-	`sha256:cc65df97003e1fdf43a52d8ff3ea55f84dfa01ea4c263ceb697e09918c64f9e7`  
		Last Modified: Thu, 26 Jun 2025 10:13:52 GMT  
		Size: 2.2 MB (2171862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f19f57694101dadef618bbb4001a3dda36cac3b1d2a49238a8e065cb866f0390`  
		Last Modified: Thu, 26 Jun 2025 10:13:52 GMT  
		Size: 31.4 KB (31381 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; s390x

```console
$ docker pull composer@sha256:bfafe9ebf051d29ab62425bddadc2d0c29cb2ad8d1ad6b9ee5292fe8ebaaf5aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77385107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e072172fb388d232784b4da30e57c08bb49213b6dbe3c7b548c142ab3229d8e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abd3e67b018bcd8c0aa4d0434d7ec04dcdb3a3cfbf444a313e2be49d0524ec2`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 5.9 MB (5932552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f41e4866617495859c5133b898f769b3867a6a3ae061aa9561da765981c5ad`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9335ac6e22dd0c0b2e07f4a5406c437168067a987662ebd8bcd3b269496018`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da3506587d8ded424a7c5730d972ae6f1735f6afc1a325c7e9f83474f399fde`  
		Last Modified: Thu, 03 Jul 2025 23:16:27 GMT  
		Size: 13.6 MB (13647264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671a375a1790dbb9b0d83c7dd0560e7f6e75fb5b06afbc76019557052c897e5a`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dc301a9ae8a743478269ed0a476a3abb5ea1e3f156da87ce855397d9ddef91`  
		Last Modified: Thu, 03 Jul 2025 23:16:26 GMT  
		Size: 21.5 MB (21450357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1074498264e134b44d0edcde237cf3cfadba39197115581cfd4b9a9c5ba0fa`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1658861fe310f53081a1e605b2427a938ceddc66bacb97178d77404b333d65a1`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105bedc3ea3fb0ab6591d908f480b2bb3c119411d1ba9dc0c0e9fd62b45f2a39`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb11fbf2308810b649dff18139a7f4e9d809ae768cc36f3d15ec258497a33363`  
		Last Modified: Fri, 04 Jul 2025 02:05:49 GMT  
		Size: 31.8 MB (31839057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb18554f4af212841fd6225002512ce8150b2738e7c8d62528fee75319d8df8`  
		Last Modified: Fri, 04 Jul 2025 02:05:34 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284f923b57510b467a904df0763fb094a786ca5d5efb9dee33c4ff2797f13c8e`  
		Last Modified: Fri, 04 Jul 2025 02:05:34 GMT  
		Size: 823.5 KB (823492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfdf27edf84b4552716698c0cd4a8bbfaf9958d22ae949cfb348d8b50039650`  
		Last Modified: Fri, 04 Jul 2025 02:05:35 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d7d8932667431a132d5dede93fa60ca30f5b39341f1d7072d41f69664e76d2`  
		Last Modified: Fri, 04 Jul 2025 02:05:35 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:fb7faf5cf8175892348a10dcccdc3788d55b475053ce50aeeb7baaee7c5cee98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7232a4fe93a4a4091b9b05b21f019324afcc9c77070a0989f74e7c2670939b4`

```dockerfile
```

-	Layers:
	-	`sha256:b4efb1ad9741df2550ba69fd17eb7147daf5a58b8466e93bdfda30213fdaa5d6`  
		Last Modified: Fri, 04 Jul 2025 04:14:28 GMT  
		Size: 2.2 MB (2171658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef5f689fa4321525c672850bf67bd7494047ab6efa85d99218ec401a6141c94`  
		Last Modified: Fri, 04 Jul 2025 04:14:29 GMT  
		Size: 31.3 KB (31348 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8`

```console
$ docker pull composer@sha256:0eed6733d75c35f13c4794990f22aa04654addc135bc575cd5692572bb3c8935
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
$ docker pull composer@sha256:864a61db30e6203c4a20b777493bc17f9c361303fd6a5e6db2cbbd4c56d5faa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79309733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21295413e1bc8c2201f98d084a45091bf7d8ee2b6514e9bec81c411a8e172682`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.10
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b94662290ef2237915af922ad14ae2b406eccea26d9201aa949ea52f20b737f`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 5.9 MB (5944403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498a67832465ef6dae00170ccca088bdbc63d05a197e0ba1403442805169a06a`  
		Last Modified: Thu, 03 Jul 2025 23:04:16 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53785dc48fc021d1c3f9c46a776ead61a024377fb5e6ab592908501762d63a7`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c87a7802578b0a5aebb57ffea8e543a2d50cff1ec6ffb0941fe8ad61b3a9e6`  
		Last Modified: Thu, 03 Jul 2025 23:04:23 GMT  
		Size: 13.6 MB (13647262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5aa21d09531523ae5c279a8b0eb00236af3b192f428c934050c61f7e1611eaa`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fccbfd125531b00b24f5c4c9c182e17714478e55b96701b7e71d30f7f70f9b`  
		Last Modified: Thu, 03 Jul 2025 23:04:28 GMT  
		Size: 21.0 MB (20971251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481b52666b981ec99f99b98b64ef13ff6ce799950970b68817767c966318dc11`  
		Last Modified: Thu, 03 Jul 2025 23:04:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a3724a01f76e5128bdebeeb89d8f42b63b2e987403c91e1f1f5c084c63ffee`  
		Last Modified: Thu, 03 Jul 2025 23:04:22 GMT  
		Size: 20.2 KB (20205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755a5679cebfbcec196508684d58f3d3479a8923825702cea8057be9ea0509ea`  
		Last Modified: Thu, 03 Jul 2025 23:04:25 GMT  
		Size: 20.2 KB (20204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c852688dfb4eb3338fa2b359258f4def968d8542cb467086d1eeea1f28905a74`  
		Last Modified: Thu, 03 Jul 2025 23:13:02 GMT  
		Size: 33.9 MB (33928299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c622ee0a80d81cfef14283072f36dba68467de22ad3d6eb6da4af6de1560b45`  
		Last Modified: Thu, 03 Jul 2025 23:13:00 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218c0a682557e725de4b4ae1b3d83acabd53d9ce5f23a45ef3e1b3721fea1262`  
		Last Modified: Thu, 03 Jul 2025 23:13:00 GMT  
		Size: 976.4 KB (976411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cc4579c8bd93cd33c1b651f3f52e56ca67655b23b2fc99ae1954c25cfc8630`  
		Last Modified: Thu, 03 Jul 2025 23:13:01 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e141382acfb75c4a31d782c5f0837bb164ef89d645af35d1c815bcdfcf5cac`  
		Last Modified: Thu, 03 Jul 2025 23:13:00 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:d4d4b49e2553833f43684f3a5905521881e8a9dfa954fc06225be2cce9d466bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbf3553c4657aa72f0ba321ebc291fa348abef46a3a72f6d93550521428759f`

```dockerfile
```

-	Layers:
	-	`sha256:3ad72884d89234dbd14e825e71a080c543f84beceb8ee170a45eb4e9be474b08`  
		Last Modified: Fri, 04 Jul 2025 01:13:40 GMT  
		Size: 2.2 MB (2175340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c65c76faf5625b204b8a6440bd9d80740b5757a5f019373204445f59774974eb`  
		Last Modified: Fri, 04 Jul 2025 01:13:41 GMT  
		Size: 31.7 KB (31652 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v6

```console
$ docker pull composer@sha256:648b0bf94ac42dff7872cea189a81b4e25e8be6ae5015b1da330a9c8c31b704f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77625569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0576b47e03b1a0e8e65bd259e7af5895948140096c3afc93f9a0dab0e88a2f48`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.10
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4a1a48d371204daac6d50cf0ade3fcbe953b7326556c347d0834eeb808b22f`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 13.6 MB (13647232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7209fb73f851518e0fbc85b54004a573116286207c48ee96ab37833cb8ea1353`  
		Last Modified: Thu, 03 Jul 2025 23:00:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7698dfdb6ae14586a077f81a7e7531ba3d394ab385475ff9c6573114a36ad047`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 22.2 MB (22216193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2822e518605b3410372bbcdb567b3220dcdbe3fc3a85d76aeeed7414a97ce84`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc23f56a1dfd1eb937c6d0d63cb116029d4ac6193e3b8e0487798f7859b09cf`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb672fb64a4977b38f156870ac6fd28ad3898b39594ead2e5d7a7a25cf62e07a`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f65dda0589cf68df6c1f7a31f2ed36448fe5ac89816b32bef12a62b39575a0`  
		Last Modified: Fri, 04 Jul 2025 01:07:05 GMT  
		Size: 33.8 MB (33807127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af16e8c9f29c59fdf9ae69e6ad7a7f42c68aea017b14dcf169ea15f538efb4e`  
		Last Modified: Fri, 04 Jul 2025 01:07:01 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d70107b5aba54d8f31fb97e22d592810074a1b8f05392fc1093eb44ac667ff8`  
		Last Modified: Fri, 04 Jul 2025 01:08:05 GMT  
		Size: 976.8 KB (976765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb15dc78f78d103edcc744c17908609b087a11d0c10548c3f9d791e07ccbca86`  
		Last Modified: Wed, 25 Jun 2025 20:29:47 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224953665089fda926db4dea1b86110c646109a8a62e68cb13246f46d3d4b95e`  
		Last Modified: Fri, 04 Jul 2025 01:08:04 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:cc5374cca047b9c29c17b890515ce54d573a889881ed1a840b780509ee1a35c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edcc52d9671e580042a8af83c87912d079d008f561c600822f9a3c9d52ccea5b`

```dockerfile
```

-	Layers:
	-	`sha256:70fb45703ae28fcbe74dc9795f343a8920c7c71d06a958b9c23a34a6eb3bfa5d`  
		Last Modified: Fri, 04 Jul 2025 04:13:56 GMT  
		Size: 31.5 KB (31539 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v7

```console
$ docker pull composer@sha256:5c2811e58deda112f1b19ea2a429444944c8ad179727b126774b90672e8e66d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74164142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c019e9b06442cd09ddf2e4b7eb65cdab0d41f4df9e0d782fec975e072b48e76d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.10
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f4b8d7b2257f1a6ac3d6d3cc6bf9a4b64ab9fc5d2607c301f7de2c7d6c4f46`  
		Last Modified: Thu, 03 Jul 2025 23:46:20 GMT  
		Size: 13.6 MB (13647249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a41d3b4f0ee7936d37a29b00d6599e6c083cdd6c3c1e87cf67e60c78bed722f`  
		Last Modified: Thu, 03 Jul 2025 23:46:17 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f25659badae5bd6d735e7a8151332a7d70260be40b9bd15903ae5024c69186a`  
		Last Modified: Thu, 03 Jul 2025 23:46:20 GMT  
		Size: 21.0 MB (20968354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9020d050ffd80f0ec4539c880f71565ba7987609cedfc9dc9ff78af7fb53b62b`  
		Last Modified: Thu, 03 Jul 2025 23:46:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9a523c3a709bd62efada35a0a92295ac64b04640f1069b295c0d6889f2487`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210dbe376a53d9ebd8229f86a814b0d26ee3ca102f0e74c6dc09a10a9c343c58`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebcb76101e3ff8f5c34e57b65c480c0f53a9657085c1dd3571c570cc1908dec`  
		Last Modified: Fri, 04 Jul 2025 03:24:53 GMT  
		Size: 32.1 MB (32069935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7837ce17d23c46b208ed90e2deb598eb1aaed88b570cd6b34760d21674e702c`  
		Last Modified: Fri, 04 Jul 2025 03:24:49 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ad676d7ee639bd12778210b726ccd10b9eead85271834e2b2c6bf311e7240a`  
		Last Modified: Fri, 04 Jul 2025 03:26:21 GMT  
		Size: 967.1 KB (967097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3b74b2060ffea794587392d8e37fc22baa87dbd5c3bee7b016a864f1aea241`  
		Last Modified: Fri, 04 Jul 2025 03:26:20 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb4cff2df01ba4618678e4f893513145e63282a0ad4f1bffe3e362bf8706220`  
		Last Modified: Fri, 04 Jul 2025 03:26:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:3578e71f433b37866bf7a4a743e8b077af4f522455beef6e247b8d02a8e137a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27499b4da1ed9b3f5ac42b35ea64b62305426f552bc2c1c6d49da8d1a84defb`

```dockerfile
```

-	Layers:
	-	`sha256:5f8a22eb1d359ca353b20fa10f9ceb96545b85653ea907d8d75b260e52891e2e`  
		Last Modified: Fri, 04 Jul 2025 04:14:00 GMT  
		Size: 2.2 MB (2175664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e26ba3a9482b3a935d3eb85feaf385751e9d4f79763ed43ff63f893b27554d5d`  
		Last Modified: Fri, 04 Jul 2025 04:14:01 GMT  
		Size: 31.8 KB (31754 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:d2dadc0c40a3554177b591599fb4d6a672330089c735772da89e0220add47f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76798022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d43140056d0abec9110d9e36cc98a921b48be8aac07425b3be37eced18794a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d74afa414d93be74315fb2fbbededff31189950343736eb9412b26b4f530d1a`  
		Last Modified: Fri, 20 Jun 2025 19:32:29 GMT  
		Size: 3.5 MB (3470712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91ea4522a211c5e50ab5b22083b52449e7ad38398a1f6e5dad24e4a62961906`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b695911010ae65b6cf4c4b5ac350b27932e3b4b29077f6094baa473db50fb5`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e2341d4b1828e7c29626f05458e9c7ac77b849f7fa211122c5e49f3db640c2`  
		Last Modified: Wed, 25 Jun 2025 19:58:30 GMT  
		Size: 13.6 MB (13640504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2214385dee2a6502125f514cfafec9ffbab10a83686ed1edebefbe13bb98e0df`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2192f9a8f7dc985e1b1534af7a423269d9525cd446882c0b66bc83bd73c1d`  
		Last Modified: Wed, 25 Jun 2025 19:58:29 GMT  
		Size: 20.5 MB (20519110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7813f4e30ce21280209e560b03ffd244261e042d03b4f926c87197d856e4d07a`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5659da52250b6def060ce2459caf69d028600439407c5609ffb01e17d290d0a`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 20.0 KB (19995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed11a0655a2eb0f0eae0b13f815d1385ec0d4bc0fc0d3e23f5c2e3aed8e1799`  
		Last Modified: Wed, 25 Jun 2025 19:58:28 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db90ec20dde1245e26657e9eeab7a68a4f381ea6442f98f105cfc54ce54e3a0b`  
		Last Modified: Thu, 26 Jun 2025 00:27:56 GMT  
		Size: 34.0 MB (34010879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb4fdb28ebd43bf90c0134d109bd7f9e79aa657ab4e9e040a42ac1d008e71aa`  
		Last Modified: Thu, 26 Jun 2025 00:27:53 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ddf66bb9ba56337081b692d4129b361f983e7f9abd1d5e349d28c1c7eade483`  
		Last Modified: Thu, 26 Jun 2025 00:28:57 GMT  
		Size: 976.0 KB (976041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b24a8ffa2909a504d9bbfc6df46cc2b56d610d921e33e9974ffc838c62bdd1d`  
		Last Modified: Thu, 26 Jun 2025 00:28:57 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821b9dea24a435946ecb336cb8278f7297bed4a94795980b99f141347beab268`  
		Last Modified: Thu, 26 Jun 2025 00:28:57 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:df1144ec9680bd760c06c95a7bfff7150690d287e025712cc341c4a5ffe356df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640d11c5a6cebe938b2fd6fab0e883dbce3befa0419a62d2c446198798adf567`

```dockerfile
```

-	Layers:
	-	`sha256:a7b2a0fdfcdccff2b7138ac64502f1f2fb239077a7b59fa7e206bf3e6f124b5c`  
		Last Modified: Thu, 26 Jun 2025 01:13:48 GMT  
		Size: 2.2 MB (2175484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91b5ec1ac58d000c75aaad3474d0386b5646668bc3b2685875bd6ce02e925b2b`  
		Last Modified: Thu, 26 Jun 2025 01:13:49 GMT  
		Size: 31.8 KB (31777 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; 386

```console
$ docker pull composer@sha256:7ea3337a73dfe929bb2a4e849d7413a67d2f8bece13a67bb7cd0b77e112e54e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80042550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5691a9cad94ac3356a7d1f58071b048add1584758c6ed163996f041ab04e4a8d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.10
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4579a4802acae62f9995bc4ca35846cfa477f9a889ce0fb2017ac6630b78bd4a`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 5.8 MB (5806973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57074fe130dea7f1367879dc4bc435c31dce84ecd32b48ea0a63d35b4a08b836`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7e9cf52dab21b2f526412767a5e92e23eeb507ad11d31f9bf4391ad5eb6a66`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee47d22d22648a57b652a67b201fb0e169513c91be3eec67cb726ba70e375a83`  
		Last Modified: Thu, 03 Jul 2025 23:05:02 GMT  
		Size: 13.6 MB (13647238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ed9c7929ede2d39288b5cdc1a881693463f9694eab366fbb269e70c0d92a49`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63b1c24d7566d919e950b1eaf0a78b66a3bebc8b853f7dac99909776dbae0f1`  
		Last Modified: Thu, 03 Jul 2025 23:05:04 GMT  
		Size: 21.5 MB (21500663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f235298ca3bcb11577f52427a9e9abe5f5708168ce3e6f7a92e3516e12f33f6`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3069db4b5ea73d2b8c2f80770d98b1ecf8fc539f7fcb87b04c2a4d4c1d2747`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 20.2 KB (20195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af93b74a51d1b8b0d9adaa24d025147b9bbb65f3dea67b796f0959416093750`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 20.2 KB (20192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c8ee1962b1a764f17623a97c88eac6b4bcd6264d017309e15662ca58ba4328`  
		Last Modified: Thu, 03 Jul 2025 23:13:04 GMT  
		Size: 34.4 MB (34436697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62967b08a91543e22a6b21fc96ea01449936ec8716111d503430bebb27b9b1cb`  
		Last Modified: Thu, 03 Jul 2025 23:13:00 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30acb5fcf8b4c6c26895514cffa50f5f9943af2422b56fb2d081f516ceedb84a`  
		Last Modified: Thu, 03 Jul 2025 23:13:01 GMT  
		Size: 989.7 KB (989711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431bf78845ea7be375b442b6d6e0b94a886a77fe6982ccd2cae5e6fba720130b`  
		Last Modified: Thu, 03 Jul 2025 23:13:01 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44a7383365beb5c7a1faf0ae044a570043a5793a4b4007761b2d0751cd244da`  
		Last Modified: Thu, 03 Jul 2025 23:13:01 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:fe8fc42c5d819f1d34f4ce945cfdf317de4a0cbb50d3aeddca71d79022c98741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b3db9f01b13546692b4ad51bad36e7e3165c293f4bf1fc24d927922991439d`

```dockerfile
```

-	Layers:
	-	`sha256:40add4385980bb9b06d7a8f0bea17a1228b127a11af5d741d0259be4e26f4bcb`  
		Last Modified: Fri, 04 Jul 2025 01:13:54 GMT  
		Size: 2.2 MB (2175123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fe1485dca730e6cd0aa0fdbb3d1bd1ee70141e35977cd5fdd159ec4fc558945`  
		Last Modified: Fri, 04 Jul 2025 01:13:55 GMT  
		Size: 31.6 KB (31616 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; ppc64le

```console
$ docker pull composer@sha256:78db100203a59f9ca077a0ea16741ec93e078dbb2a52df6ab977a16a05b666ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81508478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60ff07f83bdd829ca9ac347bcd7a91042f0c838a7658f717395cce85d77408c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.10
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7db3af28cc31124a8bce98c13cd1b2512963d13f437d0d67f9918df0d57d2b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 5.9 MB (5946924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ec39d79edfa484fac002ed8c640f17ae8077df4dce88811d8d186865593a6b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 939.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2995d4272705fc452f2b3ea9e2d118681efbad9f858c7743f6f69364d73a50`  
		Last Modified: Thu, 03 Jul 2025 23:15:35 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da4669ab0266f9dd895304e7c92d52e7df1b0acfdc30e6abf0d73fd20c6d09a`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 13.6 MB (13647243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdb584c1e59e66bf7047b954cfc1e41ae7df62560b963934f349b9bd0a11fed`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dff158c4fec087bdd22d80d469c14bd7f5e8a7d72d9a682db56d77c7977e55f`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 21.9 MB (21877134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa09d11c80e8896e162d36345eb3a1cf062f1ba207ed29c537b7783eb818f415`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09daff9fd7af3987bc24f46923dc89bca4e186069874ea11f88390e02dbca5a8`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1d9e25cff60aeed589359ca184c52454f63361a6309e3c363d0d97c227e006`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcefe2124ab8f2442794aaabac7f9422c8d266cee3bbfbb30c3cea3b0f0943f6`  
		Last Modified: Fri, 04 Jul 2025 02:29:48 GMT  
		Size: 35.3 MB (35279082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7315eb9406973e6ea300692e85a137454ee79d74bbb5b71ff352feab46e7c24`  
		Last Modified: Fri, 04 Jul 2025 02:29:46 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4508639e74c9c28c3fb419e0c8c6a031d7291e9393341921ee0f03bd59ecca`  
		Last Modified: Fri, 04 Jul 2025 02:32:05 GMT  
		Size: 983.0 KB (983049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bba142070b7380628289f45cb7efe63e1078c2dee92be982602232fb09fbb5`  
		Last Modified: Fri, 04 Jul 2025 02:32:04 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e42909435644cf68037aa4d86a52d59c7e2e1c9692af7fb3134a361b663960`  
		Last Modified: Fri, 04 Jul 2025 02:32:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:083aa2658271704da9e81255bb7d746de750303a00e3fe499cd00ea99740da16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1895718fc0cd8fbe5ed7357dbf119863fa5506eeb3a93c2a47d7e06a9a0aa085`

```dockerfile
```

-	Layers:
	-	`sha256:0e467847564c6b363f7e9023b8c2aa5c0114ffbbeeb42e175703b015ea07f2c4`  
		Last Modified: Fri, 04 Jul 2025 04:14:10 GMT  
		Size: 2.2 MB (2173903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38a725e262847343f44ce5121a7e45c8b8f973d0ab72ad75bf55dceba889c8d3`  
		Last Modified: Fri, 04 Jul 2025 04:14:11 GMT  
		Size: 31.7 KB (31700 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; riscv64

```console
$ docker pull composer@sha256:e9cf69d00e0485cfc79bbd74de2fcf971c8c0625b61f55964388187353e58dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73273033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387850bcac483e7be49354dc64c55c9837cc316862477690206f7484a1a3972e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d0224769088850e26eb3ba2638a8a3febc4b65991ac8cc63dc3f29cf199070`  
		Last Modified: Wed, 11 Jun 2025 05:05:11 GMT  
		Size: 13.6 MB (13640513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a45f979f3844cfaf9ad9f1a00668b3bb56bc478c711f2d939a7dba0c2ed6e1`  
		Last Modified: Wed, 11 Jun 2025 02:39:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b864e2d5fb63463e7b594794f1b0077ef70793371e80280a29b09008bb9771a`  
		Last Modified: Wed, 11 Jun 2025 05:05:14 GMT  
		Size: 20.4 MB (20388593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91ae988832dcf22e179ec800eee279369b0d1b8a4129c2bd761a392671d8d32`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5d276f1eb8afbe6e12101788a8d8d2c68f0875a801fca945c95b68b009ee44`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033c69f0ad5808ebac07aefd6d1a9c0933c09e134334a8bd72a2f49fb7ed2297`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 20.0 KB (19999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7d4367f9b25dba1c9057a363403805d1f3ffce81d401bb89eaa3652ee82d83`  
		Last Modified: Thu, 26 Jun 2025 08:33:02 GMT  
		Size: 31.1 MB (31107678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a85da3fdbf5b1c41e6f68043dc7ff3cb2ef316082fa092b6f23657dffda19a1`  
		Last Modified: Thu, 26 Jun 2025 08:32:59 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e85546fd2798c3532f47d4372f9fad38a6865cf751f31473179d3d7f11577b`  
		Last Modified: Thu, 26 Jun 2025 08:42:35 GMT  
		Size: 974.2 KB (974222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927f3ec758e29742e7c999ad98dd80206921dfaacd901ad5845dcb2031cda04c`  
		Last Modified: Thu, 26 Jun 2025 08:42:35 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51c338a41ea99d423dd984770a1b2961733013923d88ef9c8487dbe71b53db6`  
		Last Modified: Thu, 26 Jun 2025 08:42:35 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:04bbe23facb3ca2c4a571e15bda01bf0f877d59d3b27c3095a07e13d9629325f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94fc7603e5df6be47d63f45b110d94d3d5fb2768a684d5e4300ce3fe4240da97`

```dockerfile
```

-	Layers:
	-	`sha256:8e4a210b7c1e4a94078dafd17aeea8d7e36e455a45c72480100ddf9d731304ca`  
		Last Modified: Thu, 26 Jun 2025 10:13:47 GMT  
		Size: 2.2 MB (2172162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d93a114259e1d4e445c628108c4d73d72ff7aa9a7638c8c1b5110149716aa3`  
		Last Modified: Thu, 26 Jun 2025 10:13:48 GMT  
		Size: 31.7 KB (31691 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; s390x

```console
$ docker pull composer@sha256:76586dba6bcaf104bf78a2e926157d3ecb2162db2a90333c32b021cbba2835fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77541209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffb961ffd5347aa88d54d9bdbd0dcc69ac5ff667d532b9406faf7a02c73ef0b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.10
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abd3e67b018bcd8c0aa4d0434d7ec04dcdb3a3cfbf444a313e2be49d0524ec2`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 5.9 MB (5932552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f41e4866617495859c5133b898f769b3867a6a3ae061aa9561da765981c5ad`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9335ac6e22dd0c0b2e07f4a5406c437168067a987662ebd8bcd3b269496018`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da3506587d8ded424a7c5730d972ae6f1735f6afc1a325c7e9f83474f399fde`  
		Last Modified: Thu, 03 Jul 2025 23:16:27 GMT  
		Size: 13.6 MB (13647264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671a375a1790dbb9b0d83c7dd0560e7f6e75fb5b06afbc76019557052c897e5a`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dc301a9ae8a743478269ed0a476a3abb5ea1e3f156da87ce855397d9ddef91`  
		Last Modified: Thu, 03 Jul 2025 23:16:26 GMT  
		Size: 21.5 MB (21450357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1074498264e134b44d0edcde237cf3cfadba39197115581cfd4b9a9c5ba0fa`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1658861fe310f53081a1e605b2427a938ceddc66bacb97178d77404b333d65a1`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105bedc3ea3fb0ab6591d908f480b2bb3c119411d1ba9dc0c0e9fd62b45f2a39`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb11fbf2308810b649dff18139a7f4e9d809ae768cc36f3d15ec258497a33363`  
		Last Modified: Fri, 04 Jul 2025 02:05:49 GMT  
		Size: 31.8 MB (31839057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb18554f4af212841fd6225002512ce8150b2738e7c8d62528fee75319d8df8`  
		Last Modified: Fri, 04 Jul 2025 02:05:34 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931a141d3b8edb6ab1e8e3aeb1e9a4b3a912f88003675e89dc46803a6ca8252b`  
		Last Modified: Fri, 04 Jul 2025 02:07:05 GMT  
		Size: 979.6 KB (979593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535010aa718560098f0e81a5f45d58691a627aecca27eca3da2635e48f1c76a0`  
		Last Modified: Fri, 04 Jul 2025 02:07:04 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c75f4f8a0c4c5fdb0702183067fcc807bdd1b7d933a89e4379dc62f7a607ae`  
		Last Modified: Fri, 04 Jul 2025 02:07:04 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:ed1ab93ff8d9690acbeec0b736388e307d82a0f6bd3f3bccade5eb1aad6edf31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfadad1ce6d357c73689ef92670a2f57061dcdb641b7ffc571f0540c543ec49`

```dockerfile
```

-	Layers:
	-	`sha256:28deab63effa2f8e9b986d8fa8c5b7cd8ed330836a898ecb8793003b2a076805`  
		Last Modified: Fri, 04 Jul 2025 04:14:18 GMT  
		Size: 2.2 MB (2171952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac38573486931e331c1ddd2734691ca96fd9af6c2e2a0e1a5ed3b03be09fd97c`  
		Last Modified: Fri, 04 Jul 2025 04:14:18 GMT  
		Size: 31.7 KB (31652 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8.9`

```console
$ docker pull composer@sha256:0eed6733d75c35f13c4794990f22aa04654addc135bc575cd5692572bb3c8935
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

### `composer:2.8.9` - linux; amd64

```console
$ docker pull composer@sha256:864a61db30e6203c4a20b777493bc17f9c361303fd6a5e6db2cbbd4c56d5faa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79309733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21295413e1bc8c2201f98d084a45091bf7d8ee2b6514e9bec81c411a8e172682`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.10
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b94662290ef2237915af922ad14ae2b406eccea26d9201aa949ea52f20b737f`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 5.9 MB (5944403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498a67832465ef6dae00170ccca088bdbc63d05a197e0ba1403442805169a06a`  
		Last Modified: Thu, 03 Jul 2025 23:04:16 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53785dc48fc021d1c3f9c46a776ead61a024377fb5e6ab592908501762d63a7`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c87a7802578b0a5aebb57ffea8e543a2d50cff1ec6ffb0941fe8ad61b3a9e6`  
		Last Modified: Thu, 03 Jul 2025 23:04:23 GMT  
		Size: 13.6 MB (13647262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5aa21d09531523ae5c279a8b0eb00236af3b192f428c934050c61f7e1611eaa`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fccbfd125531b00b24f5c4c9c182e17714478e55b96701b7e71d30f7f70f9b`  
		Last Modified: Thu, 03 Jul 2025 23:04:28 GMT  
		Size: 21.0 MB (20971251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481b52666b981ec99f99b98b64ef13ff6ce799950970b68817767c966318dc11`  
		Last Modified: Thu, 03 Jul 2025 23:04:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a3724a01f76e5128bdebeeb89d8f42b63b2e987403c91e1f1f5c084c63ffee`  
		Last Modified: Thu, 03 Jul 2025 23:04:22 GMT  
		Size: 20.2 KB (20205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755a5679cebfbcec196508684d58f3d3479a8923825702cea8057be9ea0509ea`  
		Last Modified: Thu, 03 Jul 2025 23:04:25 GMT  
		Size: 20.2 KB (20204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c852688dfb4eb3338fa2b359258f4def968d8542cb467086d1eeea1f28905a74`  
		Last Modified: Thu, 03 Jul 2025 23:13:02 GMT  
		Size: 33.9 MB (33928299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c622ee0a80d81cfef14283072f36dba68467de22ad3d6eb6da4af6de1560b45`  
		Last Modified: Thu, 03 Jul 2025 23:13:00 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218c0a682557e725de4b4ae1b3d83acabd53d9ce5f23a45ef3e1b3721fea1262`  
		Last Modified: Thu, 03 Jul 2025 23:13:00 GMT  
		Size: 976.4 KB (976411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cc4579c8bd93cd33c1b651f3f52e56ca67655b23b2fc99ae1954c25cfc8630`  
		Last Modified: Thu, 03 Jul 2025 23:13:01 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e141382acfb75c4a31d782c5f0837bb164ef89d645af35d1c815bcdfcf5cac`  
		Last Modified: Thu, 03 Jul 2025 23:13:00 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.9` - unknown; unknown

```console
$ docker pull composer@sha256:d4d4b49e2553833f43684f3a5905521881e8a9dfa954fc06225be2cce9d466bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbf3553c4657aa72f0ba321ebc291fa348abef46a3a72f6d93550521428759f`

```dockerfile
```

-	Layers:
	-	`sha256:3ad72884d89234dbd14e825e71a080c543f84beceb8ee170a45eb4e9be474b08`  
		Last Modified: Fri, 04 Jul 2025 01:13:40 GMT  
		Size: 2.2 MB (2175340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c65c76faf5625b204b8a6440bd9d80740b5757a5f019373204445f59774974eb`  
		Last Modified: Fri, 04 Jul 2025 01:13:41 GMT  
		Size: 31.7 KB (31652 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.9` - linux; arm variant v6

```console
$ docker pull composer@sha256:648b0bf94ac42dff7872cea189a81b4e25e8be6ae5015b1da330a9c8c31b704f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77625569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0576b47e03b1a0e8e65bd259e7af5895948140096c3afc93f9a0dab0e88a2f48`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.10
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4a1a48d371204daac6d50cf0ade3fcbe953b7326556c347d0834eeb808b22f`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 13.6 MB (13647232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7209fb73f851518e0fbc85b54004a573116286207c48ee96ab37833cb8ea1353`  
		Last Modified: Thu, 03 Jul 2025 23:00:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7698dfdb6ae14586a077f81a7e7531ba3d394ab385475ff9c6573114a36ad047`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 22.2 MB (22216193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2822e518605b3410372bbcdb567b3220dcdbe3fc3a85d76aeeed7414a97ce84`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc23f56a1dfd1eb937c6d0d63cb116029d4ac6193e3b8e0487798f7859b09cf`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb672fb64a4977b38f156870ac6fd28ad3898b39594ead2e5d7a7a25cf62e07a`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f65dda0589cf68df6c1f7a31f2ed36448fe5ac89816b32bef12a62b39575a0`  
		Last Modified: Fri, 04 Jul 2025 01:07:05 GMT  
		Size: 33.8 MB (33807127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af16e8c9f29c59fdf9ae69e6ad7a7f42c68aea017b14dcf169ea15f538efb4e`  
		Last Modified: Fri, 04 Jul 2025 01:07:01 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d70107b5aba54d8f31fb97e22d592810074a1b8f05392fc1093eb44ac667ff8`  
		Last Modified: Fri, 04 Jul 2025 01:08:05 GMT  
		Size: 976.8 KB (976765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb15dc78f78d103edcc744c17908609b087a11d0c10548c3f9d791e07ccbca86`  
		Last Modified: Wed, 25 Jun 2025 20:29:47 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224953665089fda926db4dea1b86110c646109a8a62e68cb13246f46d3d4b95e`  
		Last Modified: Fri, 04 Jul 2025 01:08:04 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.9` - unknown; unknown

```console
$ docker pull composer@sha256:cc5374cca047b9c29c17b890515ce54d573a889881ed1a840b780509ee1a35c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edcc52d9671e580042a8af83c87912d079d008f561c600822f9a3c9d52ccea5b`

```dockerfile
```

-	Layers:
	-	`sha256:70fb45703ae28fcbe74dc9795f343a8920c7c71d06a958b9c23a34a6eb3bfa5d`  
		Last Modified: Fri, 04 Jul 2025 04:13:56 GMT  
		Size: 31.5 KB (31539 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.9` - linux; arm variant v7

```console
$ docker pull composer@sha256:5c2811e58deda112f1b19ea2a429444944c8ad179727b126774b90672e8e66d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74164142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c019e9b06442cd09ddf2e4b7eb65cdab0d41f4df9e0d782fec975e072b48e76d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.10
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f4b8d7b2257f1a6ac3d6d3cc6bf9a4b64ab9fc5d2607c301f7de2c7d6c4f46`  
		Last Modified: Thu, 03 Jul 2025 23:46:20 GMT  
		Size: 13.6 MB (13647249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a41d3b4f0ee7936d37a29b00d6599e6c083cdd6c3c1e87cf67e60c78bed722f`  
		Last Modified: Thu, 03 Jul 2025 23:46:17 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f25659badae5bd6d735e7a8151332a7d70260be40b9bd15903ae5024c69186a`  
		Last Modified: Thu, 03 Jul 2025 23:46:20 GMT  
		Size: 21.0 MB (20968354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9020d050ffd80f0ec4539c880f71565ba7987609cedfc9dc9ff78af7fb53b62b`  
		Last Modified: Thu, 03 Jul 2025 23:46:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9a523c3a709bd62efada35a0a92295ac64b04640f1069b295c0d6889f2487`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210dbe376a53d9ebd8229f86a814b0d26ee3ca102f0e74c6dc09a10a9c343c58`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebcb76101e3ff8f5c34e57b65c480c0f53a9657085c1dd3571c570cc1908dec`  
		Last Modified: Fri, 04 Jul 2025 03:24:53 GMT  
		Size: 32.1 MB (32069935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7837ce17d23c46b208ed90e2deb598eb1aaed88b570cd6b34760d21674e702c`  
		Last Modified: Fri, 04 Jul 2025 03:24:49 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ad676d7ee639bd12778210b726ccd10b9eead85271834e2b2c6bf311e7240a`  
		Last Modified: Fri, 04 Jul 2025 03:26:21 GMT  
		Size: 967.1 KB (967097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3b74b2060ffea794587392d8e37fc22baa87dbd5c3bee7b016a864f1aea241`  
		Last Modified: Fri, 04 Jul 2025 03:26:20 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb4cff2df01ba4618678e4f893513145e63282a0ad4f1bffe3e362bf8706220`  
		Last Modified: Fri, 04 Jul 2025 03:26:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.9` - unknown; unknown

```console
$ docker pull composer@sha256:3578e71f433b37866bf7a4a743e8b077af4f522455beef6e247b8d02a8e137a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27499b4da1ed9b3f5ac42b35ea64b62305426f552bc2c1c6d49da8d1a84defb`

```dockerfile
```

-	Layers:
	-	`sha256:5f8a22eb1d359ca353b20fa10f9ceb96545b85653ea907d8d75b260e52891e2e`  
		Last Modified: Fri, 04 Jul 2025 04:14:00 GMT  
		Size: 2.2 MB (2175664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e26ba3a9482b3a935d3eb85feaf385751e9d4f79763ed43ff63f893b27554d5d`  
		Last Modified: Fri, 04 Jul 2025 04:14:01 GMT  
		Size: 31.8 KB (31754 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.9` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:d2dadc0c40a3554177b591599fb4d6a672330089c735772da89e0220add47f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76798022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d43140056d0abec9110d9e36cc98a921b48be8aac07425b3be37eced18794a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d74afa414d93be74315fb2fbbededff31189950343736eb9412b26b4f530d1a`  
		Last Modified: Fri, 20 Jun 2025 19:32:29 GMT  
		Size: 3.5 MB (3470712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91ea4522a211c5e50ab5b22083b52449e7ad38398a1f6e5dad24e4a62961906`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b695911010ae65b6cf4c4b5ac350b27932e3b4b29077f6094baa473db50fb5`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e2341d4b1828e7c29626f05458e9c7ac77b849f7fa211122c5e49f3db640c2`  
		Last Modified: Wed, 25 Jun 2025 19:58:30 GMT  
		Size: 13.6 MB (13640504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2214385dee2a6502125f514cfafec9ffbab10a83686ed1edebefbe13bb98e0df`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2192f9a8f7dc985e1b1534af7a423269d9525cd446882c0b66bc83bd73c1d`  
		Last Modified: Wed, 25 Jun 2025 19:58:29 GMT  
		Size: 20.5 MB (20519110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7813f4e30ce21280209e560b03ffd244261e042d03b4f926c87197d856e4d07a`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5659da52250b6def060ce2459caf69d028600439407c5609ffb01e17d290d0a`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 20.0 KB (19995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed11a0655a2eb0f0eae0b13f815d1385ec0d4bc0fc0d3e23f5c2e3aed8e1799`  
		Last Modified: Wed, 25 Jun 2025 19:58:28 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db90ec20dde1245e26657e9eeab7a68a4f381ea6442f98f105cfc54ce54e3a0b`  
		Last Modified: Thu, 26 Jun 2025 00:27:56 GMT  
		Size: 34.0 MB (34010879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb4fdb28ebd43bf90c0134d109bd7f9e79aa657ab4e9e040a42ac1d008e71aa`  
		Last Modified: Thu, 26 Jun 2025 00:27:53 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ddf66bb9ba56337081b692d4129b361f983e7f9abd1d5e349d28c1c7eade483`  
		Last Modified: Thu, 26 Jun 2025 00:28:57 GMT  
		Size: 976.0 KB (976041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b24a8ffa2909a504d9bbfc6df46cc2b56d610d921e33e9974ffc838c62bdd1d`  
		Last Modified: Thu, 26 Jun 2025 00:28:57 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821b9dea24a435946ecb336cb8278f7297bed4a94795980b99f141347beab268`  
		Last Modified: Thu, 26 Jun 2025 00:28:57 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.9` - unknown; unknown

```console
$ docker pull composer@sha256:df1144ec9680bd760c06c95a7bfff7150690d287e025712cc341c4a5ffe356df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640d11c5a6cebe938b2fd6fab0e883dbce3befa0419a62d2c446198798adf567`

```dockerfile
```

-	Layers:
	-	`sha256:a7b2a0fdfcdccff2b7138ac64502f1f2fb239077a7b59fa7e206bf3e6f124b5c`  
		Last Modified: Thu, 26 Jun 2025 01:13:48 GMT  
		Size: 2.2 MB (2175484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91b5ec1ac58d000c75aaad3474d0386b5646668bc3b2685875bd6ce02e925b2b`  
		Last Modified: Thu, 26 Jun 2025 01:13:49 GMT  
		Size: 31.8 KB (31777 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.9` - linux; 386

```console
$ docker pull composer@sha256:7ea3337a73dfe929bb2a4e849d7413a67d2f8bece13a67bb7cd0b77e112e54e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80042550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5691a9cad94ac3356a7d1f58071b048add1584758c6ed163996f041ab04e4a8d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.10
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4579a4802acae62f9995bc4ca35846cfa477f9a889ce0fb2017ac6630b78bd4a`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 5.8 MB (5806973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57074fe130dea7f1367879dc4bc435c31dce84ecd32b48ea0a63d35b4a08b836`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7e9cf52dab21b2f526412767a5e92e23eeb507ad11d31f9bf4391ad5eb6a66`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee47d22d22648a57b652a67b201fb0e169513c91be3eec67cb726ba70e375a83`  
		Last Modified: Thu, 03 Jul 2025 23:05:02 GMT  
		Size: 13.6 MB (13647238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ed9c7929ede2d39288b5cdc1a881693463f9694eab366fbb269e70c0d92a49`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63b1c24d7566d919e950b1eaf0a78b66a3bebc8b853f7dac99909776dbae0f1`  
		Last Modified: Thu, 03 Jul 2025 23:05:04 GMT  
		Size: 21.5 MB (21500663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f235298ca3bcb11577f52427a9e9abe5f5708168ce3e6f7a92e3516e12f33f6`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3069db4b5ea73d2b8c2f80770d98b1ecf8fc539f7fcb87b04c2a4d4c1d2747`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 20.2 KB (20195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af93b74a51d1b8b0d9adaa24d025147b9bbb65f3dea67b796f0959416093750`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 20.2 KB (20192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c8ee1962b1a764f17623a97c88eac6b4bcd6264d017309e15662ca58ba4328`  
		Last Modified: Thu, 03 Jul 2025 23:13:04 GMT  
		Size: 34.4 MB (34436697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62967b08a91543e22a6b21fc96ea01449936ec8716111d503430bebb27b9b1cb`  
		Last Modified: Thu, 03 Jul 2025 23:13:00 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30acb5fcf8b4c6c26895514cffa50f5f9943af2422b56fb2d081f516ceedb84a`  
		Last Modified: Thu, 03 Jul 2025 23:13:01 GMT  
		Size: 989.7 KB (989711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431bf78845ea7be375b442b6d6e0b94a886a77fe6982ccd2cae5e6fba720130b`  
		Last Modified: Thu, 03 Jul 2025 23:13:01 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44a7383365beb5c7a1faf0ae044a570043a5793a4b4007761b2d0751cd244da`  
		Last Modified: Thu, 03 Jul 2025 23:13:01 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.9` - unknown; unknown

```console
$ docker pull composer@sha256:fe8fc42c5d819f1d34f4ce945cfdf317de4a0cbb50d3aeddca71d79022c98741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b3db9f01b13546692b4ad51bad36e7e3165c293f4bf1fc24d927922991439d`

```dockerfile
```

-	Layers:
	-	`sha256:40add4385980bb9b06d7a8f0bea17a1228b127a11af5d741d0259be4e26f4bcb`  
		Last Modified: Fri, 04 Jul 2025 01:13:54 GMT  
		Size: 2.2 MB (2175123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fe1485dca730e6cd0aa0fdbb3d1bd1ee70141e35977cd5fdd159ec4fc558945`  
		Last Modified: Fri, 04 Jul 2025 01:13:55 GMT  
		Size: 31.6 KB (31616 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.9` - linux; ppc64le

```console
$ docker pull composer@sha256:78db100203a59f9ca077a0ea16741ec93e078dbb2a52df6ab977a16a05b666ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81508478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60ff07f83bdd829ca9ac347bcd7a91042f0c838a7658f717395cce85d77408c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.10
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7db3af28cc31124a8bce98c13cd1b2512963d13f437d0d67f9918df0d57d2b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 5.9 MB (5946924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ec39d79edfa484fac002ed8c640f17ae8077df4dce88811d8d186865593a6b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 939.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2995d4272705fc452f2b3ea9e2d118681efbad9f858c7743f6f69364d73a50`  
		Last Modified: Thu, 03 Jul 2025 23:15:35 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da4669ab0266f9dd895304e7c92d52e7df1b0acfdc30e6abf0d73fd20c6d09a`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 13.6 MB (13647243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdb584c1e59e66bf7047b954cfc1e41ae7df62560b963934f349b9bd0a11fed`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dff158c4fec087bdd22d80d469c14bd7f5e8a7d72d9a682db56d77c7977e55f`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 21.9 MB (21877134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa09d11c80e8896e162d36345eb3a1cf062f1ba207ed29c537b7783eb818f415`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09daff9fd7af3987bc24f46923dc89bca4e186069874ea11f88390e02dbca5a8`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1d9e25cff60aeed589359ca184c52454f63361a6309e3c363d0d97c227e006`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcefe2124ab8f2442794aaabac7f9422c8d266cee3bbfbb30c3cea3b0f0943f6`  
		Last Modified: Fri, 04 Jul 2025 02:29:48 GMT  
		Size: 35.3 MB (35279082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7315eb9406973e6ea300692e85a137454ee79d74bbb5b71ff352feab46e7c24`  
		Last Modified: Fri, 04 Jul 2025 02:29:46 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4508639e74c9c28c3fb419e0c8c6a031d7291e9393341921ee0f03bd59ecca`  
		Last Modified: Fri, 04 Jul 2025 02:32:05 GMT  
		Size: 983.0 KB (983049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bba142070b7380628289f45cb7efe63e1078c2dee92be982602232fb09fbb5`  
		Last Modified: Fri, 04 Jul 2025 02:32:04 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e42909435644cf68037aa4d86a52d59c7e2e1c9692af7fb3134a361b663960`  
		Last Modified: Fri, 04 Jul 2025 02:32:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.9` - unknown; unknown

```console
$ docker pull composer@sha256:083aa2658271704da9e81255bb7d746de750303a00e3fe499cd00ea99740da16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1895718fc0cd8fbe5ed7357dbf119863fa5506eeb3a93c2a47d7e06a9a0aa085`

```dockerfile
```

-	Layers:
	-	`sha256:0e467847564c6b363f7e9023b8c2aa5c0114ffbbeeb42e175703b015ea07f2c4`  
		Last Modified: Fri, 04 Jul 2025 04:14:10 GMT  
		Size: 2.2 MB (2173903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38a725e262847343f44ce5121a7e45c8b8f973d0ab72ad75bf55dceba889c8d3`  
		Last Modified: Fri, 04 Jul 2025 04:14:11 GMT  
		Size: 31.7 KB (31700 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.9` - linux; riscv64

```console
$ docker pull composer@sha256:e9cf69d00e0485cfc79bbd74de2fcf971c8c0625b61f55964388187353e58dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73273033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387850bcac483e7be49354dc64c55c9837cc316862477690206f7484a1a3972e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d0224769088850e26eb3ba2638a8a3febc4b65991ac8cc63dc3f29cf199070`  
		Last Modified: Wed, 11 Jun 2025 05:05:11 GMT  
		Size: 13.6 MB (13640513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a45f979f3844cfaf9ad9f1a00668b3bb56bc478c711f2d939a7dba0c2ed6e1`  
		Last Modified: Wed, 11 Jun 2025 02:39:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b864e2d5fb63463e7b594794f1b0077ef70793371e80280a29b09008bb9771a`  
		Last Modified: Wed, 11 Jun 2025 05:05:14 GMT  
		Size: 20.4 MB (20388593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91ae988832dcf22e179ec800eee279369b0d1b8a4129c2bd761a392671d8d32`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5d276f1eb8afbe6e12101788a8d8d2c68f0875a801fca945c95b68b009ee44`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033c69f0ad5808ebac07aefd6d1a9c0933c09e134334a8bd72a2f49fb7ed2297`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 20.0 KB (19999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7d4367f9b25dba1c9057a363403805d1f3ffce81d401bb89eaa3652ee82d83`  
		Last Modified: Thu, 26 Jun 2025 08:33:02 GMT  
		Size: 31.1 MB (31107678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a85da3fdbf5b1c41e6f68043dc7ff3cb2ef316082fa092b6f23657dffda19a1`  
		Last Modified: Thu, 26 Jun 2025 08:32:59 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e85546fd2798c3532f47d4372f9fad38a6865cf751f31473179d3d7f11577b`  
		Last Modified: Thu, 26 Jun 2025 08:42:35 GMT  
		Size: 974.2 KB (974222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927f3ec758e29742e7c999ad98dd80206921dfaacd901ad5845dcb2031cda04c`  
		Last Modified: Thu, 26 Jun 2025 08:42:35 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51c338a41ea99d423dd984770a1b2961733013923d88ef9c8487dbe71b53db6`  
		Last Modified: Thu, 26 Jun 2025 08:42:35 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.9` - unknown; unknown

```console
$ docker pull composer@sha256:04bbe23facb3ca2c4a571e15bda01bf0f877d59d3b27c3095a07e13d9629325f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94fc7603e5df6be47d63f45b110d94d3d5fb2768a684d5e4300ce3fe4240da97`

```dockerfile
```

-	Layers:
	-	`sha256:8e4a210b7c1e4a94078dafd17aeea8d7e36e455a45c72480100ddf9d731304ca`  
		Last Modified: Thu, 26 Jun 2025 10:13:47 GMT  
		Size: 2.2 MB (2172162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d93a114259e1d4e445c628108c4d73d72ff7aa9a7638c8c1b5110149716aa3`  
		Last Modified: Thu, 26 Jun 2025 10:13:48 GMT  
		Size: 31.7 KB (31691 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.9` - linux; s390x

```console
$ docker pull composer@sha256:76586dba6bcaf104bf78a2e926157d3ecb2162db2a90333c32b021cbba2835fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77541209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffb961ffd5347aa88d54d9bdbd0dcc69ac5ff667d532b9406faf7a02c73ef0b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.10
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abd3e67b018bcd8c0aa4d0434d7ec04dcdb3a3cfbf444a313e2be49d0524ec2`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 5.9 MB (5932552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f41e4866617495859c5133b898f769b3867a6a3ae061aa9561da765981c5ad`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9335ac6e22dd0c0b2e07f4a5406c437168067a987662ebd8bcd3b269496018`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da3506587d8ded424a7c5730d972ae6f1735f6afc1a325c7e9f83474f399fde`  
		Last Modified: Thu, 03 Jul 2025 23:16:27 GMT  
		Size: 13.6 MB (13647264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671a375a1790dbb9b0d83c7dd0560e7f6e75fb5b06afbc76019557052c897e5a`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dc301a9ae8a743478269ed0a476a3abb5ea1e3f156da87ce855397d9ddef91`  
		Last Modified: Thu, 03 Jul 2025 23:16:26 GMT  
		Size: 21.5 MB (21450357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1074498264e134b44d0edcde237cf3cfadba39197115581cfd4b9a9c5ba0fa`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1658861fe310f53081a1e605b2427a938ceddc66bacb97178d77404b333d65a1`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105bedc3ea3fb0ab6591d908f480b2bb3c119411d1ba9dc0c0e9fd62b45f2a39`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb11fbf2308810b649dff18139a7f4e9d809ae768cc36f3d15ec258497a33363`  
		Last Modified: Fri, 04 Jul 2025 02:05:49 GMT  
		Size: 31.8 MB (31839057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb18554f4af212841fd6225002512ce8150b2738e7c8d62528fee75319d8df8`  
		Last Modified: Fri, 04 Jul 2025 02:05:34 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931a141d3b8edb6ab1e8e3aeb1e9a4b3a912f88003675e89dc46803a6ca8252b`  
		Last Modified: Fri, 04 Jul 2025 02:07:05 GMT  
		Size: 979.6 KB (979593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535010aa718560098f0e81a5f45d58691a627aecca27eca3da2635e48f1c76a0`  
		Last Modified: Fri, 04 Jul 2025 02:07:04 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c75f4f8a0c4c5fdb0702183067fcc807bdd1b7d933a89e4379dc62f7a607ae`  
		Last Modified: Fri, 04 Jul 2025 02:07:04 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.9` - unknown; unknown

```console
$ docker pull composer@sha256:ed1ab93ff8d9690acbeec0b736388e307d82a0f6bd3f3bccade5eb1aad6edf31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfadad1ce6d357c73689ef92670a2f57061dcdb641b7ffc571f0540c543ec49`

```dockerfile
```

-	Layers:
	-	`sha256:28deab63effa2f8e9b986d8fa8c5b7cd8ed330836a898ecb8793003b2a076805`  
		Last Modified: Fri, 04 Jul 2025 04:14:18 GMT  
		Size: 2.2 MB (2171952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac38573486931e331c1ddd2734691ca96fd9af6c2e2a0e1a5ed3b03be09fd97c`  
		Last Modified: Fri, 04 Jul 2025 04:14:18 GMT  
		Size: 31.7 KB (31652 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:latest`

```console
$ docker pull composer@sha256:0eed6733d75c35f13c4794990f22aa04654addc135bc575cd5692572bb3c8935
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
$ docker pull composer@sha256:864a61db30e6203c4a20b777493bc17f9c361303fd6a5e6db2cbbd4c56d5faa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79309733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21295413e1bc8c2201f98d084a45091bf7d8ee2b6514e9bec81c411a8e172682`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.10
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b94662290ef2237915af922ad14ae2b406eccea26d9201aa949ea52f20b737f`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 5.9 MB (5944403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498a67832465ef6dae00170ccca088bdbc63d05a197e0ba1403442805169a06a`  
		Last Modified: Thu, 03 Jul 2025 23:04:16 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53785dc48fc021d1c3f9c46a776ead61a024377fb5e6ab592908501762d63a7`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c87a7802578b0a5aebb57ffea8e543a2d50cff1ec6ffb0941fe8ad61b3a9e6`  
		Last Modified: Thu, 03 Jul 2025 23:04:23 GMT  
		Size: 13.6 MB (13647262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5aa21d09531523ae5c279a8b0eb00236af3b192f428c934050c61f7e1611eaa`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fccbfd125531b00b24f5c4c9c182e17714478e55b96701b7e71d30f7f70f9b`  
		Last Modified: Thu, 03 Jul 2025 23:04:28 GMT  
		Size: 21.0 MB (20971251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481b52666b981ec99f99b98b64ef13ff6ce799950970b68817767c966318dc11`  
		Last Modified: Thu, 03 Jul 2025 23:04:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a3724a01f76e5128bdebeeb89d8f42b63b2e987403c91e1f1f5c084c63ffee`  
		Last Modified: Thu, 03 Jul 2025 23:04:22 GMT  
		Size: 20.2 KB (20205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755a5679cebfbcec196508684d58f3d3479a8923825702cea8057be9ea0509ea`  
		Last Modified: Thu, 03 Jul 2025 23:04:25 GMT  
		Size: 20.2 KB (20204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c852688dfb4eb3338fa2b359258f4def968d8542cb467086d1eeea1f28905a74`  
		Last Modified: Thu, 03 Jul 2025 23:13:02 GMT  
		Size: 33.9 MB (33928299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c622ee0a80d81cfef14283072f36dba68467de22ad3d6eb6da4af6de1560b45`  
		Last Modified: Thu, 03 Jul 2025 23:13:00 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218c0a682557e725de4b4ae1b3d83acabd53d9ce5f23a45ef3e1b3721fea1262`  
		Last Modified: Thu, 03 Jul 2025 23:13:00 GMT  
		Size: 976.4 KB (976411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cc4579c8bd93cd33c1b651f3f52e56ca67655b23b2fc99ae1954c25cfc8630`  
		Last Modified: Thu, 03 Jul 2025 23:13:01 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e141382acfb75c4a31d782c5f0837bb164ef89d645af35d1c815bcdfcf5cac`  
		Last Modified: Thu, 03 Jul 2025 23:13:00 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:d4d4b49e2553833f43684f3a5905521881e8a9dfa954fc06225be2cce9d466bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbf3553c4657aa72f0ba321ebc291fa348abef46a3a72f6d93550521428759f`

```dockerfile
```

-	Layers:
	-	`sha256:3ad72884d89234dbd14e825e71a080c543f84beceb8ee170a45eb4e9be474b08`  
		Last Modified: Fri, 04 Jul 2025 01:13:40 GMT  
		Size: 2.2 MB (2175340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c65c76faf5625b204b8a6440bd9d80740b5757a5f019373204445f59774974eb`  
		Last Modified: Fri, 04 Jul 2025 01:13:41 GMT  
		Size: 31.7 KB (31652 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:648b0bf94ac42dff7872cea189a81b4e25e8be6ae5015b1da330a9c8c31b704f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77625569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0576b47e03b1a0e8e65bd259e7af5895948140096c3afc93f9a0dab0e88a2f48`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.10
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4a1a48d371204daac6d50cf0ade3fcbe953b7326556c347d0834eeb808b22f`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 13.6 MB (13647232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7209fb73f851518e0fbc85b54004a573116286207c48ee96ab37833cb8ea1353`  
		Last Modified: Thu, 03 Jul 2025 23:00:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7698dfdb6ae14586a077f81a7e7531ba3d394ab385475ff9c6573114a36ad047`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 22.2 MB (22216193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2822e518605b3410372bbcdb567b3220dcdbe3fc3a85d76aeeed7414a97ce84`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc23f56a1dfd1eb937c6d0d63cb116029d4ac6193e3b8e0487798f7859b09cf`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb672fb64a4977b38f156870ac6fd28ad3898b39594ead2e5d7a7a25cf62e07a`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f65dda0589cf68df6c1f7a31f2ed36448fe5ac89816b32bef12a62b39575a0`  
		Last Modified: Fri, 04 Jul 2025 01:07:05 GMT  
		Size: 33.8 MB (33807127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af16e8c9f29c59fdf9ae69e6ad7a7f42c68aea017b14dcf169ea15f538efb4e`  
		Last Modified: Fri, 04 Jul 2025 01:07:01 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d70107b5aba54d8f31fb97e22d592810074a1b8f05392fc1093eb44ac667ff8`  
		Last Modified: Fri, 04 Jul 2025 01:08:05 GMT  
		Size: 976.8 KB (976765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb15dc78f78d103edcc744c17908609b087a11d0c10548c3f9d791e07ccbca86`  
		Last Modified: Wed, 25 Jun 2025 20:29:47 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224953665089fda926db4dea1b86110c646109a8a62e68cb13246f46d3d4b95e`  
		Last Modified: Fri, 04 Jul 2025 01:08:04 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:cc5374cca047b9c29c17b890515ce54d573a889881ed1a840b780509ee1a35c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edcc52d9671e580042a8af83c87912d079d008f561c600822f9a3c9d52ccea5b`

```dockerfile
```

-	Layers:
	-	`sha256:70fb45703ae28fcbe74dc9795f343a8920c7c71d06a958b9c23a34a6eb3bfa5d`  
		Last Modified: Fri, 04 Jul 2025 04:13:56 GMT  
		Size: 31.5 KB (31539 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:5c2811e58deda112f1b19ea2a429444944c8ad179727b126774b90672e8e66d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74164142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c019e9b06442cd09ddf2e4b7eb65cdab0d41f4df9e0d782fec975e072b48e76d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.10
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f4b8d7b2257f1a6ac3d6d3cc6bf9a4b64ab9fc5d2607c301f7de2c7d6c4f46`  
		Last Modified: Thu, 03 Jul 2025 23:46:20 GMT  
		Size: 13.6 MB (13647249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a41d3b4f0ee7936d37a29b00d6599e6c083cdd6c3c1e87cf67e60c78bed722f`  
		Last Modified: Thu, 03 Jul 2025 23:46:17 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f25659badae5bd6d735e7a8151332a7d70260be40b9bd15903ae5024c69186a`  
		Last Modified: Thu, 03 Jul 2025 23:46:20 GMT  
		Size: 21.0 MB (20968354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9020d050ffd80f0ec4539c880f71565ba7987609cedfc9dc9ff78af7fb53b62b`  
		Last Modified: Thu, 03 Jul 2025 23:46:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9a523c3a709bd62efada35a0a92295ac64b04640f1069b295c0d6889f2487`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210dbe376a53d9ebd8229f86a814b0d26ee3ca102f0e74c6dc09a10a9c343c58`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebcb76101e3ff8f5c34e57b65c480c0f53a9657085c1dd3571c570cc1908dec`  
		Last Modified: Fri, 04 Jul 2025 03:24:53 GMT  
		Size: 32.1 MB (32069935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7837ce17d23c46b208ed90e2deb598eb1aaed88b570cd6b34760d21674e702c`  
		Last Modified: Fri, 04 Jul 2025 03:24:49 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ad676d7ee639bd12778210b726ccd10b9eead85271834e2b2c6bf311e7240a`  
		Last Modified: Fri, 04 Jul 2025 03:26:21 GMT  
		Size: 967.1 KB (967097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3b74b2060ffea794587392d8e37fc22baa87dbd5c3bee7b016a864f1aea241`  
		Last Modified: Fri, 04 Jul 2025 03:26:20 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb4cff2df01ba4618678e4f893513145e63282a0ad4f1bffe3e362bf8706220`  
		Last Modified: Fri, 04 Jul 2025 03:26:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:3578e71f433b37866bf7a4a743e8b077af4f522455beef6e247b8d02a8e137a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27499b4da1ed9b3f5ac42b35ea64b62305426f552bc2c1c6d49da8d1a84defb`

```dockerfile
```

-	Layers:
	-	`sha256:5f8a22eb1d359ca353b20fa10f9ceb96545b85653ea907d8d75b260e52891e2e`  
		Last Modified: Fri, 04 Jul 2025 04:14:00 GMT  
		Size: 2.2 MB (2175664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e26ba3a9482b3a935d3eb85feaf385751e9d4f79763ed43ff63f893b27554d5d`  
		Last Modified: Fri, 04 Jul 2025 04:14:01 GMT  
		Size: 31.8 KB (31754 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:d2dadc0c40a3554177b591599fb4d6a672330089c735772da89e0220add47f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76798022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d43140056d0abec9110d9e36cc98a921b48be8aac07425b3be37eced18794a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d74afa414d93be74315fb2fbbededff31189950343736eb9412b26b4f530d1a`  
		Last Modified: Fri, 20 Jun 2025 19:32:29 GMT  
		Size: 3.5 MB (3470712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91ea4522a211c5e50ab5b22083b52449e7ad38398a1f6e5dad24e4a62961906`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b695911010ae65b6cf4c4b5ac350b27932e3b4b29077f6094baa473db50fb5`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e2341d4b1828e7c29626f05458e9c7ac77b849f7fa211122c5e49f3db640c2`  
		Last Modified: Wed, 25 Jun 2025 19:58:30 GMT  
		Size: 13.6 MB (13640504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2214385dee2a6502125f514cfafec9ffbab10a83686ed1edebefbe13bb98e0df`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2192f9a8f7dc985e1b1534af7a423269d9525cd446882c0b66bc83bd73c1d`  
		Last Modified: Wed, 25 Jun 2025 19:58:29 GMT  
		Size: 20.5 MB (20519110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7813f4e30ce21280209e560b03ffd244261e042d03b4f926c87197d856e4d07a`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5659da52250b6def060ce2459caf69d028600439407c5609ffb01e17d290d0a`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 20.0 KB (19995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed11a0655a2eb0f0eae0b13f815d1385ec0d4bc0fc0d3e23f5c2e3aed8e1799`  
		Last Modified: Wed, 25 Jun 2025 19:58:28 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db90ec20dde1245e26657e9eeab7a68a4f381ea6442f98f105cfc54ce54e3a0b`  
		Last Modified: Thu, 26 Jun 2025 00:27:56 GMT  
		Size: 34.0 MB (34010879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb4fdb28ebd43bf90c0134d109bd7f9e79aa657ab4e9e040a42ac1d008e71aa`  
		Last Modified: Thu, 26 Jun 2025 00:27:53 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ddf66bb9ba56337081b692d4129b361f983e7f9abd1d5e349d28c1c7eade483`  
		Last Modified: Thu, 26 Jun 2025 00:28:57 GMT  
		Size: 976.0 KB (976041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b24a8ffa2909a504d9bbfc6df46cc2b56d610d921e33e9974ffc838c62bdd1d`  
		Last Modified: Thu, 26 Jun 2025 00:28:57 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821b9dea24a435946ecb336cb8278f7297bed4a94795980b99f141347beab268`  
		Last Modified: Thu, 26 Jun 2025 00:28:57 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:df1144ec9680bd760c06c95a7bfff7150690d287e025712cc341c4a5ffe356df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640d11c5a6cebe938b2fd6fab0e883dbce3befa0419a62d2c446198798adf567`

```dockerfile
```

-	Layers:
	-	`sha256:a7b2a0fdfcdccff2b7138ac64502f1f2fb239077a7b59fa7e206bf3e6f124b5c`  
		Last Modified: Thu, 26 Jun 2025 01:13:48 GMT  
		Size: 2.2 MB (2175484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91b5ec1ac58d000c75aaad3474d0386b5646668bc3b2685875bd6ce02e925b2b`  
		Last Modified: Thu, 26 Jun 2025 01:13:49 GMT  
		Size: 31.8 KB (31777 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; 386

```console
$ docker pull composer@sha256:7ea3337a73dfe929bb2a4e849d7413a67d2f8bece13a67bb7cd0b77e112e54e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80042550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5691a9cad94ac3356a7d1f58071b048add1584758c6ed163996f041ab04e4a8d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.10
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4579a4802acae62f9995bc4ca35846cfa477f9a889ce0fb2017ac6630b78bd4a`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 5.8 MB (5806973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57074fe130dea7f1367879dc4bc435c31dce84ecd32b48ea0a63d35b4a08b836`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7e9cf52dab21b2f526412767a5e92e23eeb507ad11d31f9bf4391ad5eb6a66`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee47d22d22648a57b652a67b201fb0e169513c91be3eec67cb726ba70e375a83`  
		Last Modified: Thu, 03 Jul 2025 23:05:02 GMT  
		Size: 13.6 MB (13647238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ed9c7929ede2d39288b5cdc1a881693463f9694eab366fbb269e70c0d92a49`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63b1c24d7566d919e950b1eaf0a78b66a3bebc8b853f7dac99909776dbae0f1`  
		Last Modified: Thu, 03 Jul 2025 23:05:04 GMT  
		Size: 21.5 MB (21500663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f235298ca3bcb11577f52427a9e9abe5f5708168ce3e6f7a92e3516e12f33f6`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3069db4b5ea73d2b8c2f80770d98b1ecf8fc539f7fcb87b04c2a4d4c1d2747`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 20.2 KB (20195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af93b74a51d1b8b0d9adaa24d025147b9bbb65f3dea67b796f0959416093750`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 20.2 KB (20192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c8ee1962b1a764f17623a97c88eac6b4bcd6264d017309e15662ca58ba4328`  
		Last Modified: Thu, 03 Jul 2025 23:13:04 GMT  
		Size: 34.4 MB (34436697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62967b08a91543e22a6b21fc96ea01449936ec8716111d503430bebb27b9b1cb`  
		Last Modified: Thu, 03 Jul 2025 23:13:00 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30acb5fcf8b4c6c26895514cffa50f5f9943af2422b56fb2d081f516ceedb84a`  
		Last Modified: Thu, 03 Jul 2025 23:13:01 GMT  
		Size: 989.7 KB (989711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431bf78845ea7be375b442b6d6e0b94a886a77fe6982ccd2cae5e6fba720130b`  
		Last Modified: Thu, 03 Jul 2025 23:13:01 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44a7383365beb5c7a1faf0ae044a570043a5793a4b4007761b2d0751cd244da`  
		Last Modified: Thu, 03 Jul 2025 23:13:01 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:fe8fc42c5d819f1d34f4ce945cfdf317de4a0cbb50d3aeddca71d79022c98741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b3db9f01b13546692b4ad51bad36e7e3165c293f4bf1fc24d927922991439d`

```dockerfile
```

-	Layers:
	-	`sha256:40add4385980bb9b06d7a8f0bea17a1228b127a11af5d741d0259be4e26f4bcb`  
		Last Modified: Fri, 04 Jul 2025 01:13:54 GMT  
		Size: 2.2 MB (2175123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fe1485dca730e6cd0aa0fdbb3d1bd1ee70141e35977cd5fdd159ec4fc558945`  
		Last Modified: Fri, 04 Jul 2025 01:13:55 GMT  
		Size: 31.6 KB (31616 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; ppc64le

```console
$ docker pull composer@sha256:78db100203a59f9ca077a0ea16741ec93e078dbb2a52df6ab977a16a05b666ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81508478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60ff07f83bdd829ca9ac347bcd7a91042f0c838a7658f717395cce85d77408c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.10
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7db3af28cc31124a8bce98c13cd1b2512963d13f437d0d67f9918df0d57d2b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 5.9 MB (5946924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ec39d79edfa484fac002ed8c640f17ae8077df4dce88811d8d186865593a6b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 939.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2995d4272705fc452f2b3ea9e2d118681efbad9f858c7743f6f69364d73a50`  
		Last Modified: Thu, 03 Jul 2025 23:15:35 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da4669ab0266f9dd895304e7c92d52e7df1b0acfdc30e6abf0d73fd20c6d09a`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 13.6 MB (13647243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdb584c1e59e66bf7047b954cfc1e41ae7df62560b963934f349b9bd0a11fed`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dff158c4fec087bdd22d80d469c14bd7f5e8a7d72d9a682db56d77c7977e55f`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 21.9 MB (21877134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa09d11c80e8896e162d36345eb3a1cf062f1ba207ed29c537b7783eb818f415`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09daff9fd7af3987bc24f46923dc89bca4e186069874ea11f88390e02dbca5a8`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1d9e25cff60aeed589359ca184c52454f63361a6309e3c363d0d97c227e006`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcefe2124ab8f2442794aaabac7f9422c8d266cee3bbfbb30c3cea3b0f0943f6`  
		Last Modified: Fri, 04 Jul 2025 02:29:48 GMT  
		Size: 35.3 MB (35279082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7315eb9406973e6ea300692e85a137454ee79d74bbb5b71ff352feab46e7c24`  
		Last Modified: Fri, 04 Jul 2025 02:29:46 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4508639e74c9c28c3fb419e0c8c6a031d7291e9393341921ee0f03bd59ecca`  
		Last Modified: Fri, 04 Jul 2025 02:32:05 GMT  
		Size: 983.0 KB (983049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bba142070b7380628289f45cb7efe63e1078c2dee92be982602232fb09fbb5`  
		Last Modified: Fri, 04 Jul 2025 02:32:04 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e42909435644cf68037aa4d86a52d59c7e2e1c9692af7fb3134a361b663960`  
		Last Modified: Fri, 04 Jul 2025 02:32:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:083aa2658271704da9e81255bb7d746de750303a00e3fe499cd00ea99740da16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1895718fc0cd8fbe5ed7357dbf119863fa5506eeb3a93c2a47d7e06a9a0aa085`

```dockerfile
```

-	Layers:
	-	`sha256:0e467847564c6b363f7e9023b8c2aa5c0114ffbbeeb42e175703b015ea07f2c4`  
		Last Modified: Fri, 04 Jul 2025 04:14:10 GMT  
		Size: 2.2 MB (2173903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38a725e262847343f44ce5121a7e45c8b8f973d0ab72ad75bf55dceba889c8d3`  
		Last Modified: Fri, 04 Jul 2025 04:14:11 GMT  
		Size: 31.7 KB (31700 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; riscv64

```console
$ docker pull composer@sha256:e9cf69d00e0485cfc79bbd74de2fcf971c8c0625b61f55964388187353e58dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73273033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387850bcac483e7be49354dc64c55c9837cc316862477690206f7484a1a3972e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d0224769088850e26eb3ba2638a8a3febc4b65991ac8cc63dc3f29cf199070`  
		Last Modified: Wed, 11 Jun 2025 05:05:11 GMT  
		Size: 13.6 MB (13640513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a45f979f3844cfaf9ad9f1a00668b3bb56bc478c711f2d939a7dba0c2ed6e1`  
		Last Modified: Wed, 11 Jun 2025 02:39:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b864e2d5fb63463e7b594794f1b0077ef70793371e80280a29b09008bb9771a`  
		Last Modified: Wed, 11 Jun 2025 05:05:14 GMT  
		Size: 20.4 MB (20388593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91ae988832dcf22e179ec800eee279369b0d1b8a4129c2bd761a392671d8d32`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5d276f1eb8afbe6e12101788a8d8d2c68f0875a801fca945c95b68b009ee44`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033c69f0ad5808ebac07aefd6d1a9c0933c09e134334a8bd72a2f49fb7ed2297`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 20.0 KB (19999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7d4367f9b25dba1c9057a363403805d1f3ffce81d401bb89eaa3652ee82d83`  
		Last Modified: Thu, 26 Jun 2025 08:33:02 GMT  
		Size: 31.1 MB (31107678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a85da3fdbf5b1c41e6f68043dc7ff3cb2ef316082fa092b6f23657dffda19a1`  
		Last Modified: Thu, 26 Jun 2025 08:32:59 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e85546fd2798c3532f47d4372f9fad38a6865cf751f31473179d3d7f11577b`  
		Last Modified: Thu, 26 Jun 2025 08:42:35 GMT  
		Size: 974.2 KB (974222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927f3ec758e29742e7c999ad98dd80206921dfaacd901ad5845dcb2031cda04c`  
		Last Modified: Thu, 26 Jun 2025 08:42:35 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51c338a41ea99d423dd984770a1b2961733013923d88ef9c8487dbe71b53db6`  
		Last Modified: Thu, 26 Jun 2025 08:42:35 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:04bbe23facb3ca2c4a571e15bda01bf0f877d59d3b27c3095a07e13d9629325f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94fc7603e5df6be47d63f45b110d94d3d5fb2768a684d5e4300ce3fe4240da97`

```dockerfile
```

-	Layers:
	-	`sha256:8e4a210b7c1e4a94078dafd17aeea8d7e36e455a45c72480100ddf9d731304ca`  
		Last Modified: Thu, 26 Jun 2025 10:13:47 GMT  
		Size: 2.2 MB (2172162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d93a114259e1d4e445c628108c4d73d72ff7aa9a7638c8c1b5110149716aa3`  
		Last Modified: Thu, 26 Jun 2025 10:13:48 GMT  
		Size: 31.7 KB (31691 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; s390x

```console
$ docker pull composer@sha256:76586dba6bcaf104bf78a2e926157d3ecb2162db2a90333c32b021cbba2835fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77541209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffb961ffd5347aa88d54d9bdbd0dcc69ac5ff667d532b9406faf7a02c73ef0b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.10
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abd3e67b018bcd8c0aa4d0434d7ec04dcdb3a3cfbf444a313e2be49d0524ec2`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 5.9 MB (5932552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f41e4866617495859c5133b898f769b3867a6a3ae061aa9561da765981c5ad`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9335ac6e22dd0c0b2e07f4a5406c437168067a987662ebd8bcd3b269496018`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da3506587d8ded424a7c5730d972ae6f1735f6afc1a325c7e9f83474f399fde`  
		Last Modified: Thu, 03 Jul 2025 23:16:27 GMT  
		Size: 13.6 MB (13647264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671a375a1790dbb9b0d83c7dd0560e7f6e75fb5b06afbc76019557052c897e5a`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dc301a9ae8a743478269ed0a476a3abb5ea1e3f156da87ce855397d9ddef91`  
		Last Modified: Thu, 03 Jul 2025 23:16:26 GMT  
		Size: 21.5 MB (21450357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1074498264e134b44d0edcde237cf3cfadba39197115581cfd4b9a9c5ba0fa`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1658861fe310f53081a1e605b2427a938ceddc66bacb97178d77404b333d65a1`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105bedc3ea3fb0ab6591d908f480b2bb3c119411d1ba9dc0c0e9fd62b45f2a39`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb11fbf2308810b649dff18139a7f4e9d809ae768cc36f3d15ec258497a33363`  
		Last Modified: Fri, 04 Jul 2025 02:05:49 GMT  
		Size: 31.8 MB (31839057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb18554f4af212841fd6225002512ce8150b2738e7c8d62528fee75319d8df8`  
		Last Modified: Fri, 04 Jul 2025 02:05:34 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931a141d3b8edb6ab1e8e3aeb1e9a4b3a912f88003675e89dc46803a6ca8252b`  
		Last Modified: Fri, 04 Jul 2025 02:07:05 GMT  
		Size: 979.6 KB (979593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535010aa718560098f0e81a5f45d58691a627aecca27eca3da2635e48f1c76a0`  
		Last Modified: Fri, 04 Jul 2025 02:07:04 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c75f4f8a0c4c5fdb0702183067fcc807bdd1b7d933a89e4379dc62f7a607ae`  
		Last Modified: Fri, 04 Jul 2025 02:07:04 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:ed1ab93ff8d9690acbeec0b736388e307d82a0f6bd3f3bccade5eb1aad6edf31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfadad1ce6d357c73689ef92670a2f57061dcdb641b7ffc571f0540c543ec49`

```dockerfile
```

-	Layers:
	-	`sha256:28deab63effa2f8e9b986d8fa8c5b7cd8ed330836a898ecb8793003b2a076805`  
		Last Modified: Fri, 04 Jul 2025 04:14:18 GMT  
		Size: 2.2 MB (2171952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac38573486931e331c1ddd2734691ca96fd9af6c2e2a0e1a5ed3b03be09fd97c`  
		Last Modified: Fri, 04 Jul 2025 04:14:18 GMT  
		Size: 31.7 KB (31652 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:lts`

```console
$ docker pull composer@sha256:d3851732b404b46cc3079f0ba6a2f54fb112f05d652cfb88bcd329f6f1922762
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
$ docker pull composer@sha256:c55bbcc0b5116f3ada5b2b794253e8d642d534800f5d711ec781a0631a511b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79153683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bfb9c90c0dd2a8370857b01de5e68a396844fc9b3eb4036bcee5238053fcd1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b94662290ef2237915af922ad14ae2b406eccea26d9201aa949ea52f20b737f`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 5.9 MB (5944403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498a67832465ef6dae00170ccca088bdbc63d05a197e0ba1403442805169a06a`  
		Last Modified: Thu, 03 Jul 2025 23:04:16 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53785dc48fc021d1c3f9c46a776ead61a024377fb5e6ab592908501762d63a7`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c87a7802578b0a5aebb57ffea8e543a2d50cff1ec6ffb0941fe8ad61b3a9e6`  
		Last Modified: Thu, 03 Jul 2025 23:04:23 GMT  
		Size: 13.6 MB (13647262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5aa21d09531523ae5c279a8b0eb00236af3b192f428c934050c61f7e1611eaa`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fccbfd125531b00b24f5c4c9c182e17714478e55b96701b7e71d30f7f70f9b`  
		Last Modified: Thu, 03 Jul 2025 23:04:28 GMT  
		Size: 21.0 MB (20971251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481b52666b981ec99f99b98b64ef13ff6ce799950970b68817767c966318dc11`  
		Last Modified: Thu, 03 Jul 2025 23:04:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a3724a01f76e5128bdebeeb89d8f42b63b2e987403c91e1f1f5c084c63ffee`  
		Last Modified: Thu, 03 Jul 2025 23:04:22 GMT  
		Size: 20.2 KB (20205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755a5679cebfbcec196508684d58f3d3479a8923825702cea8057be9ea0509ea`  
		Last Modified: Thu, 03 Jul 2025 23:04:25 GMT  
		Size: 20.2 KB (20204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c852688dfb4eb3338fa2b359258f4def968d8542cb467086d1eeea1f28905a74`  
		Last Modified: Thu, 03 Jul 2025 23:13:02 GMT  
		Size: 33.9 MB (33928299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c622ee0a80d81cfef14283072f36dba68467de22ad3d6eb6da4af6de1560b45`  
		Last Modified: Thu, 03 Jul 2025 23:13:00 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e46b6d68b19d40cae9d582d523d29cb5445750042c67b4dcd85a60dfeed7b1d`  
		Last Modified: Thu, 03 Jul 2025 23:13:02 GMT  
		Size: 820.4 KB (820361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a977cbab4acac7e284670ad25a082da694101e85439356ae5286a8f42f5f31dc`  
		Last Modified: Thu, 03 Jul 2025 23:13:01 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86faa8ac4003596a871ab1662361aac1e1c5201c5cfc449f82586191cc1255f5`  
		Last Modified: Thu, 03 Jul 2025 23:13:01 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:c559a7d2440eea7f5c9fb090622a49108e7ce577a37fd104b2a86b33e73d37b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6da2df0aa7c1b16267d729ffc7881169798d1c7d7c0d658c344b4e2eb72c10e`

```dockerfile
```

-	Layers:
	-	`sha256:9f3f5251f9a561a4d427ff51a3736e50496fc6f56a1a01f7892baa753af2a16a`  
		Last Modified: Fri, 04 Jul 2025 01:13:55 GMT  
		Size: 2.2 MB (2175046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1f9403682c82b56933aafbf66ffbb44b9473316fa9703c0243d322d72269fab`  
		Last Modified: Fri, 04 Jul 2025 01:13:55 GMT  
		Size: 31.3 KB (31348 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v6

```console
$ docker pull composer@sha256:e2b50196a498bf516318301d17e1754812c652b1cb1b4aef8bf98a89bd1bd148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77469333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1bad0aebd938e64f2f9d6c7ccaf6c85d7415bb322ec240b81eabfeb48d741c3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4a1a48d371204daac6d50cf0ade3fcbe953b7326556c347d0834eeb808b22f`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 13.6 MB (13647232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7209fb73f851518e0fbc85b54004a573116286207c48ee96ab37833cb8ea1353`  
		Last Modified: Thu, 03 Jul 2025 23:00:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7698dfdb6ae14586a077f81a7e7531ba3d394ab385475ff9c6573114a36ad047`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 22.2 MB (22216193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2822e518605b3410372bbcdb567b3220dcdbe3fc3a85d76aeeed7414a97ce84`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc23f56a1dfd1eb937c6d0d63cb116029d4ac6193e3b8e0487798f7859b09cf`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb672fb64a4977b38f156870ac6fd28ad3898b39594ead2e5d7a7a25cf62e07a`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f65dda0589cf68df6c1f7a31f2ed36448fe5ac89816b32bef12a62b39575a0`  
		Last Modified: Fri, 04 Jul 2025 01:07:05 GMT  
		Size: 33.8 MB (33807127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af16e8c9f29c59fdf9ae69e6ad7a7f42c68aea017b14dcf169ea15f538efb4e`  
		Last Modified: Fri, 04 Jul 2025 01:07:01 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a14a438fbcc90ca30c5c0ec991fd8be0c7b0045bcb84a8024e31659a0d3b48`  
		Last Modified: Fri, 04 Jul 2025 01:07:01 GMT  
		Size: 820.5 KB (820527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b158de7fb3568a394e48de871c0ea3498efb3301159509001ed1fd223c54d4`  
		Last Modified: Wed, 25 Jun 2025 22:15:59 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae54c6b7690f712d9ed6c572e55edda2a4f98703d5ccf8231cdcc9464c367027`  
		Last Modified: Fri, 04 Jul 2025 01:07:01 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:e685378f23766e35af132e6630f24e30d2bf9d499dd7eddc7137591a01ed6753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 KB (31227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4222e1dceb530beb0faf6358b42874b5eb34aa6b58bf897d879f22afcd42c1a`

```dockerfile
```

-	Layers:
	-	`sha256:bc7ebbfd707900fd28ec922eab6305413e75e3662224a563f21ae914c3e88644`  
		Last Modified: Fri, 04 Jul 2025 01:13:59 GMT  
		Size: 31.2 KB (31227 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v7

```console
$ docker pull composer@sha256:f3949d6210c4853d4e70c327eb54d77fb4008a7d4185c65e455b4f67f54e1a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74007856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5949582ae4b3af19fee7236ce4e6124d3674852ff8d9c1d4e279b6c52aa22467`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f4b8d7b2257f1a6ac3d6d3cc6bf9a4b64ab9fc5d2607c301f7de2c7d6c4f46`  
		Last Modified: Thu, 03 Jul 2025 23:46:20 GMT  
		Size: 13.6 MB (13647249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a41d3b4f0ee7936d37a29b00d6599e6c083cdd6c3c1e87cf67e60c78bed722f`  
		Last Modified: Thu, 03 Jul 2025 23:46:17 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f25659badae5bd6d735e7a8151332a7d70260be40b9bd15903ae5024c69186a`  
		Last Modified: Thu, 03 Jul 2025 23:46:20 GMT  
		Size: 21.0 MB (20968354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9020d050ffd80f0ec4539c880f71565ba7987609cedfc9dc9ff78af7fb53b62b`  
		Last Modified: Thu, 03 Jul 2025 23:46:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9a523c3a709bd62efada35a0a92295ac64b04640f1069b295c0d6889f2487`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210dbe376a53d9ebd8229f86a814b0d26ee3ca102f0e74c6dc09a10a9c343c58`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebcb76101e3ff8f5c34e57b65c480c0f53a9657085c1dd3571c570cc1908dec`  
		Last Modified: Fri, 04 Jul 2025 03:24:53 GMT  
		Size: 32.1 MB (32069935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7837ce17d23c46b208ed90e2deb598eb1aaed88b570cd6b34760d21674e702c`  
		Last Modified: Fri, 04 Jul 2025 03:24:49 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96945c09f40b176ab77a7871c4d0245fc17200393e11f0a86cb15276ffffebe9`  
		Last Modified: Fri, 04 Jul 2025 03:24:49 GMT  
		Size: 810.8 KB (810811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9bea4b503a13b84e2efeffaf50b9aa643a7ac9bbec2d0a88af5e10a9c63041`  
		Last Modified: Fri, 04 Jul 2025 03:24:50 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aace2bbaa356b1919a453abdc3f1926c1872e041d872c73ff36900d640c8a5a2`  
		Last Modified: Fri, 04 Jul 2025 03:24:50 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:1aeece1929aa0c9636b78b6db45b66360f6661dbf8dada85537311bb2e130359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2320e765b2631037672fda62c7b5c948ece89bb914689ebade1b9ee8ea1672a8`

```dockerfile
```

-	Layers:
	-	`sha256:804e6aeffccb78ffebb3871f7fcad9d6e4d21cbf66924b669c8bbbcef3453148`  
		Last Modified: Fri, 04 Jul 2025 04:14:11 GMT  
		Size: 2.2 MB (2175362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2db0ddd6dd1e92805aebf376641b8014a696bf31cef4a90f47df81d601769657`  
		Last Modified: Fri, 04 Jul 2025 04:14:11 GMT  
		Size: 31.4 KB (31442 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:8f286e6030c88da3ebf654805893416ce91c0ff0b6c587922c758719addd7866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76642077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7fc2bfa74eb8329a653fbc48ce981ae1b47ba41c1dfbdf3bdc798f246890e0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d74afa414d93be74315fb2fbbededff31189950343736eb9412b26b4f530d1a`  
		Last Modified: Fri, 20 Jun 2025 19:32:29 GMT  
		Size: 3.5 MB (3470712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91ea4522a211c5e50ab5b22083b52449e7ad38398a1f6e5dad24e4a62961906`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b695911010ae65b6cf4c4b5ac350b27932e3b4b29077f6094baa473db50fb5`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e2341d4b1828e7c29626f05458e9c7ac77b849f7fa211122c5e49f3db640c2`  
		Last Modified: Wed, 25 Jun 2025 19:58:30 GMT  
		Size: 13.6 MB (13640504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2214385dee2a6502125f514cfafec9ffbab10a83686ed1edebefbe13bb98e0df`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2192f9a8f7dc985e1b1534af7a423269d9525cd446882c0b66bc83bd73c1d`  
		Last Modified: Wed, 25 Jun 2025 19:58:29 GMT  
		Size: 20.5 MB (20519110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7813f4e30ce21280209e560b03ffd244261e042d03b4f926c87197d856e4d07a`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5659da52250b6def060ce2459caf69d028600439407c5609ffb01e17d290d0a`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 20.0 KB (19995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed11a0655a2eb0f0eae0b13f815d1385ec0d4bc0fc0d3e23f5c2e3aed8e1799`  
		Last Modified: Wed, 25 Jun 2025 19:58:28 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db90ec20dde1245e26657e9eeab7a68a4f381ea6442f98f105cfc54ce54e3a0b`  
		Last Modified: Thu, 26 Jun 2025 00:27:56 GMT  
		Size: 34.0 MB (34010879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb4fdb28ebd43bf90c0134d109bd7f9e79aa657ab4e9e040a42ac1d008e71aa`  
		Last Modified: Thu, 26 Jun 2025 00:27:53 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6ec42a724f2aeefbcb1a20585daef187b07891cf75207c6c8db8117c63f9dc`  
		Last Modified: Thu, 26 Jun 2025 00:27:53 GMT  
		Size: 820.1 KB (820096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c471c3b23b3d1c864515b5a0b7cb90ce65eeeab79a4a63f4124a62b97d0a47`  
		Last Modified: Thu, 26 Jun 2025 00:27:54 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86049f63a03e6d1fc9d7a24051761f819a9295c93f7a01b04a0aa6399c11a3f`  
		Last Modified: Thu, 26 Jun 2025 00:27:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:cc3d9242f043df599446e6c0b5e5f1a301af00ffedac8d01124c669a5f4fbc83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7786c5b0b76b9606b04ac037989fe51ed5022aa69503163ea017ac00f4988cc7`

```dockerfile
```

-	Layers:
	-	`sha256:0a7c6843ff21da43780c0935db32f4b4a9f1781127257f6fbca18f55263c549d`  
		Last Modified: Thu, 26 Jun 2025 01:13:57 GMT  
		Size: 2.2 MB (2175178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75d88db614b9377920d6ef117f33d1dc25945865090eb46f2ebed565a1843b39`  
		Last Modified: Thu, 26 Jun 2025 01:13:58 GMT  
		Size: 31.5 KB (31461 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; 386

```console
$ docker pull composer@sha256:3549d1950413df9cf9ec5dc3cba56b8a4003b398f6aaa586dabe82fe4561687e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79886978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f414549109ad3eaf016596d8b177151fdd48b457782dd8dd896c90ef88a8d3e3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4579a4802acae62f9995bc4ca35846cfa477f9a889ce0fb2017ac6630b78bd4a`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 5.8 MB (5806973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57074fe130dea7f1367879dc4bc435c31dce84ecd32b48ea0a63d35b4a08b836`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7e9cf52dab21b2f526412767a5e92e23eeb507ad11d31f9bf4391ad5eb6a66`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee47d22d22648a57b652a67b201fb0e169513c91be3eec67cb726ba70e375a83`  
		Last Modified: Thu, 03 Jul 2025 23:05:02 GMT  
		Size: 13.6 MB (13647238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ed9c7929ede2d39288b5cdc1a881693463f9694eab366fbb269e70c0d92a49`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63b1c24d7566d919e950b1eaf0a78b66a3bebc8b853f7dac99909776dbae0f1`  
		Last Modified: Thu, 03 Jul 2025 23:05:04 GMT  
		Size: 21.5 MB (21500663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f235298ca3bcb11577f52427a9e9abe5f5708168ce3e6f7a92e3516e12f33f6`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3069db4b5ea73d2b8c2f80770d98b1ecf8fc539f7fcb87b04c2a4d4c1d2747`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 20.2 KB (20195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af93b74a51d1b8b0d9adaa24d025147b9bbb65f3dea67b796f0959416093750`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 20.2 KB (20192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8afe5fb2921fe882cd785fafb8a340bc48fa984eaeb95084167790e1303e977`  
		Last Modified: Thu, 03 Jul 2025 23:12:10 GMT  
		Size: 34.4 MB (34436630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f1c0fa4f5c61d324236c0742a29d9c95bfd3957e20bf4b0b2737ca6d553db7`  
		Last Modified: Thu, 03 Jul 2025 23:12:08 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a0f472aa74942d9a4ee3c0864e5be87ebfd153fe0626ec341f9e4bf8532dd8`  
		Last Modified: Thu, 03 Jul 2025 23:12:08 GMT  
		Size: 834.2 KB (834207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4accc71185fa51ed185fc3226e03f27c8bf432a8af67578471b49317a5d6f501`  
		Last Modified: Thu, 03 Jul 2025 23:12:07 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d8365033a3cd146c7ce81b6969d385bc6830b8b0e7b79f9b8178fe789738e0`  
		Last Modified: Thu, 03 Jul 2025 23:12:07 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:78d5e6ade889c8d8ab29ae66c8b2c10b66b6e8ff4c2d587f7b6c704c44bbf784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b7cdd657a2cd5660845907325e60ef43285c10450db487f79e4f039bec77e1`

```dockerfile
```

-	Layers:
	-	`sha256:fa6faf45644f32be1508f47e007d90b37c699e54e366da94d5110b2450da5b12`  
		Last Modified: Fri, 04 Jul 2025 01:14:11 GMT  
		Size: 2.2 MB (2174834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3844137036bf9a81ac64e5bd8df05c0abf34b7d05ae60974c75f020d99ff72e9`  
		Last Modified: Fri, 04 Jul 2025 01:14:12 GMT  
		Size: 31.3 KB (31316 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; ppc64le

```console
$ docker pull composer@sha256:cb811f7a53815aaff13d20e33272b43032a9870c7545cf239a2b7d78d015c859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81352455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70c2739af288fd915ffad2abad92a531272beeca8ee264dfc05bae5210a568f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7db3af28cc31124a8bce98c13cd1b2512963d13f437d0d67f9918df0d57d2b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 5.9 MB (5946924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ec39d79edfa484fac002ed8c640f17ae8077df4dce88811d8d186865593a6b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 939.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2995d4272705fc452f2b3ea9e2d118681efbad9f858c7743f6f69364d73a50`  
		Last Modified: Thu, 03 Jul 2025 23:15:35 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da4669ab0266f9dd895304e7c92d52e7df1b0acfdc30e6abf0d73fd20c6d09a`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 13.6 MB (13647243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdb584c1e59e66bf7047b954cfc1e41ae7df62560b963934f349b9bd0a11fed`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dff158c4fec087bdd22d80d469c14bd7f5e8a7d72d9a682db56d77c7977e55f`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 21.9 MB (21877134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa09d11c80e8896e162d36345eb3a1cf062f1ba207ed29c537b7783eb818f415`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09daff9fd7af3987bc24f46923dc89bca4e186069874ea11f88390e02dbca5a8`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1d9e25cff60aeed589359ca184c52454f63361a6309e3c363d0d97c227e006`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcefe2124ab8f2442794aaabac7f9422c8d266cee3bbfbb30c3cea3b0f0943f6`  
		Last Modified: Fri, 04 Jul 2025 02:29:48 GMT  
		Size: 35.3 MB (35279082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7315eb9406973e6ea300692e85a137454ee79d74bbb5b71ff352feab46e7c24`  
		Last Modified: Fri, 04 Jul 2025 02:29:46 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25eec6677352d68955b0c10e8094221f23fc06aef202fbc10253c6c4e08f771c`  
		Last Modified: Fri, 04 Jul 2025 02:29:46 GMT  
		Size: 827.0 KB (827027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad00320a6985a0b0a5499c7098e1eb623468009265828215ae95bfb5e45752e2`  
		Last Modified: Fri, 04 Jul 2025 02:29:46 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12ce73e32b7af06aeddeb151281962f8ffd52453e3d47450a02a290baa00a6a`  
		Last Modified: Fri, 04 Jul 2025 02:29:45 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:019b8c31fae7edd2a39df33dd433d1b9dd96ccaafb9d6241bd32758eb9bc8f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f6a30a1405b7d0430cd2b2fbe71c24ee6b41cdd1d100cd0484effeeceb427b`

```dockerfile
```

-	Layers:
	-	`sha256:5008b24787427934003444e4aa7353b81254b5e480b7e94064d7c0ef7caab0d2`  
		Last Modified: Fri, 04 Jul 2025 04:14:21 GMT  
		Size: 2.2 MB (2173603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2effc5836e4c06454a9dd7f3af58faef337b470d29c16e4837f8c37097d65c22`  
		Last Modified: Fri, 04 Jul 2025 04:14:22 GMT  
		Size: 31.4 KB (31390 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; riscv64

```console
$ docker pull composer@sha256:9860f66c267457248e2763c6a09e85eb82ceb877f6d62a9e676ba6c8ae4187ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73116976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8966d79120c2abe2947477d17e117a3104862944b5f4e13ef23367ead908a2c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d0224769088850e26eb3ba2638a8a3febc4b65991ac8cc63dc3f29cf199070`  
		Last Modified: Wed, 11 Jun 2025 05:05:11 GMT  
		Size: 13.6 MB (13640513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a45f979f3844cfaf9ad9f1a00668b3bb56bc478c711f2d939a7dba0c2ed6e1`  
		Last Modified: Wed, 11 Jun 2025 02:39:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b864e2d5fb63463e7b594794f1b0077ef70793371e80280a29b09008bb9771a`  
		Last Modified: Wed, 11 Jun 2025 05:05:14 GMT  
		Size: 20.4 MB (20388593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91ae988832dcf22e179ec800eee279369b0d1b8a4129c2bd761a392671d8d32`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5d276f1eb8afbe6e12101788a8d8d2c68f0875a801fca945c95b68b009ee44`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033c69f0ad5808ebac07aefd6d1a9c0933c09e134334a8bd72a2f49fb7ed2297`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 20.0 KB (19999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7d4367f9b25dba1c9057a363403805d1f3ffce81d401bb89eaa3652ee82d83`  
		Last Modified: Thu, 26 Jun 2025 08:33:02 GMT  
		Size: 31.1 MB (31107678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a85da3fdbf5b1c41e6f68043dc7ff3cb2ef316082fa092b6f23657dffda19a1`  
		Last Modified: Thu, 26 Jun 2025 08:32:59 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7494a442b1a2a3710ab64d55620187bf77c0d16ae5055db9f579c4613fc818`  
		Last Modified: Thu, 26 Jun 2025 08:32:59 GMT  
		Size: 818.2 KB (818166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb79f82b329094c3615c093e293350ba5ba421f1a9af75f3edfda9333a8544ce`  
		Last Modified: Thu, 26 Jun 2025 08:32:59 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9e9900ee8d756b449b4fd43c55d64c8e8395d9abf19cefb38fa404c3b7bfa2`  
		Last Modified: Thu, 26 Jun 2025 08:33:00 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:d4dcc48985653e30399123cfa46b169aa591904b480bc2df5ba88df19e87917c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4124f1fb2e0f031c7b2758e04efcd50a6e073195d783b727ba466240a5c7408e`

```dockerfile
```

-	Layers:
	-	`sha256:cc65df97003e1fdf43a52d8ff3ea55f84dfa01ea4c263ceb697e09918c64f9e7`  
		Last Modified: Thu, 26 Jun 2025 10:13:52 GMT  
		Size: 2.2 MB (2171862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f19f57694101dadef618bbb4001a3dda36cac3b1d2a49238a8e065cb866f0390`  
		Last Modified: Thu, 26 Jun 2025 10:13:52 GMT  
		Size: 31.4 KB (31381 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; s390x

```console
$ docker pull composer@sha256:bfafe9ebf051d29ab62425bddadc2d0c29cb2ad8d1ad6b9ee5292fe8ebaaf5aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77385107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e072172fb388d232784b4da30e57c08bb49213b6dbe3c7b548c142ab3229d8e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abd3e67b018bcd8c0aa4d0434d7ec04dcdb3a3cfbf444a313e2be49d0524ec2`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 5.9 MB (5932552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f41e4866617495859c5133b898f769b3867a6a3ae061aa9561da765981c5ad`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9335ac6e22dd0c0b2e07f4a5406c437168067a987662ebd8bcd3b269496018`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da3506587d8ded424a7c5730d972ae6f1735f6afc1a325c7e9f83474f399fde`  
		Last Modified: Thu, 03 Jul 2025 23:16:27 GMT  
		Size: 13.6 MB (13647264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671a375a1790dbb9b0d83c7dd0560e7f6e75fb5b06afbc76019557052c897e5a`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dc301a9ae8a743478269ed0a476a3abb5ea1e3f156da87ce855397d9ddef91`  
		Last Modified: Thu, 03 Jul 2025 23:16:26 GMT  
		Size: 21.5 MB (21450357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1074498264e134b44d0edcde237cf3cfadba39197115581cfd4b9a9c5ba0fa`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1658861fe310f53081a1e605b2427a938ceddc66bacb97178d77404b333d65a1`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105bedc3ea3fb0ab6591d908f480b2bb3c119411d1ba9dc0c0e9fd62b45f2a39`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb11fbf2308810b649dff18139a7f4e9d809ae768cc36f3d15ec258497a33363`  
		Last Modified: Fri, 04 Jul 2025 02:05:49 GMT  
		Size: 31.8 MB (31839057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb18554f4af212841fd6225002512ce8150b2738e7c8d62528fee75319d8df8`  
		Last Modified: Fri, 04 Jul 2025 02:05:34 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284f923b57510b467a904df0763fb094a786ca5d5efb9dee33c4ff2797f13c8e`  
		Last Modified: Fri, 04 Jul 2025 02:05:34 GMT  
		Size: 823.5 KB (823492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfdf27edf84b4552716698c0cd4a8bbfaf9958d22ae949cfb348d8b50039650`  
		Last Modified: Fri, 04 Jul 2025 02:05:35 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d7d8932667431a132d5dede93fa60ca30f5b39341f1d7072d41f69664e76d2`  
		Last Modified: Fri, 04 Jul 2025 02:05:35 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:fb7faf5cf8175892348a10dcccdc3788d55b475053ce50aeeb7baaee7c5cee98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7232a4fe93a4a4091b9b05b21f019324afcc9c77070a0989f74e7c2670939b4`

```dockerfile
```

-	Layers:
	-	`sha256:b4efb1ad9741df2550ba69fd17eb7147daf5a58b8466e93bdfda30213fdaa5d6`  
		Last Modified: Fri, 04 Jul 2025 04:14:28 GMT  
		Size: 2.2 MB (2171658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef5f689fa4321525c672850bf67bd7494047ab6efa85d99218ec401a6141c94`  
		Last Modified: Fri, 04 Jul 2025 04:14:29 GMT  
		Size: 31.3 KB (31348 bytes)  
		MIME: application/vnd.in-toto+json
