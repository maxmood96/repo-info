<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `composer`

-	[`composer:1`](#composer1)
-	[`composer:1.10`](#composer110)
-	[`composer:1.10.27`](#composer11027)
-	[`composer:2`](#composer2)
-	[`composer:2.2`](#composer22)
-	[`composer:2.2.24`](#composer2224)
-	[`composer:2.8`](#composer28)
-	[`composer:2.8.3`](#composer283)
-	[`composer:latest`](#composerlatest)
-	[`composer:lts`](#composerlts)

## `composer:1`

```console
$ docker pull composer@sha256:07ba70f0c0ae5c1ec693f8a2d06dbbc1e751a83aae3ada1229a4c2a731974858
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
$ docker pull composer@sha256:271c61c137814ae9dc30c52db0369fe63fe03c037b26c5ce16e806d5fce59094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74791707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3298b88edb965e9ee1c0083c52993d7fef5ba52efddbbd1c54b7e9f0dd63bc70`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4026d1cc5245f59e156bffd596323974be67dd48771842c57ace1b9fcb840`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 5.6 MB (5583566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca19f9a3dd1a82729217796a0e8ef626bd25c881db51316ae1d7b6baca3c979`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d429435d57d0d3420a2bb847cb1a04a76483e18d14ae4486b653e998810c2dc8`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22359169dee3cb23309dde8b4845f0a26d5ced82572690f0ec5de9aa5c37df6b`  
		Last Modified: Thu, 21 Nov 2024 18:00:31 GMT  
		Size: 13.6 MB (13572755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60636de7ac448f3bfc52c2d3f3fbdd7e572b65b45a980647e217005c89f46ddd`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6574e97188f3a55184dd55cbc3377b5b1826fe8ac69257fc044d8d1826cf62a`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 20.8 MB (20763608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0db01ff42c14dc52ac7bd7aad09e0a0e2b0050a0ad2796a55eb92246ce39d2`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e12f7079c7bc22fa3df852b4eebe6e7b01a834b3924a0f365f1b0f3437b7eab`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 19.7 KB (19661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68923c66655255aedb65dd09e59a37aaa412e773dfbd12c4b0b808ad5eee6f87`  
		Last Modified: Thu, 21 Nov 2024 18:10:42 GMT  
		Size: 30.4 MB (30368562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb78a38fa743ba495e6f5cc9d38bb8ccd7d84cd2115b43fc683282d9e0cf122`  
		Last Modified: Thu, 21 Nov 2024 18:10:40 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905723d4efe3958647df07867bf18f602de0ef65a0344b331ca70e5e1c11d305`  
		Last Modified: Thu, 21 Nov 2024 18:10:41 GMT  
		Size: 854.8 KB (854802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c251cb0cf2f282bf47bae3434ac36afaf46b6b4e168441d7361b7f3f76650431`  
		Last Modified: Thu, 21 Nov 2024 18:10:40 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb0c74b28b1a5cf47e26e8fec2c840aca547b64a308d1f713a87c93c3561567`  
		Last Modified: Thu, 21 Nov 2024 18:10:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:834e10e96e2c184faeac9fd6318bb4c542bbc65e735f53f1e5ec80e6414bf15c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ea0f462a32e67502f906cb5fdcbda3700837f2bf5c5001a08e662f0de542cf`

```dockerfile
```

-	Layers:
	-	`sha256:7ebc56eca022572000f8c4951b23f6a51625686b37922183512398192b60ec5d`  
		Last Modified: Thu, 21 Nov 2024 18:10:40 GMT  
		Size: 2.1 MB (2146302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ed6a13ee18a234d21ef1846067d9e94bb299f2fcab272f15fc75687f0a376d0`  
		Last Modified: Thu, 21 Nov 2024 18:10:40 GMT  
		Size: 30.7 KB (30664 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v6

```console
$ docker pull composer@sha256:d436d6a8df64d4f2d3975a371459ebf45a6b2a01ae15b63ad363dda5ac1ae094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71251046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66548c01bab1b1ef118b3f7e8815c43feb7a5a8fe6b6245f23436d1cbfe7ddf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdae56950198dea1248e6f62d7e9ef311c976d55790449240dfa46ad43351f7`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 5.2 MB (5236002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773d98c98ade13dc692eaf9700be32a03220033d99905be410eda923ce054fb9`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ae964d3deb57dca49dadfc5c487d64a372e3df3db6ef51b58087c318beb33d`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851605dfb3d928a53fef3860db97edb0f94316d382df472a9f36d31603ae85dc`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 13.6 MB (13572750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb476219577608ba4633ce4f2bf10a95d8fd1bd1bb56c2fb972587e5207cb3f`  
		Last Modified: Thu, 21 Nov 2024 17:58:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698c845cc5fd3760e20d315377bdca792a2b899c35f1288b5ddf2bf66c3e10d4`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 19.0 MB (19027128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7c3d46b7180237d2a402261f2cb181901e0149fed38e5a97d2214f64ba90ac`  
		Last Modified: Thu, 21 Nov 2024 17:58:04 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72176ade970c8f4af9d251ca5d0fc1aefd6e0fa47866d9d792bf9e85a4ac16c`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 19.4 KB (19437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487dce5effb993971148992fe8918fe413df14e91c1a17c2d7a26c254d6a7b29`  
		Last Modified: Thu, 21 Nov 2024 19:21:58 GMT  
		Size: 29.2 MB (29169296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812056dc604d2f3d588dcb3b1441239d4f3a938f21cabe40a0c26a26245a6f23`  
		Last Modified: Thu, 21 Nov 2024 19:21:57 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a0bd9e12093a9ba38738b70817db6b7187d4855220a01d4dc852c966b94a84`  
		Last Modified: Thu, 21 Nov 2024 19:22:38 GMT  
		Size: 855.0 KB (854973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed5767f74313c3e5de86f485fe9bbe739863c243e3873bfd4cd246bc2251e8f`  
		Last Modified: Thu, 14 Nov 2024 17:28:22 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a862f13a225e8dc51a6e453b4bf82929be1892d05c31143272be56474da71077`  
		Last Modified: Thu, 21 Nov 2024 19:22:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:01f1a493411308fe6b6e86513377669613599dbac58bcae9de96e139f7d0fbcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc845c14c1fc28db2c2ea5c011979005443f46c56788c3cc1abba71f384a031f`

```dockerfile
```

-	Layers:
	-	`sha256:8bb8f2588138ccd3eff9d3b85191c4ef6e977ff6bb795d411fe5fdba47718005`  
		Last Modified: Thu, 21 Nov 2024 19:22:37 GMT  
		Size: 30.5 KB (30543 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v7

```console
$ docker pull composer@sha256:514895123da8e0bfb7f864e3df3e3b7ffe6724ca7d7e4dc148001d81df2f7b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69147109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e039a5774f9a4e85c4316232efa6f899478ede7e731877afb04c223f4c8d10a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2878563f55378e5cb0d2e6fc051acec0bad59706b4c55d991502e489d45f15b9`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 4.9 MB (4894482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1da599409a1b1b855c6d69889b78470128711398dd127ceb61f803c590c9c39`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fec221aedc472ddb77d24345957296ec946aab0b124953af99b1b103ca464d6`  
		Last Modified: Tue, 12 Nov 2024 03:55:37 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46d0dd0a80f3bfa93fe376e12f14d3cf1bf7c86c9c039106b233b8584ec9aac`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 13.6 MB (13572743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d138265234b8809a223e845ff20a559fa757eebafc98f9e9bf724fe8e7dc8b6c`  
		Last Modified: Thu, 21 Nov 2024 18:28:27 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b99f01624e25d17567cb4316e05b197890eaf269e39da90cf62573fc75f8dab`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 17.9 MB (17928178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc46c2ae1e666fefa71dcffefd35978d65be61640f7a3dae1293e1c413955d01`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4995aff739b8938a9a1f51923b6e970cc4d974c131fb8f2f8be37bd64c89bf1e`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 19.5 KB (19454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8371af98339513b427681640d9952ffda9674c0a7837c1f5e1ca4b91fa04e1`  
		Last Modified: Thu, 21 Nov 2024 22:48:27 GMT  
		Size: 28.8 MB (28798173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7861e6ac85a5be9e606f1a0b1ed4b0869e26847132c16ba05c326da3b82f1fb`  
		Last Modified: Thu, 21 Nov 2024 22:48:26 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17c7640c26724864975077bf1e09f1bc144baec0963df65ea611bd0db7e7c1a`  
		Last Modified: Thu, 21 Nov 2024 22:49:43 GMT  
		Size: 833.7 KB (833728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c986168709ad21a473495a55e31d91312bc9d6e2191d5bd45a177f16e72872fa`  
		Last Modified: Thu, 21 Nov 2024 22:49:43 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e303a6405c7d0268805b35c2753d13e230ba7b71b8621e6999232cf659d5ee`  
		Last Modified: Thu, 21 Nov 2024 22:49:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:8900bb1bae91598a6abb3f9fc19778c688d2eb6c5323b75c2ee5d4623c7cc107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd33650b2a16cc0f8118ff841aac3d24129f79d478c8e054820ef4435097aeca`

```dockerfile
```

-	Layers:
	-	`sha256:bdd752f419f5d036c1eb0e27f30d8a3cc8318b10aaf178cb51b308b094f3e292`  
		Last Modified: Thu, 21 Nov 2024 22:49:42 GMT  
		Size: 2.1 MB (2146615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd8dfb138a4c035491e50f18aa124940d7cacef37e67e48c6cc9fd6fbff21d15`  
		Last Modified: Thu, 21 Nov 2024 22:49:42 GMT  
		Size: 30.8 KB (30758 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:8c09078aa0143c4c74f5e6eba17a4628e4fbc0798f1adbdca5c00399342d7e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75854450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af832822517b339994dd32d9f6bfa26b6562112cd86d8ff1686012a32cb9b468`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8484336630ebb870b45fd46b300831768da17cae91aa6a615fe97d849bf7d9`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 6.0 MB (6047382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f0bf50f7dfd6864235893d3a770f2748c511f29a319b959cd61ab88719f191`  
		Last Modified: Thu, 21 Nov 2024 18:25:40 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4094551f517548ba326fd9610784089231cb5fe7b32fb0fd484b4ef62a06ec4e`  
		Last Modified: Thu, 21 Nov 2024 18:25:40 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f3a19954028229594dc87f84401ff6bb04343f60f6850d3ffd56376584e127`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 13.6 MB (13572746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cec773ac8fce78f9e43c85101520fcc9a1dfd15d5ae6b0086a53ed446c44e83`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c49e3ab1eba1efe295397f466820586f5b4c820bf03494c07afc622cb0d4b80`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 20.4 MB (20379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f558eac651d11a18dc2c9e83c547cfe4241937c5dc84ca0e2f00d0fcc438eb`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec25731eb581dc3064873d8a03e05f5820ff6c09af884fce4b25f79b77d6f34e`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 19.4 KB (19426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7fe1a5fdee0abebec8c80d0770c46acf11edac729c491803ec919a7373c8c`  
		Last Modified: Thu, 21 Nov 2024 22:17:56 GMT  
		Size: 30.9 MB (30879490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0fda769fb77685ab9ff0bd8069d8c4670c1a85af4283162afa7524a8124d45`  
		Last Modified: Thu, 21 Nov 2024 22:17:55 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3335c5ef4a35514bfc87bb05ddcb1ee519fd4122e61a41bfb420aecd63e58cb`  
		Last Modified: Thu, 21 Nov 2024 22:18:43 GMT  
		Size: 863.8 KB (863813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca999384ec6746acf1e469fc0eb9cc73c295632ff0fa2a7afe6b13d7a4cf8b5`  
		Last Modified: Thu, 21 Nov 2024 22:18:43 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634de817593f116268a9879e4501325e7636c63b131e19d91fe1138ac601f8b1`  
		Last Modified: Thu, 21 Nov 2024 22:18:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:4088ab6830b52313a01b43473d7e5e2d74223a4ffb86cd106921fd9ba16c8728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76fb29bd68f438752d253299e46b00a9f9715c12f8c6c36275528069c829ee2f`

```dockerfile
```

-	Layers:
	-	`sha256:bc5c192a57b0d7463da5c5473331e02fa2bae181f22c0745ca80087ac46d8d22`  
		Last Modified: Thu, 21 Nov 2024 22:18:43 GMT  
		Size: 2.1 MB (2146441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d23d5bec7081b2a11ff5a69dade36678b164e78c62346441da13b5ce29d06f0`  
		Last Modified: Thu, 21 Nov 2024 22:18:43 GMT  
		Size: 30.8 KB (30786 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; 386

```console
$ docker pull composer@sha256:26557f734cc9f2b8898c23790680839103ec3a9e98c6314d1bd02d85baba01e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (55956701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e9ee8039d45aa15aaec585ccbc49c883cb228759f3f79564f825bf00fbaa50`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e11d2a2a48dac61e9ac66af5a5b296591c6a200cf9944fd4df55e48749cce57`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 5.5 MB (5468335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3858fed08c63431ed26286b0317883b23277e3ce014a38a3ca7392c05f0e669a`  
		Last Modified: Thu, 21 Nov 2024 18:00:49 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d4c27ab44c7e13de299ad07b09e18b7c98dee3c34fbee400448997573becdb`  
		Last Modified: Thu, 21 Nov 2024 18:00:49 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b25b38e344c1ca4be9ca4235d6cde628e170971af37a03e30f897cf5a758c`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 13.6 MB (13572753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1764d36b8a53c825b53731114444100b7e1bf8a517ab182b4dab438333bee585`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6444425964f24bb27686445f1e394678dae6d912247a4b8f26e4d7b57e90f54`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 21.3 MB (21300265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2465ec415dcb964fc8b6deb3edeeddfb60a77336ebafdeeff9780a230562a2`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b021291a02d8b49460ff1ff13393725cf6e1616dbb1b2a1ef9c7a69fdeab5b4`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 19.6 KB (19644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b1bc8fa7da4b6087462666fa266fcabca74d746c2d07ee57a21670a552b92f`  
		Last Modified: Thu, 21 Nov 2024 19:31:15 GMT  
		Size: 11.3 MB (11281344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aafffe5ec1d54ba87a86bf601eb7f84880e74c50040c43638027881aaeca84`  
		Last Modified: Thu, 21 Nov 2024 19:31:15 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb76b7393013da6f7706b7b520b04826cf2d79befa4a047b929772130690e69e`  
		Last Modified: Thu, 21 Nov 2024 19:31:15 GMT  
		Size: 840.3 KB (840284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2453a27148d2afe3b36a639140a4e7fecf776c29bfe59e96838ab091c98e744`  
		Last Modified: Thu, 21 Nov 2024 19:31:15 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52942540edf0e81f0e5b34b27fe7d54df44188c6c0fc472f4a87b6f07fe7e584`  
		Last Modified: Thu, 21 Nov 2024 19:31:16 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:858132f021f1dec88a334ddc42238ad7f185e6ab66af68fff03c4ff543b1cb6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.6 KB (450608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c017cd16f8a0aeb7afbca5190fbc71427d6b7b31c4e9dbc8a4adec733a99f14b`

```dockerfile
```

-	Layers:
	-	`sha256:e58d9c79a82c41c17b6949b43650e2a5a10af472103cd0801753531ea4603dd5`  
		Last Modified: Thu, 21 Nov 2024 19:31:15 GMT  
		Size: 420.0 KB (419976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c14d62a1e3af4fc70cf8a1e0b343005b419033d0a6c67a483b4658b4fae62549`  
		Last Modified: Thu, 21 Nov 2024 19:31:15 GMT  
		Size: 30.6 KB (30632 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; ppc64le

```console
$ docker pull composer@sha256:6471c3128b50189fa0684e11f5ba9dde0cf5be76435d6955c8729dcfce177069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76730823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f2f1602dd4a116d4de2a3914d4549eaae1cebc3cc86b39c36a2303db5e8a9a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2473147d3bc2923a26c8ba560c425ef2674fbae2edbc29833bb5790c2c94db2`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 5.6 MB (5572572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53975073457162c05af82756884811d86cf52d05953b0589749a216a80864431`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58037573bd03f9687676a3398cb715ac628a3bc280f63aa990e8171ef59ce1c9`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f80183c138cedf9dc24420caf7f9769369bf61c8db0eb09729c4303c31ba1b`  
		Last Modified: Thu, 21 Nov 2024 18:14:28 GMT  
		Size: 13.6 MB (13572757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1746563bd5a8883ee2e1758e12423a999df46412bbeb663f9f774dc595e96ed`  
		Last Modified: Thu, 21 Nov 2024 18:14:27 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3428ebe5f2568169c292765c92b0cc55c0ef85fc46ab1c4d0b60b2d86970b4b3`  
		Last Modified: Thu, 21 Nov 2024 18:14:29 GMT  
		Size: 21.7 MB (21712721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f8424c24e908ec0192f8ff40322e44264734608539de7427be91c3398884dc`  
		Last Modified: Thu, 21 Nov 2024 18:14:27 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef3b5629726f19111a47ee6dc86f22265d0002270ef68da5bb572a2fa8a6d04`  
		Last Modified: Thu, 21 Nov 2024 18:14:28 GMT  
		Size: 19.4 KB (19424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf7d67a2a72f10bea3ee74b2250affb6d2de6aac3751149e9003e6b4ff24a2e`  
		Last Modified: Thu, 21 Nov 2024 21:22:37 GMT  
		Size: 31.4 MB (31402451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011cd0419150962df2f83f6c5e96043ca7df1ddb5a812e226d6f2b98814c7fc0`  
		Last Modified: Thu, 21 Nov 2024 21:22:35 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff276f1507c273d3ac8e2f1347db08fa9f3a7446e1208315cc4a7dd40c9366f8`  
		Last Modified: Thu, 21 Nov 2024 21:23:38 GMT  
		Size: 873.6 KB (873567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a783a497ac98b52f6ba3fab1e879d47fc1c667b088a53d1e1c55ec0b801d7a`  
		Last Modified: Thu, 21 Nov 2024 21:23:38 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575b447e5395cb0169ef16815a1e03559492888b43ee8a46e52dd46d3c589503`  
		Last Modified: Thu, 21 Nov 2024 21:23:38 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:d577c45086565b8c546d0b88c59f6921da8cd5ed17132111a8e7e657c7e98c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2175557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84791cd025a60cebd27ecd9f8f5ec55ee96983d807373839f865602bc99bc043`

```dockerfile
```

-	Layers:
	-	`sha256:9703b93fd237691d1ea4841d323889d2a0c276a3bca97030a550e92f98a683c0`  
		Last Modified: Thu, 21 Nov 2024 21:23:38 GMT  
		Size: 2.1 MB (2144851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04775ba402f4f95f561c4a738ad64290a56acf5ad60d48e028bc05677f3fe017`  
		Last Modified: Thu, 21 Nov 2024 21:23:38 GMT  
		Size: 30.7 KB (30706 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; riscv64

```console
$ docker pull composer@sha256:1b87bd93805801aedd14a04369e29ba8270da7b70c92d2dbe26ecb5954635291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69748763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00729bca6163735bda0cc3607242b21ea01432fbb50fb6ac63615abd1eea7615`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
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
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8ca85c9d20c6f76d0a8087ac3a4ddd6a1e40652d189dc8dad7ca6b0737c4b0`  
		Last Modified: Tue, 12 Nov 2024 06:14:49 GMT  
		Size: 5.4 MB (5382174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d2dfe107b4bddcc389bedcee9ca3fc81f02dc0799e313c21f307ddb454b4dc`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df7310166e795cb48e721a885b92af688db981613ad6597943011293aca738c`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626cc5aa152e22cd453ede74c922b963a3bc8a4bcf66d8a4763c977a36db9bbf`  
		Last Modified: Tue, 12 Nov 2024 11:38:11 GMT  
		Size: 12.5 MB (12504597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e68d6f9ff3ad2f5f92d5d2e1da7c8e8e8c7acf26714c65fb1634379b0ceabea`  
		Last Modified: Tue, 12 Nov 2024 11:38:08 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7ef4ac959dd31d8a66fcf270291f1312424b277d8adec2eded58a835d3130c`  
		Last Modified: Tue, 12 Nov 2024 11:38:11 GMT  
		Size: 16.8 MB (16791439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f9910ad73e6186422edca968a56743133f52309ae7e8fbfaeba5689ec14ce1`  
		Last Modified: Tue, 12 Nov 2024 11:38:08 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cccb83ba6c8bd3926d00dba2c6475d1639c61ec7b4dc48a094f44e9ef2d363f`  
		Last Modified: Tue, 12 Nov 2024 11:38:10 GMT  
		Size: 19.4 KB (19444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1184794faa4cb72388841b6ca5edd801726298f1bc7a901384a6611a072b84d`  
		Last Modified: Wed, 13 Nov 2024 13:17:47 GMT  
		Size: 30.8 MB (30811150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0835e0d761497dfe92dfd2f01937792ca5c678bba375a232324b9fbb0ba5120`  
		Last Modified: Wed, 13 Nov 2024 13:17:42 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def70436aad825b91c93f68e6cd9319acc47844dd03907e4b3f58fd57ed6fb74`  
		Last Modified: Thu, 14 Nov 2024 17:36:28 GMT  
		Size: 863.6 KB (863606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8833f40640acdf41afe00d9e8ec372094a3162b1f5e9a2eee402b886fd020d26`  
		Last Modified: Thu, 14 Nov 2024 17:36:28 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d623967f7eb7838edfd7d9aba19dc57c5f949bb72f6a819cb1fbd7ac74bf618e`  
		Last Modified: Thu, 14 Nov 2024 17:36:28 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:c21c2a3cced01019307214354233618d4716e9211c62d1862ada2734b2ebd6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2175183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f730e9238a7e14feb8548bedb11b7840f35b70218e1751440d9d1083d2d88b11`

```dockerfile
```

-	Layers:
	-	`sha256:1b678c2f08fb3128c3ebca438809479b25ef7fc75678086e49859c98bf31b6e3`  
		Last Modified: Thu, 14 Nov 2024 17:36:28 GMT  
		Size: 2.1 MB (2144468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7574c9ca63cd3b5b86dc11bd65d12591c592c14480a000581566e7013419689c`  
		Last Modified: Thu, 14 Nov 2024 17:36:28 GMT  
		Size: 30.7 KB (30715 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; s390x

```console
$ docker pull composer@sha256:c05f08b3551475a37a9c85853c3c189b9779f5d0476e596bfbf6ca0a83ecd699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76051227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9836f25e54ec98e36c87729fed3064714b271c72cee9c557d81b2e652e9a12`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26915a92034b18e2de9232a415d1ad92dc1c7a9f9e2b5bb9c590ce4c503ab73e`  
		Last Modified: Tue, 12 Nov 2024 03:39:27 GMT  
		Size: 5.5 MB (5532119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4041b6d620078267a8ee6dd6b9c31735d82dee5f22aa96467865a8134d616c`  
		Last Modified: Tue, 12 Nov 2024 03:39:26 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5555efb309fc5275c2fd44eabaaf4ca859f01b510ef24cbad6009d7ed6dc4696`  
		Last Modified: Tue, 12 Nov 2024 03:39:26 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ebcb70bd65f646a0a9f4f475ec50ab3b189c26c5453f7261bc927c566c16f4`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 13.6 MB (13572754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1fe669f736130225879d8f3a94b1a2dc84c8a542232c1010d5c0efdfb490ab`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ebb202afe7221a69abb8b0e5dd9a734085f863f2a450dd0794f4e1c6bc5189`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 21.3 MB (21250100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7a60154e6bcac48ec5bae22b14f7b46c6200a532944883ccb70d97a5f9ff15`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76035e400728cb3a6c7bd01204127072929a705a4be9f5ab31588ec5dce5bd70`  
		Last Modified: Thu, 21 Nov 2024 18:24:27 GMT  
		Size: 19.4 KB (19435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391e13c55cb9dd9b3adaa2c815b5a344bfd110a0afc12b82e71ba8af9327a7a3`  
		Last Modified: Thu, 21 Nov 2024 21:24:03 GMT  
		Size: 31.3 MB (31338617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d1aea81c97d878724863520afce631476bbf2f86f4eaf2a4b781b5d4f855ba`  
		Last Modified: Thu, 21 Nov 2024 21:24:02 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b7be21a6dd37e02c120d709b9d0bb379b04287af4d63cbcd8c8fb5f2c18b4e`  
		Last Modified: Thu, 21 Nov 2024 21:24:57 GMT  
		Size: 871.7 KB (871735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda851f9276d2b6e87f74a89ad041fff1d95d8c68662512cbcabe416d9541cc9`  
		Last Modified: Thu, 21 Nov 2024 21:24:57 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4439b65fae976103d9df04da80b1c25779e74128097f8581fa46d47fccb2ea2`  
		Last Modified: Thu, 21 Nov 2024 21:24:52 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:3f04c199b7ba482fb2fa4107a95a5393e8e9df001d691631faed57bcddf9b7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2174917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca358a0f39ac9866f37e5c8b7451afe7c8bf7a637840a7f941c91e9209c3e9a0`

```dockerfile
```

-	Layers:
	-	`sha256:22bf62761c035de19bac7e81a734db5d49aba267cdc0b4abe515a621ca906fac`  
		Last Modified: Thu, 21 Nov 2024 21:24:57 GMT  
		Size: 2.1 MB (2144253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:986552d0afe5bdcf0fd315f09a2692cef9f7398406690e5e64a8f7df76e8185b`  
		Last Modified: Thu, 21 Nov 2024 21:24:57 GMT  
		Size: 30.7 KB (30664 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10`

```console
$ docker pull composer@sha256:07ba70f0c0ae5c1ec693f8a2d06dbbc1e751a83aae3ada1229a4c2a731974858
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
$ docker pull composer@sha256:271c61c137814ae9dc30c52db0369fe63fe03c037b26c5ce16e806d5fce59094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74791707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3298b88edb965e9ee1c0083c52993d7fef5ba52efddbbd1c54b7e9f0dd63bc70`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4026d1cc5245f59e156bffd596323974be67dd48771842c57ace1b9fcb840`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 5.6 MB (5583566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca19f9a3dd1a82729217796a0e8ef626bd25c881db51316ae1d7b6baca3c979`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d429435d57d0d3420a2bb847cb1a04a76483e18d14ae4486b653e998810c2dc8`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22359169dee3cb23309dde8b4845f0a26d5ced82572690f0ec5de9aa5c37df6b`  
		Last Modified: Thu, 21 Nov 2024 18:00:31 GMT  
		Size: 13.6 MB (13572755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60636de7ac448f3bfc52c2d3f3fbdd7e572b65b45a980647e217005c89f46ddd`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6574e97188f3a55184dd55cbc3377b5b1826fe8ac69257fc044d8d1826cf62a`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 20.8 MB (20763608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0db01ff42c14dc52ac7bd7aad09e0a0e2b0050a0ad2796a55eb92246ce39d2`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e12f7079c7bc22fa3df852b4eebe6e7b01a834b3924a0f365f1b0f3437b7eab`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 19.7 KB (19661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68923c66655255aedb65dd09e59a37aaa412e773dfbd12c4b0b808ad5eee6f87`  
		Last Modified: Thu, 21 Nov 2024 18:10:42 GMT  
		Size: 30.4 MB (30368562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb78a38fa743ba495e6f5cc9d38bb8ccd7d84cd2115b43fc683282d9e0cf122`  
		Last Modified: Thu, 21 Nov 2024 18:10:40 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905723d4efe3958647df07867bf18f602de0ef65a0344b331ca70e5e1c11d305`  
		Last Modified: Thu, 21 Nov 2024 18:10:41 GMT  
		Size: 854.8 KB (854802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c251cb0cf2f282bf47bae3434ac36afaf46b6b4e168441d7361b7f3f76650431`  
		Last Modified: Thu, 21 Nov 2024 18:10:40 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb0c74b28b1a5cf47e26e8fec2c840aca547b64a308d1f713a87c93c3561567`  
		Last Modified: Thu, 21 Nov 2024 18:10:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:834e10e96e2c184faeac9fd6318bb4c542bbc65e735f53f1e5ec80e6414bf15c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ea0f462a32e67502f906cb5fdcbda3700837f2bf5c5001a08e662f0de542cf`

```dockerfile
```

-	Layers:
	-	`sha256:7ebc56eca022572000f8c4951b23f6a51625686b37922183512398192b60ec5d`  
		Last Modified: Thu, 21 Nov 2024 18:10:40 GMT  
		Size: 2.1 MB (2146302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ed6a13ee18a234d21ef1846067d9e94bb299f2fcab272f15fc75687f0a376d0`  
		Last Modified: Thu, 21 Nov 2024 18:10:40 GMT  
		Size: 30.7 KB (30664 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v6

```console
$ docker pull composer@sha256:d436d6a8df64d4f2d3975a371459ebf45a6b2a01ae15b63ad363dda5ac1ae094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71251046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66548c01bab1b1ef118b3f7e8815c43feb7a5a8fe6b6245f23436d1cbfe7ddf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdae56950198dea1248e6f62d7e9ef311c976d55790449240dfa46ad43351f7`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 5.2 MB (5236002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773d98c98ade13dc692eaf9700be32a03220033d99905be410eda923ce054fb9`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ae964d3deb57dca49dadfc5c487d64a372e3df3db6ef51b58087c318beb33d`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851605dfb3d928a53fef3860db97edb0f94316d382df472a9f36d31603ae85dc`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 13.6 MB (13572750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb476219577608ba4633ce4f2bf10a95d8fd1bd1bb56c2fb972587e5207cb3f`  
		Last Modified: Thu, 21 Nov 2024 17:58:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698c845cc5fd3760e20d315377bdca792a2b899c35f1288b5ddf2bf66c3e10d4`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 19.0 MB (19027128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7c3d46b7180237d2a402261f2cb181901e0149fed38e5a97d2214f64ba90ac`  
		Last Modified: Thu, 21 Nov 2024 17:58:04 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72176ade970c8f4af9d251ca5d0fc1aefd6e0fa47866d9d792bf9e85a4ac16c`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 19.4 KB (19437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487dce5effb993971148992fe8918fe413df14e91c1a17c2d7a26c254d6a7b29`  
		Last Modified: Thu, 21 Nov 2024 19:21:58 GMT  
		Size: 29.2 MB (29169296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812056dc604d2f3d588dcb3b1441239d4f3a938f21cabe40a0c26a26245a6f23`  
		Last Modified: Thu, 21 Nov 2024 19:21:57 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a0bd9e12093a9ba38738b70817db6b7187d4855220a01d4dc852c966b94a84`  
		Last Modified: Thu, 21 Nov 2024 19:22:38 GMT  
		Size: 855.0 KB (854973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed5767f74313c3e5de86f485fe9bbe739863c243e3873bfd4cd246bc2251e8f`  
		Last Modified: Thu, 14 Nov 2024 17:28:22 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a862f13a225e8dc51a6e453b4bf82929be1892d05c31143272be56474da71077`  
		Last Modified: Thu, 21 Nov 2024 19:22:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:01f1a493411308fe6b6e86513377669613599dbac58bcae9de96e139f7d0fbcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc845c14c1fc28db2c2ea5c011979005443f46c56788c3cc1abba71f384a031f`

```dockerfile
```

-	Layers:
	-	`sha256:8bb8f2588138ccd3eff9d3b85191c4ef6e977ff6bb795d411fe5fdba47718005`  
		Last Modified: Thu, 21 Nov 2024 19:22:37 GMT  
		Size: 30.5 KB (30543 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v7

```console
$ docker pull composer@sha256:514895123da8e0bfb7f864e3df3e3b7ffe6724ca7d7e4dc148001d81df2f7b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69147109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e039a5774f9a4e85c4316232efa6f899478ede7e731877afb04c223f4c8d10a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2878563f55378e5cb0d2e6fc051acec0bad59706b4c55d991502e489d45f15b9`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 4.9 MB (4894482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1da599409a1b1b855c6d69889b78470128711398dd127ceb61f803c590c9c39`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fec221aedc472ddb77d24345957296ec946aab0b124953af99b1b103ca464d6`  
		Last Modified: Tue, 12 Nov 2024 03:55:37 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46d0dd0a80f3bfa93fe376e12f14d3cf1bf7c86c9c039106b233b8584ec9aac`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 13.6 MB (13572743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d138265234b8809a223e845ff20a559fa757eebafc98f9e9bf724fe8e7dc8b6c`  
		Last Modified: Thu, 21 Nov 2024 18:28:27 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b99f01624e25d17567cb4316e05b197890eaf269e39da90cf62573fc75f8dab`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 17.9 MB (17928178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc46c2ae1e666fefa71dcffefd35978d65be61640f7a3dae1293e1c413955d01`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4995aff739b8938a9a1f51923b6e970cc4d974c131fb8f2f8be37bd64c89bf1e`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 19.5 KB (19454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8371af98339513b427681640d9952ffda9674c0a7837c1f5e1ca4b91fa04e1`  
		Last Modified: Thu, 21 Nov 2024 22:48:27 GMT  
		Size: 28.8 MB (28798173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7861e6ac85a5be9e606f1a0b1ed4b0869e26847132c16ba05c326da3b82f1fb`  
		Last Modified: Thu, 21 Nov 2024 22:48:26 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17c7640c26724864975077bf1e09f1bc144baec0963df65ea611bd0db7e7c1a`  
		Last Modified: Thu, 21 Nov 2024 22:49:43 GMT  
		Size: 833.7 KB (833728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c986168709ad21a473495a55e31d91312bc9d6e2191d5bd45a177f16e72872fa`  
		Last Modified: Thu, 21 Nov 2024 22:49:43 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e303a6405c7d0268805b35c2753d13e230ba7b71b8621e6999232cf659d5ee`  
		Last Modified: Thu, 21 Nov 2024 22:49:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:8900bb1bae91598a6abb3f9fc19778c688d2eb6c5323b75c2ee5d4623c7cc107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd33650b2a16cc0f8118ff841aac3d24129f79d478c8e054820ef4435097aeca`

```dockerfile
```

-	Layers:
	-	`sha256:bdd752f419f5d036c1eb0e27f30d8a3cc8318b10aaf178cb51b308b094f3e292`  
		Last Modified: Thu, 21 Nov 2024 22:49:42 GMT  
		Size: 2.1 MB (2146615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd8dfb138a4c035491e50f18aa124940d7cacef37e67e48c6cc9fd6fbff21d15`  
		Last Modified: Thu, 21 Nov 2024 22:49:42 GMT  
		Size: 30.8 KB (30758 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:8c09078aa0143c4c74f5e6eba17a4628e4fbc0798f1adbdca5c00399342d7e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75854450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af832822517b339994dd32d9f6bfa26b6562112cd86d8ff1686012a32cb9b468`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8484336630ebb870b45fd46b300831768da17cae91aa6a615fe97d849bf7d9`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 6.0 MB (6047382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f0bf50f7dfd6864235893d3a770f2748c511f29a319b959cd61ab88719f191`  
		Last Modified: Thu, 21 Nov 2024 18:25:40 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4094551f517548ba326fd9610784089231cb5fe7b32fb0fd484b4ef62a06ec4e`  
		Last Modified: Thu, 21 Nov 2024 18:25:40 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f3a19954028229594dc87f84401ff6bb04343f60f6850d3ffd56376584e127`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 13.6 MB (13572746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cec773ac8fce78f9e43c85101520fcc9a1dfd15d5ae6b0086a53ed446c44e83`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c49e3ab1eba1efe295397f466820586f5b4c820bf03494c07afc622cb0d4b80`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 20.4 MB (20379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f558eac651d11a18dc2c9e83c547cfe4241937c5dc84ca0e2f00d0fcc438eb`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec25731eb581dc3064873d8a03e05f5820ff6c09af884fce4b25f79b77d6f34e`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 19.4 KB (19426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7fe1a5fdee0abebec8c80d0770c46acf11edac729c491803ec919a7373c8c`  
		Last Modified: Thu, 21 Nov 2024 22:17:56 GMT  
		Size: 30.9 MB (30879490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0fda769fb77685ab9ff0bd8069d8c4670c1a85af4283162afa7524a8124d45`  
		Last Modified: Thu, 21 Nov 2024 22:17:55 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3335c5ef4a35514bfc87bb05ddcb1ee519fd4122e61a41bfb420aecd63e58cb`  
		Last Modified: Thu, 21 Nov 2024 22:18:43 GMT  
		Size: 863.8 KB (863813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca999384ec6746acf1e469fc0eb9cc73c295632ff0fa2a7afe6b13d7a4cf8b5`  
		Last Modified: Thu, 21 Nov 2024 22:18:43 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634de817593f116268a9879e4501325e7636c63b131e19d91fe1138ac601f8b1`  
		Last Modified: Thu, 21 Nov 2024 22:18:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:4088ab6830b52313a01b43473d7e5e2d74223a4ffb86cd106921fd9ba16c8728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76fb29bd68f438752d253299e46b00a9f9715c12f8c6c36275528069c829ee2f`

```dockerfile
```

-	Layers:
	-	`sha256:bc5c192a57b0d7463da5c5473331e02fa2bae181f22c0745ca80087ac46d8d22`  
		Last Modified: Thu, 21 Nov 2024 22:18:43 GMT  
		Size: 2.1 MB (2146441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d23d5bec7081b2a11ff5a69dade36678b164e78c62346441da13b5ce29d06f0`  
		Last Modified: Thu, 21 Nov 2024 22:18:43 GMT  
		Size: 30.8 KB (30786 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; 386

```console
$ docker pull composer@sha256:26557f734cc9f2b8898c23790680839103ec3a9e98c6314d1bd02d85baba01e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (55956701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e9ee8039d45aa15aaec585ccbc49c883cb228759f3f79564f825bf00fbaa50`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e11d2a2a48dac61e9ac66af5a5b296591c6a200cf9944fd4df55e48749cce57`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 5.5 MB (5468335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3858fed08c63431ed26286b0317883b23277e3ce014a38a3ca7392c05f0e669a`  
		Last Modified: Thu, 21 Nov 2024 18:00:49 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d4c27ab44c7e13de299ad07b09e18b7c98dee3c34fbee400448997573becdb`  
		Last Modified: Thu, 21 Nov 2024 18:00:49 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b25b38e344c1ca4be9ca4235d6cde628e170971af37a03e30f897cf5a758c`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 13.6 MB (13572753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1764d36b8a53c825b53731114444100b7e1bf8a517ab182b4dab438333bee585`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6444425964f24bb27686445f1e394678dae6d912247a4b8f26e4d7b57e90f54`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 21.3 MB (21300265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2465ec415dcb964fc8b6deb3edeeddfb60a77336ebafdeeff9780a230562a2`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b021291a02d8b49460ff1ff13393725cf6e1616dbb1b2a1ef9c7a69fdeab5b4`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 19.6 KB (19644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b1bc8fa7da4b6087462666fa266fcabca74d746c2d07ee57a21670a552b92f`  
		Last Modified: Thu, 21 Nov 2024 19:31:15 GMT  
		Size: 11.3 MB (11281344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aafffe5ec1d54ba87a86bf601eb7f84880e74c50040c43638027881aaeca84`  
		Last Modified: Thu, 21 Nov 2024 19:31:15 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb76b7393013da6f7706b7b520b04826cf2d79befa4a047b929772130690e69e`  
		Last Modified: Thu, 21 Nov 2024 19:31:15 GMT  
		Size: 840.3 KB (840284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2453a27148d2afe3b36a639140a4e7fecf776c29bfe59e96838ab091c98e744`  
		Last Modified: Thu, 21 Nov 2024 19:31:15 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52942540edf0e81f0e5b34b27fe7d54df44188c6c0fc472f4a87b6f07fe7e584`  
		Last Modified: Thu, 21 Nov 2024 19:31:16 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:858132f021f1dec88a334ddc42238ad7f185e6ab66af68fff03c4ff543b1cb6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.6 KB (450608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c017cd16f8a0aeb7afbca5190fbc71427d6b7b31c4e9dbc8a4adec733a99f14b`

```dockerfile
```

-	Layers:
	-	`sha256:e58d9c79a82c41c17b6949b43650e2a5a10af472103cd0801753531ea4603dd5`  
		Last Modified: Thu, 21 Nov 2024 19:31:15 GMT  
		Size: 420.0 KB (419976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c14d62a1e3af4fc70cf8a1e0b343005b419033d0a6c67a483b4658b4fae62549`  
		Last Modified: Thu, 21 Nov 2024 19:31:15 GMT  
		Size: 30.6 KB (30632 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; ppc64le

```console
$ docker pull composer@sha256:6471c3128b50189fa0684e11f5ba9dde0cf5be76435d6955c8729dcfce177069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76730823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f2f1602dd4a116d4de2a3914d4549eaae1cebc3cc86b39c36a2303db5e8a9a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2473147d3bc2923a26c8ba560c425ef2674fbae2edbc29833bb5790c2c94db2`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 5.6 MB (5572572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53975073457162c05af82756884811d86cf52d05953b0589749a216a80864431`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58037573bd03f9687676a3398cb715ac628a3bc280f63aa990e8171ef59ce1c9`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f80183c138cedf9dc24420caf7f9769369bf61c8db0eb09729c4303c31ba1b`  
		Last Modified: Thu, 21 Nov 2024 18:14:28 GMT  
		Size: 13.6 MB (13572757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1746563bd5a8883ee2e1758e12423a999df46412bbeb663f9f774dc595e96ed`  
		Last Modified: Thu, 21 Nov 2024 18:14:27 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3428ebe5f2568169c292765c92b0cc55c0ef85fc46ab1c4d0b60b2d86970b4b3`  
		Last Modified: Thu, 21 Nov 2024 18:14:29 GMT  
		Size: 21.7 MB (21712721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f8424c24e908ec0192f8ff40322e44264734608539de7427be91c3398884dc`  
		Last Modified: Thu, 21 Nov 2024 18:14:27 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef3b5629726f19111a47ee6dc86f22265d0002270ef68da5bb572a2fa8a6d04`  
		Last Modified: Thu, 21 Nov 2024 18:14:28 GMT  
		Size: 19.4 KB (19424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf7d67a2a72f10bea3ee74b2250affb6d2de6aac3751149e9003e6b4ff24a2e`  
		Last Modified: Thu, 21 Nov 2024 21:22:37 GMT  
		Size: 31.4 MB (31402451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011cd0419150962df2f83f6c5e96043ca7df1ddb5a812e226d6f2b98814c7fc0`  
		Last Modified: Thu, 21 Nov 2024 21:22:35 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff276f1507c273d3ac8e2f1347db08fa9f3a7446e1208315cc4a7dd40c9366f8`  
		Last Modified: Thu, 21 Nov 2024 21:23:38 GMT  
		Size: 873.6 KB (873567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a783a497ac98b52f6ba3fab1e879d47fc1c667b088a53d1e1c55ec0b801d7a`  
		Last Modified: Thu, 21 Nov 2024 21:23:38 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575b447e5395cb0169ef16815a1e03559492888b43ee8a46e52dd46d3c589503`  
		Last Modified: Thu, 21 Nov 2024 21:23:38 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:d577c45086565b8c546d0b88c59f6921da8cd5ed17132111a8e7e657c7e98c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2175557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84791cd025a60cebd27ecd9f8f5ec55ee96983d807373839f865602bc99bc043`

```dockerfile
```

-	Layers:
	-	`sha256:9703b93fd237691d1ea4841d323889d2a0c276a3bca97030a550e92f98a683c0`  
		Last Modified: Thu, 21 Nov 2024 21:23:38 GMT  
		Size: 2.1 MB (2144851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04775ba402f4f95f561c4a738ad64290a56acf5ad60d48e028bc05677f3fe017`  
		Last Modified: Thu, 21 Nov 2024 21:23:38 GMT  
		Size: 30.7 KB (30706 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; riscv64

```console
$ docker pull composer@sha256:1b87bd93805801aedd14a04369e29ba8270da7b70c92d2dbe26ecb5954635291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69748763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00729bca6163735bda0cc3607242b21ea01432fbb50fb6ac63615abd1eea7615`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
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
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8ca85c9d20c6f76d0a8087ac3a4ddd6a1e40652d189dc8dad7ca6b0737c4b0`  
		Last Modified: Tue, 12 Nov 2024 06:14:49 GMT  
		Size: 5.4 MB (5382174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d2dfe107b4bddcc389bedcee9ca3fc81f02dc0799e313c21f307ddb454b4dc`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df7310166e795cb48e721a885b92af688db981613ad6597943011293aca738c`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626cc5aa152e22cd453ede74c922b963a3bc8a4bcf66d8a4763c977a36db9bbf`  
		Last Modified: Tue, 12 Nov 2024 11:38:11 GMT  
		Size: 12.5 MB (12504597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e68d6f9ff3ad2f5f92d5d2e1da7c8e8e8c7acf26714c65fb1634379b0ceabea`  
		Last Modified: Tue, 12 Nov 2024 11:38:08 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7ef4ac959dd31d8a66fcf270291f1312424b277d8adec2eded58a835d3130c`  
		Last Modified: Tue, 12 Nov 2024 11:38:11 GMT  
		Size: 16.8 MB (16791439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f9910ad73e6186422edca968a56743133f52309ae7e8fbfaeba5689ec14ce1`  
		Last Modified: Tue, 12 Nov 2024 11:38:08 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cccb83ba6c8bd3926d00dba2c6475d1639c61ec7b4dc48a094f44e9ef2d363f`  
		Last Modified: Tue, 12 Nov 2024 11:38:10 GMT  
		Size: 19.4 KB (19444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1184794faa4cb72388841b6ca5edd801726298f1bc7a901384a6611a072b84d`  
		Last Modified: Wed, 13 Nov 2024 13:17:47 GMT  
		Size: 30.8 MB (30811150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0835e0d761497dfe92dfd2f01937792ca5c678bba375a232324b9fbb0ba5120`  
		Last Modified: Wed, 13 Nov 2024 13:17:42 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def70436aad825b91c93f68e6cd9319acc47844dd03907e4b3f58fd57ed6fb74`  
		Last Modified: Thu, 14 Nov 2024 17:36:28 GMT  
		Size: 863.6 KB (863606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8833f40640acdf41afe00d9e8ec372094a3162b1f5e9a2eee402b886fd020d26`  
		Last Modified: Thu, 14 Nov 2024 17:36:28 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d623967f7eb7838edfd7d9aba19dc57c5f949bb72f6a819cb1fbd7ac74bf618e`  
		Last Modified: Thu, 14 Nov 2024 17:36:28 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:c21c2a3cced01019307214354233618d4716e9211c62d1862ada2734b2ebd6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2175183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f730e9238a7e14feb8548bedb11b7840f35b70218e1751440d9d1083d2d88b11`

```dockerfile
```

-	Layers:
	-	`sha256:1b678c2f08fb3128c3ebca438809479b25ef7fc75678086e49859c98bf31b6e3`  
		Last Modified: Thu, 14 Nov 2024 17:36:28 GMT  
		Size: 2.1 MB (2144468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7574c9ca63cd3b5b86dc11bd65d12591c592c14480a000581566e7013419689c`  
		Last Modified: Thu, 14 Nov 2024 17:36:28 GMT  
		Size: 30.7 KB (30715 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; s390x

```console
$ docker pull composer@sha256:c05f08b3551475a37a9c85853c3c189b9779f5d0476e596bfbf6ca0a83ecd699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76051227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9836f25e54ec98e36c87729fed3064714b271c72cee9c557d81b2e652e9a12`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26915a92034b18e2de9232a415d1ad92dc1c7a9f9e2b5bb9c590ce4c503ab73e`  
		Last Modified: Tue, 12 Nov 2024 03:39:27 GMT  
		Size: 5.5 MB (5532119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4041b6d620078267a8ee6dd6b9c31735d82dee5f22aa96467865a8134d616c`  
		Last Modified: Tue, 12 Nov 2024 03:39:26 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5555efb309fc5275c2fd44eabaaf4ca859f01b510ef24cbad6009d7ed6dc4696`  
		Last Modified: Tue, 12 Nov 2024 03:39:26 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ebcb70bd65f646a0a9f4f475ec50ab3b189c26c5453f7261bc927c566c16f4`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 13.6 MB (13572754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1fe669f736130225879d8f3a94b1a2dc84c8a542232c1010d5c0efdfb490ab`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ebb202afe7221a69abb8b0e5dd9a734085f863f2a450dd0794f4e1c6bc5189`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 21.3 MB (21250100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7a60154e6bcac48ec5bae22b14f7b46c6200a532944883ccb70d97a5f9ff15`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76035e400728cb3a6c7bd01204127072929a705a4be9f5ab31588ec5dce5bd70`  
		Last Modified: Thu, 21 Nov 2024 18:24:27 GMT  
		Size: 19.4 KB (19435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391e13c55cb9dd9b3adaa2c815b5a344bfd110a0afc12b82e71ba8af9327a7a3`  
		Last Modified: Thu, 21 Nov 2024 21:24:03 GMT  
		Size: 31.3 MB (31338617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d1aea81c97d878724863520afce631476bbf2f86f4eaf2a4b781b5d4f855ba`  
		Last Modified: Thu, 21 Nov 2024 21:24:02 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b7be21a6dd37e02c120d709b9d0bb379b04287af4d63cbcd8c8fb5f2c18b4e`  
		Last Modified: Thu, 21 Nov 2024 21:24:57 GMT  
		Size: 871.7 KB (871735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda851f9276d2b6e87f74a89ad041fff1d95d8c68662512cbcabe416d9541cc9`  
		Last Modified: Thu, 21 Nov 2024 21:24:57 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4439b65fae976103d9df04da80b1c25779e74128097f8581fa46d47fccb2ea2`  
		Last Modified: Thu, 21 Nov 2024 21:24:52 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:3f04c199b7ba482fb2fa4107a95a5393e8e9df001d691631faed57bcddf9b7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2174917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca358a0f39ac9866f37e5c8b7451afe7c8bf7a637840a7f941c91e9209c3e9a0`

```dockerfile
```

-	Layers:
	-	`sha256:22bf62761c035de19bac7e81a734db5d49aba267cdc0b4abe515a621ca906fac`  
		Last Modified: Thu, 21 Nov 2024 21:24:57 GMT  
		Size: 2.1 MB (2144253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:986552d0afe5bdcf0fd315f09a2692cef9f7398406690e5e64a8f7df76e8185b`  
		Last Modified: Thu, 21 Nov 2024 21:24:57 GMT  
		Size: 30.7 KB (30664 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10.27`

```console
$ docker pull composer@sha256:07ba70f0c0ae5c1ec693f8a2d06dbbc1e751a83aae3ada1229a4c2a731974858
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
$ docker pull composer@sha256:271c61c137814ae9dc30c52db0369fe63fe03c037b26c5ce16e806d5fce59094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74791707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3298b88edb965e9ee1c0083c52993d7fef5ba52efddbbd1c54b7e9f0dd63bc70`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4026d1cc5245f59e156bffd596323974be67dd48771842c57ace1b9fcb840`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 5.6 MB (5583566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca19f9a3dd1a82729217796a0e8ef626bd25c881db51316ae1d7b6baca3c979`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d429435d57d0d3420a2bb847cb1a04a76483e18d14ae4486b653e998810c2dc8`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22359169dee3cb23309dde8b4845f0a26d5ced82572690f0ec5de9aa5c37df6b`  
		Last Modified: Thu, 21 Nov 2024 18:00:31 GMT  
		Size: 13.6 MB (13572755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60636de7ac448f3bfc52c2d3f3fbdd7e572b65b45a980647e217005c89f46ddd`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6574e97188f3a55184dd55cbc3377b5b1826fe8ac69257fc044d8d1826cf62a`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 20.8 MB (20763608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0db01ff42c14dc52ac7bd7aad09e0a0e2b0050a0ad2796a55eb92246ce39d2`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e12f7079c7bc22fa3df852b4eebe6e7b01a834b3924a0f365f1b0f3437b7eab`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 19.7 KB (19661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68923c66655255aedb65dd09e59a37aaa412e773dfbd12c4b0b808ad5eee6f87`  
		Last Modified: Thu, 21 Nov 2024 18:10:42 GMT  
		Size: 30.4 MB (30368562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb78a38fa743ba495e6f5cc9d38bb8ccd7d84cd2115b43fc683282d9e0cf122`  
		Last Modified: Thu, 21 Nov 2024 18:10:40 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905723d4efe3958647df07867bf18f602de0ef65a0344b331ca70e5e1c11d305`  
		Last Modified: Thu, 21 Nov 2024 18:10:41 GMT  
		Size: 854.8 KB (854802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c251cb0cf2f282bf47bae3434ac36afaf46b6b4e168441d7361b7f3f76650431`  
		Last Modified: Thu, 21 Nov 2024 18:10:40 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb0c74b28b1a5cf47e26e8fec2c840aca547b64a308d1f713a87c93c3561567`  
		Last Modified: Thu, 21 Nov 2024 18:10:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:834e10e96e2c184faeac9fd6318bb4c542bbc65e735f53f1e5ec80e6414bf15c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ea0f462a32e67502f906cb5fdcbda3700837f2bf5c5001a08e662f0de542cf`

```dockerfile
```

-	Layers:
	-	`sha256:7ebc56eca022572000f8c4951b23f6a51625686b37922183512398192b60ec5d`  
		Last Modified: Thu, 21 Nov 2024 18:10:40 GMT  
		Size: 2.1 MB (2146302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ed6a13ee18a234d21ef1846067d9e94bb299f2fcab272f15fc75687f0a376d0`  
		Last Modified: Thu, 21 Nov 2024 18:10:40 GMT  
		Size: 30.7 KB (30664 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v6

```console
$ docker pull composer@sha256:d436d6a8df64d4f2d3975a371459ebf45a6b2a01ae15b63ad363dda5ac1ae094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71251046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66548c01bab1b1ef118b3f7e8815c43feb7a5a8fe6b6245f23436d1cbfe7ddf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdae56950198dea1248e6f62d7e9ef311c976d55790449240dfa46ad43351f7`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 5.2 MB (5236002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773d98c98ade13dc692eaf9700be32a03220033d99905be410eda923ce054fb9`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ae964d3deb57dca49dadfc5c487d64a372e3df3db6ef51b58087c318beb33d`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851605dfb3d928a53fef3860db97edb0f94316d382df472a9f36d31603ae85dc`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 13.6 MB (13572750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb476219577608ba4633ce4f2bf10a95d8fd1bd1bb56c2fb972587e5207cb3f`  
		Last Modified: Thu, 21 Nov 2024 17:58:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698c845cc5fd3760e20d315377bdca792a2b899c35f1288b5ddf2bf66c3e10d4`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 19.0 MB (19027128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7c3d46b7180237d2a402261f2cb181901e0149fed38e5a97d2214f64ba90ac`  
		Last Modified: Thu, 21 Nov 2024 17:58:04 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72176ade970c8f4af9d251ca5d0fc1aefd6e0fa47866d9d792bf9e85a4ac16c`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 19.4 KB (19437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487dce5effb993971148992fe8918fe413df14e91c1a17c2d7a26c254d6a7b29`  
		Last Modified: Thu, 21 Nov 2024 19:21:58 GMT  
		Size: 29.2 MB (29169296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812056dc604d2f3d588dcb3b1441239d4f3a938f21cabe40a0c26a26245a6f23`  
		Last Modified: Thu, 21 Nov 2024 19:21:57 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a0bd9e12093a9ba38738b70817db6b7187d4855220a01d4dc852c966b94a84`  
		Last Modified: Thu, 21 Nov 2024 19:22:38 GMT  
		Size: 855.0 KB (854973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed5767f74313c3e5de86f485fe9bbe739863c243e3873bfd4cd246bc2251e8f`  
		Last Modified: Thu, 14 Nov 2024 17:28:22 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a862f13a225e8dc51a6e453b4bf82929be1892d05c31143272be56474da71077`  
		Last Modified: Thu, 21 Nov 2024 19:22:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:01f1a493411308fe6b6e86513377669613599dbac58bcae9de96e139f7d0fbcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc845c14c1fc28db2c2ea5c011979005443f46c56788c3cc1abba71f384a031f`

```dockerfile
```

-	Layers:
	-	`sha256:8bb8f2588138ccd3eff9d3b85191c4ef6e977ff6bb795d411fe5fdba47718005`  
		Last Modified: Thu, 21 Nov 2024 19:22:37 GMT  
		Size: 30.5 KB (30543 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v7

```console
$ docker pull composer@sha256:514895123da8e0bfb7f864e3df3e3b7ffe6724ca7d7e4dc148001d81df2f7b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69147109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e039a5774f9a4e85c4316232efa6f899478ede7e731877afb04c223f4c8d10a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2878563f55378e5cb0d2e6fc051acec0bad59706b4c55d991502e489d45f15b9`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 4.9 MB (4894482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1da599409a1b1b855c6d69889b78470128711398dd127ceb61f803c590c9c39`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fec221aedc472ddb77d24345957296ec946aab0b124953af99b1b103ca464d6`  
		Last Modified: Tue, 12 Nov 2024 03:55:37 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46d0dd0a80f3bfa93fe376e12f14d3cf1bf7c86c9c039106b233b8584ec9aac`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 13.6 MB (13572743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d138265234b8809a223e845ff20a559fa757eebafc98f9e9bf724fe8e7dc8b6c`  
		Last Modified: Thu, 21 Nov 2024 18:28:27 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b99f01624e25d17567cb4316e05b197890eaf269e39da90cf62573fc75f8dab`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 17.9 MB (17928178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc46c2ae1e666fefa71dcffefd35978d65be61640f7a3dae1293e1c413955d01`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4995aff739b8938a9a1f51923b6e970cc4d974c131fb8f2f8be37bd64c89bf1e`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 19.5 KB (19454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8371af98339513b427681640d9952ffda9674c0a7837c1f5e1ca4b91fa04e1`  
		Last Modified: Thu, 21 Nov 2024 22:48:27 GMT  
		Size: 28.8 MB (28798173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7861e6ac85a5be9e606f1a0b1ed4b0869e26847132c16ba05c326da3b82f1fb`  
		Last Modified: Thu, 21 Nov 2024 22:48:26 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17c7640c26724864975077bf1e09f1bc144baec0963df65ea611bd0db7e7c1a`  
		Last Modified: Thu, 21 Nov 2024 22:49:43 GMT  
		Size: 833.7 KB (833728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c986168709ad21a473495a55e31d91312bc9d6e2191d5bd45a177f16e72872fa`  
		Last Modified: Thu, 21 Nov 2024 22:49:43 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e303a6405c7d0268805b35c2753d13e230ba7b71b8621e6999232cf659d5ee`  
		Last Modified: Thu, 21 Nov 2024 22:49:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:8900bb1bae91598a6abb3f9fc19778c688d2eb6c5323b75c2ee5d4623c7cc107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd33650b2a16cc0f8118ff841aac3d24129f79d478c8e054820ef4435097aeca`

```dockerfile
```

-	Layers:
	-	`sha256:bdd752f419f5d036c1eb0e27f30d8a3cc8318b10aaf178cb51b308b094f3e292`  
		Last Modified: Thu, 21 Nov 2024 22:49:42 GMT  
		Size: 2.1 MB (2146615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd8dfb138a4c035491e50f18aa124940d7cacef37e67e48c6cc9fd6fbff21d15`  
		Last Modified: Thu, 21 Nov 2024 22:49:42 GMT  
		Size: 30.8 KB (30758 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:8c09078aa0143c4c74f5e6eba17a4628e4fbc0798f1adbdca5c00399342d7e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75854450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af832822517b339994dd32d9f6bfa26b6562112cd86d8ff1686012a32cb9b468`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8484336630ebb870b45fd46b300831768da17cae91aa6a615fe97d849bf7d9`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 6.0 MB (6047382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f0bf50f7dfd6864235893d3a770f2748c511f29a319b959cd61ab88719f191`  
		Last Modified: Thu, 21 Nov 2024 18:25:40 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4094551f517548ba326fd9610784089231cb5fe7b32fb0fd484b4ef62a06ec4e`  
		Last Modified: Thu, 21 Nov 2024 18:25:40 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f3a19954028229594dc87f84401ff6bb04343f60f6850d3ffd56376584e127`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 13.6 MB (13572746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cec773ac8fce78f9e43c85101520fcc9a1dfd15d5ae6b0086a53ed446c44e83`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c49e3ab1eba1efe295397f466820586f5b4c820bf03494c07afc622cb0d4b80`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 20.4 MB (20379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f558eac651d11a18dc2c9e83c547cfe4241937c5dc84ca0e2f00d0fcc438eb`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec25731eb581dc3064873d8a03e05f5820ff6c09af884fce4b25f79b77d6f34e`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 19.4 KB (19426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7fe1a5fdee0abebec8c80d0770c46acf11edac729c491803ec919a7373c8c`  
		Last Modified: Thu, 21 Nov 2024 22:17:56 GMT  
		Size: 30.9 MB (30879490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0fda769fb77685ab9ff0bd8069d8c4670c1a85af4283162afa7524a8124d45`  
		Last Modified: Thu, 21 Nov 2024 22:17:55 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3335c5ef4a35514bfc87bb05ddcb1ee519fd4122e61a41bfb420aecd63e58cb`  
		Last Modified: Thu, 21 Nov 2024 22:18:43 GMT  
		Size: 863.8 KB (863813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca999384ec6746acf1e469fc0eb9cc73c295632ff0fa2a7afe6b13d7a4cf8b5`  
		Last Modified: Thu, 21 Nov 2024 22:18:43 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634de817593f116268a9879e4501325e7636c63b131e19d91fe1138ac601f8b1`  
		Last Modified: Thu, 21 Nov 2024 22:18:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:4088ab6830b52313a01b43473d7e5e2d74223a4ffb86cd106921fd9ba16c8728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76fb29bd68f438752d253299e46b00a9f9715c12f8c6c36275528069c829ee2f`

```dockerfile
```

-	Layers:
	-	`sha256:bc5c192a57b0d7463da5c5473331e02fa2bae181f22c0745ca80087ac46d8d22`  
		Last Modified: Thu, 21 Nov 2024 22:18:43 GMT  
		Size: 2.1 MB (2146441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d23d5bec7081b2a11ff5a69dade36678b164e78c62346441da13b5ce29d06f0`  
		Last Modified: Thu, 21 Nov 2024 22:18:43 GMT  
		Size: 30.8 KB (30786 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; 386

```console
$ docker pull composer@sha256:26557f734cc9f2b8898c23790680839103ec3a9e98c6314d1bd02d85baba01e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (55956701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e9ee8039d45aa15aaec585ccbc49c883cb228759f3f79564f825bf00fbaa50`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e11d2a2a48dac61e9ac66af5a5b296591c6a200cf9944fd4df55e48749cce57`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 5.5 MB (5468335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3858fed08c63431ed26286b0317883b23277e3ce014a38a3ca7392c05f0e669a`  
		Last Modified: Thu, 21 Nov 2024 18:00:49 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d4c27ab44c7e13de299ad07b09e18b7c98dee3c34fbee400448997573becdb`  
		Last Modified: Thu, 21 Nov 2024 18:00:49 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b25b38e344c1ca4be9ca4235d6cde628e170971af37a03e30f897cf5a758c`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 13.6 MB (13572753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1764d36b8a53c825b53731114444100b7e1bf8a517ab182b4dab438333bee585`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6444425964f24bb27686445f1e394678dae6d912247a4b8f26e4d7b57e90f54`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 21.3 MB (21300265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2465ec415dcb964fc8b6deb3edeeddfb60a77336ebafdeeff9780a230562a2`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b021291a02d8b49460ff1ff13393725cf6e1616dbb1b2a1ef9c7a69fdeab5b4`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 19.6 KB (19644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b1bc8fa7da4b6087462666fa266fcabca74d746c2d07ee57a21670a552b92f`  
		Last Modified: Thu, 21 Nov 2024 19:31:15 GMT  
		Size: 11.3 MB (11281344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aafffe5ec1d54ba87a86bf601eb7f84880e74c50040c43638027881aaeca84`  
		Last Modified: Thu, 21 Nov 2024 19:31:15 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb76b7393013da6f7706b7b520b04826cf2d79befa4a047b929772130690e69e`  
		Last Modified: Thu, 21 Nov 2024 19:31:15 GMT  
		Size: 840.3 KB (840284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2453a27148d2afe3b36a639140a4e7fecf776c29bfe59e96838ab091c98e744`  
		Last Modified: Thu, 21 Nov 2024 19:31:15 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52942540edf0e81f0e5b34b27fe7d54df44188c6c0fc472f4a87b6f07fe7e584`  
		Last Modified: Thu, 21 Nov 2024 19:31:16 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:858132f021f1dec88a334ddc42238ad7f185e6ab66af68fff03c4ff543b1cb6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.6 KB (450608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c017cd16f8a0aeb7afbca5190fbc71427d6b7b31c4e9dbc8a4adec733a99f14b`

```dockerfile
```

-	Layers:
	-	`sha256:e58d9c79a82c41c17b6949b43650e2a5a10af472103cd0801753531ea4603dd5`  
		Last Modified: Thu, 21 Nov 2024 19:31:15 GMT  
		Size: 420.0 KB (419976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c14d62a1e3af4fc70cf8a1e0b343005b419033d0a6c67a483b4658b4fae62549`  
		Last Modified: Thu, 21 Nov 2024 19:31:15 GMT  
		Size: 30.6 KB (30632 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; ppc64le

```console
$ docker pull composer@sha256:6471c3128b50189fa0684e11f5ba9dde0cf5be76435d6955c8729dcfce177069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76730823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f2f1602dd4a116d4de2a3914d4549eaae1cebc3cc86b39c36a2303db5e8a9a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2473147d3bc2923a26c8ba560c425ef2674fbae2edbc29833bb5790c2c94db2`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 5.6 MB (5572572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53975073457162c05af82756884811d86cf52d05953b0589749a216a80864431`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58037573bd03f9687676a3398cb715ac628a3bc280f63aa990e8171ef59ce1c9`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f80183c138cedf9dc24420caf7f9769369bf61c8db0eb09729c4303c31ba1b`  
		Last Modified: Thu, 21 Nov 2024 18:14:28 GMT  
		Size: 13.6 MB (13572757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1746563bd5a8883ee2e1758e12423a999df46412bbeb663f9f774dc595e96ed`  
		Last Modified: Thu, 21 Nov 2024 18:14:27 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3428ebe5f2568169c292765c92b0cc55c0ef85fc46ab1c4d0b60b2d86970b4b3`  
		Last Modified: Thu, 21 Nov 2024 18:14:29 GMT  
		Size: 21.7 MB (21712721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f8424c24e908ec0192f8ff40322e44264734608539de7427be91c3398884dc`  
		Last Modified: Thu, 21 Nov 2024 18:14:27 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef3b5629726f19111a47ee6dc86f22265d0002270ef68da5bb572a2fa8a6d04`  
		Last Modified: Thu, 21 Nov 2024 18:14:28 GMT  
		Size: 19.4 KB (19424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf7d67a2a72f10bea3ee74b2250affb6d2de6aac3751149e9003e6b4ff24a2e`  
		Last Modified: Thu, 21 Nov 2024 21:22:37 GMT  
		Size: 31.4 MB (31402451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011cd0419150962df2f83f6c5e96043ca7df1ddb5a812e226d6f2b98814c7fc0`  
		Last Modified: Thu, 21 Nov 2024 21:22:35 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff276f1507c273d3ac8e2f1347db08fa9f3a7446e1208315cc4a7dd40c9366f8`  
		Last Modified: Thu, 21 Nov 2024 21:23:38 GMT  
		Size: 873.6 KB (873567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a783a497ac98b52f6ba3fab1e879d47fc1c667b088a53d1e1c55ec0b801d7a`  
		Last Modified: Thu, 21 Nov 2024 21:23:38 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575b447e5395cb0169ef16815a1e03559492888b43ee8a46e52dd46d3c589503`  
		Last Modified: Thu, 21 Nov 2024 21:23:38 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:d577c45086565b8c546d0b88c59f6921da8cd5ed17132111a8e7e657c7e98c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2175557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84791cd025a60cebd27ecd9f8f5ec55ee96983d807373839f865602bc99bc043`

```dockerfile
```

-	Layers:
	-	`sha256:9703b93fd237691d1ea4841d323889d2a0c276a3bca97030a550e92f98a683c0`  
		Last Modified: Thu, 21 Nov 2024 21:23:38 GMT  
		Size: 2.1 MB (2144851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04775ba402f4f95f561c4a738ad64290a56acf5ad60d48e028bc05677f3fe017`  
		Last Modified: Thu, 21 Nov 2024 21:23:38 GMT  
		Size: 30.7 KB (30706 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; riscv64

```console
$ docker pull composer@sha256:1b87bd93805801aedd14a04369e29ba8270da7b70c92d2dbe26ecb5954635291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69748763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00729bca6163735bda0cc3607242b21ea01432fbb50fb6ac63615abd1eea7615`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
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
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8ca85c9d20c6f76d0a8087ac3a4ddd6a1e40652d189dc8dad7ca6b0737c4b0`  
		Last Modified: Tue, 12 Nov 2024 06:14:49 GMT  
		Size: 5.4 MB (5382174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d2dfe107b4bddcc389bedcee9ca3fc81f02dc0799e313c21f307ddb454b4dc`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df7310166e795cb48e721a885b92af688db981613ad6597943011293aca738c`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626cc5aa152e22cd453ede74c922b963a3bc8a4bcf66d8a4763c977a36db9bbf`  
		Last Modified: Tue, 12 Nov 2024 11:38:11 GMT  
		Size: 12.5 MB (12504597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e68d6f9ff3ad2f5f92d5d2e1da7c8e8e8c7acf26714c65fb1634379b0ceabea`  
		Last Modified: Tue, 12 Nov 2024 11:38:08 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7ef4ac959dd31d8a66fcf270291f1312424b277d8adec2eded58a835d3130c`  
		Last Modified: Tue, 12 Nov 2024 11:38:11 GMT  
		Size: 16.8 MB (16791439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f9910ad73e6186422edca968a56743133f52309ae7e8fbfaeba5689ec14ce1`  
		Last Modified: Tue, 12 Nov 2024 11:38:08 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cccb83ba6c8bd3926d00dba2c6475d1639c61ec7b4dc48a094f44e9ef2d363f`  
		Last Modified: Tue, 12 Nov 2024 11:38:10 GMT  
		Size: 19.4 KB (19444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1184794faa4cb72388841b6ca5edd801726298f1bc7a901384a6611a072b84d`  
		Last Modified: Wed, 13 Nov 2024 13:17:47 GMT  
		Size: 30.8 MB (30811150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0835e0d761497dfe92dfd2f01937792ca5c678bba375a232324b9fbb0ba5120`  
		Last Modified: Wed, 13 Nov 2024 13:17:42 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def70436aad825b91c93f68e6cd9319acc47844dd03907e4b3f58fd57ed6fb74`  
		Last Modified: Thu, 14 Nov 2024 17:36:28 GMT  
		Size: 863.6 KB (863606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8833f40640acdf41afe00d9e8ec372094a3162b1f5e9a2eee402b886fd020d26`  
		Last Modified: Thu, 14 Nov 2024 17:36:28 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d623967f7eb7838edfd7d9aba19dc57c5f949bb72f6a819cb1fbd7ac74bf618e`  
		Last Modified: Thu, 14 Nov 2024 17:36:28 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:c21c2a3cced01019307214354233618d4716e9211c62d1862ada2734b2ebd6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2175183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f730e9238a7e14feb8548bedb11b7840f35b70218e1751440d9d1083d2d88b11`

```dockerfile
```

-	Layers:
	-	`sha256:1b678c2f08fb3128c3ebca438809479b25ef7fc75678086e49859c98bf31b6e3`  
		Last Modified: Thu, 14 Nov 2024 17:36:28 GMT  
		Size: 2.1 MB (2144468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7574c9ca63cd3b5b86dc11bd65d12591c592c14480a000581566e7013419689c`  
		Last Modified: Thu, 14 Nov 2024 17:36:28 GMT  
		Size: 30.7 KB (30715 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; s390x

```console
$ docker pull composer@sha256:c05f08b3551475a37a9c85853c3c189b9779f5d0476e596bfbf6ca0a83ecd699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76051227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9836f25e54ec98e36c87729fed3064714b271c72cee9c557d81b2e652e9a12`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26915a92034b18e2de9232a415d1ad92dc1c7a9f9e2b5bb9c590ce4c503ab73e`  
		Last Modified: Tue, 12 Nov 2024 03:39:27 GMT  
		Size: 5.5 MB (5532119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4041b6d620078267a8ee6dd6b9c31735d82dee5f22aa96467865a8134d616c`  
		Last Modified: Tue, 12 Nov 2024 03:39:26 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5555efb309fc5275c2fd44eabaaf4ca859f01b510ef24cbad6009d7ed6dc4696`  
		Last Modified: Tue, 12 Nov 2024 03:39:26 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ebcb70bd65f646a0a9f4f475ec50ab3b189c26c5453f7261bc927c566c16f4`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 13.6 MB (13572754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1fe669f736130225879d8f3a94b1a2dc84c8a542232c1010d5c0efdfb490ab`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ebb202afe7221a69abb8b0e5dd9a734085f863f2a450dd0794f4e1c6bc5189`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 21.3 MB (21250100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7a60154e6bcac48ec5bae22b14f7b46c6200a532944883ccb70d97a5f9ff15`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76035e400728cb3a6c7bd01204127072929a705a4be9f5ab31588ec5dce5bd70`  
		Last Modified: Thu, 21 Nov 2024 18:24:27 GMT  
		Size: 19.4 KB (19435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391e13c55cb9dd9b3adaa2c815b5a344bfd110a0afc12b82e71ba8af9327a7a3`  
		Last Modified: Thu, 21 Nov 2024 21:24:03 GMT  
		Size: 31.3 MB (31338617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d1aea81c97d878724863520afce631476bbf2f86f4eaf2a4b781b5d4f855ba`  
		Last Modified: Thu, 21 Nov 2024 21:24:02 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b7be21a6dd37e02c120d709b9d0bb379b04287af4d63cbcd8c8fb5f2c18b4e`  
		Last Modified: Thu, 21 Nov 2024 21:24:57 GMT  
		Size: 871.7 KB (871735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda851f9276d2b6e87f74a89ad041fff1d95d8c68662512cbcabe416d9541cc9`  
		Last Modified: Thu, 21 Nov 2024 21:24:57 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4439b65fae976103d9df04da80b1c25779e74128097f8581fa46d47fccb2ea2`  
		Last Modified: Thu, 21 Nov 2024 21:24:52 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:3f04c199b7ba482fb2fa4107a95a5393e8e9df001d691631faed57bcddf9b7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2174917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca358a0f39ac9866f37e5c8b7451afe7c8bf7a637840a7f941c91e9209c3e9a0`

```dockerfile
```

-	Layers:
	-	`sha256:22bf62761c035de19bac7e81a734db5d49aba267cdc0b4abe515a621ca906fac`  
		Last Modified: Thu, 21 Nov 2024 21:24:57 GMT  
		Size: 2.1 MB (2144253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:986552d0afe5bdcf0fd315f09a2692cef9f7398406690e5e64a8f7df76e8185b`  
		Last Modified: Thu, 21 Nov 2024 21:24:57 GMT  
		Size: 30.7 KB (30664 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2`

```console
$ docker pull composer@sha256:8bbdf5ccb6c6ddd23c578cf0e80243b42addabc07f9d421f617a166e9afe84f5
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
$ docker pull composer@sha256:4e059cb2b0bc5a68edf1cc4d310072f47831855a417f492cb5a18a82e49cf76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75020361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3f4c1ff4e156cfeb9f0ef1bc602bce75485db306c03438e390874f6589216f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4026d1cc5245f59e156bffd596323974be67dd48771842c57ace1b9fcb840`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 5.6 MB (5583566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca19f9a3dd1a82729217796a0e8ef626bd25c881db51316ae1d7b6baca3c979`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d429435d57d0d3420a2bb847cb1a04a76483e18d14ae4486b653e998810c2dc8`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22359169dee3cb23309dde8b4845f0a26d5ced82572690f0ec5de9aa5c37df6b`  
		Last Modified: Thu, 21 Nov 2024 18:00:31 GMT  
		Size: 13.6 MB (13572755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60636de7ac448f3bfc52c2d3f3fbdd7e572b65b45a980647e217005c89f46ddd`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6574e97188f3a55184dd55cbc3377b5b1826fe8ac69257fc044d8d1826cf62a`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 20.8 MB (20763608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0db01ff42c14dc52ac7bd7aad09e0a0e2b0050a0ad2796a55eb92246ce39d2`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e12f7079c7bc22fa3df852b4eebe6e7b01a834b3924a0f365f1b0f3437b7eab`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 19.7 KB (19661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa4e2f4bc7afd1f94a77567f83ba03777652ce81c4c159b7b5a3fd802f9a07f`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 30.4 MB (30368666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f00e6d7d58a0de384fb60d6cae9d9e89e93999483637376e44408cd5568bfb`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d38d791dd39b847b0d2fca9f88e1f9e5a32deabf8d1db6f92e7ebb1e8e43a9`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 1.1 MB (1083341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30cdbc582e7a47a26c3d2987f21b875b06c7e908768493752631cdd9d6c620e`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f722a00c1e03183935b573019373cf60f3ec25db1c4eee7ca88b9f9b04d218`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:ae44f042feb54af530dcaede39a40f1c6e061dbb0cee268407a9e5542014a307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6565fd02e5ace02440f1e5fd8f5bb2b3a3b5cb7ceeddacca1956af65a4fe5f4c`

```dockerfile
```

-	Layers:
	-	`sha256:bf003505388f520b1732b29b58a5b2a33d4f01c44c01adc95b5a51dfea808f43`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 2.1 MB (2147787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f5510ab4926f7df0fd363daf31833ba811e31f90655736c575847e831f23e82`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 31.0 KB (30961 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v6

```console
$ docker pull composer@sha256:a1a8aa8dedf34d24825ed172fbc10989ee1d018f39755c722050e86662dc6710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71478643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a3debd87b60e1a417ef9aa4a09488eb547162846824c7816e0ef13e96b7175`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdae56950198dea1248e6f62d7e9ef311c976d55790449240dfa46ad43351f7`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 5.2 MB (5236002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773d98c98ade13dc692eaf9700be32a03220033d99905be410eda923ce054fb9`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ae964d3deb57dca49dadfc5c487d64a372e3df3db6ef51b58087c318beb33d`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851605dfb3d928a53fef3860db97edb0f94316d382df472a9f36d31603ae85dc`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 13.6 MB (13572750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb476219577608ba4633ce4f2bf10a95d8fd1bd1bb56c2fb972587e5207cb3f`  
		Last Modified: Thu, 21 Nov 2024 17:58:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698c845cc5fd3760e20d315377bdca792a2b899c35f1288b5ddf2bf66c3e10d4`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 19.0 MB (19027128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7c3d46b7180237d2a402261f2cb181901e0149fed38e5a97d2214f64ba90ac`  
		Last Modified: Thu, 21 Nov 2024 17:58:04 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72176ade970c8f4af9d251ca5d0fc1aefd6e0fa47866d9d792bf9e85a4ac16c`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 19.4 KB (19437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487dce5effb993971148992fe8918fe413df14e91c1a17c2d7a26c254d6a7b29`  
		Last Modified: Thu, 21 Nov 2024 19:21:58 GMT  
		Size: 29.2 MB (29169296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812056dc604d2f3d588dcb3b1441239d4f3a938f21cabe40a0c26a26245a6f23`  
		Last Modified: Thu, 21 Nov 2024 19:21:57 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c30396d8c38d03f44a9669abfdcb1464e3752bb97120d8313ce5f23687a2197`  
		Last Modified: Thu, 21 Nov 2024 19:23:22 GMT  
		Size: 1.1 MB (1082560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb0c3ba98f312cc7166562cc003a0957dda83f716dde5bfda8830ad7379374b`  
		Last Modified: Mon, 18 Nov 2024 19:48:06 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46386c7251234ca16cef7ef7981829cec1c68a31f633038fae82f6fa4bea6548`  
		Last Modified: Thu, 21 Nov 2024 19:23:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:60e2c0bf91ca903330a7cceee1b41c2a1bbdb267bf7b5e4cc9e5a1c2d822c321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:460c835358535ff48139328c022972640ebc869facb7cf89d3ee604273a63765`

```dockerfile
```

-	Layers:
	-	`sha256:8c21f2e4345b18b3fe6f8b8efa0f6ed566833b64e77ca88d1600710a2bfd87fd`  
		Last Modified: Thu, 21 Nov 2024 19:23:21 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v7

```console
$ docker pull composer@sha256:2a2fda30bd0a71491f52d5f8ba6fd1c8b75128d4f453e41948f7d4b6d449b33d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69375719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd54441d7ac9c328c06b46add65b2869b5cf1eba49739aa76e0dbef1e2c8fb51`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2878563f55378e5cb0d2e6fc051acec0bad59706b4c55d991502e489d45f15b9`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 4.9 MB (4894482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1da599409a1b1b855c6d69889b78470128711398dd127ceb61f803c590c9c39`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fec221aedc472ddb77d24345957296ec946aab0b124953af99b1b103ca464d6`  
		Last Modified: Tue, 12 Nov 2024 03:55:37 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46d0dd0a80f3bfa93fe376e12f14d3cf1bf7c86c9c039106b233b8584ec9aac`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 13.6 MB (13572743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d138265234b8809a223e845ff20a559fa757eebafc98f9e9bf724fe8e7dc8b6c`  
		Last Modified: Thu, 21 Nov 2024 18:28:27 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b99f01624e25d17567cb4316e05b197890eaf269e39da90cf62573fc75f8dab`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 17.9 MB (17928178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc46c2ae1e666fefa71dcffefd35978d65be61640f7a3dae1293e1c413955d01`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4995aff739b8938a9a1f51923b6e970cc4d974c131fb8f2f8be37bd64c89bf1e`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 19.5 KB (19454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8371af98339513b427681640d9952ffda9674c0a7837c1f5e1ca4b91fa04e1`  
		Last Modified: Thu, 21 Nov 2024 22:48:27 GMT  
		Size: 28.8 MB (28798173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7861e6ac85a5be9e606f1a0b1ed4b0869e26847132c16ba05c326da3b82f1fb`  
		Last Modified: Thu, 21 Nov 2024 22:48:26 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685e48610c1b40acc2e7489adf5cd45075bc17f1989f32ff40ec88bab369412e`  
		Last Modified: Thu, 21 Nov 2024 22:51:00 GMT  
		Size: 1.1 MB (1062327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f436ad28fae8c9b37d0931ddc038b6260d88038cc84c5bac52a80de62e584f`  
		Last Modified: Mon, 18 Nov 2024 20:23:42 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b313c209ec4a8a313770caaea8ce391741ccc849671d0a07bcca4cba673646`  
		Last Modified: Thu, 21 Nov 2024 22:50:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:7fc4bb9deae034836057b0de9d2cd6e75dd5b12a05fca77bfaa86b783e7219ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a837dc411a94406d400408f2f1e540fc9d76247dfafcc1cbd167c8025c31b39`

```dockerfile
```

-	Layers:
	-	`sha256:e7520a751b99b025d4a994bb6fc0fdb2eec68fd15549efc4ef455996369d7149`  
		Last Modified: Thu, 21 Nov 2024 22:50:59 GMT  
		Size: 2.1 MB (2148108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:568ebb246b0ab7809dc7d276c7da38d3d728e1928d445eab02832dbe5a4493f6`  
		Last Modified: Thu, 21 Nov 2024 22:50:59 GMT  
		Size: 31.1 KB (31062 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:4b882bdbb24c6e89273dc14535bcbd6dab179fc237347ff42a8d62c866bf401f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76081794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7595d594af7fee7f4faf35786a3cb54cbbeeae63a9412e75ee8ce6dc7290c3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8484336630ebb870b45fd46b300831768da17cae91aa6a615fe97d849bf7d9`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 6.0 MB (6047382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f0bf50f7dfd6864235893d3a770f2748c511f29a319b959cd61ab88719f191`  
		Last Modified: Thu, 21 Nov 2024 18:25:40 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4094551f517548ba326fd9610784089231cb5fe7b32fb0fd484b4ef62a06ec4e`  
		Last Modified: Thu, 21 Nov 2024 18:25:40 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f3a19954028229594dc87f84401ff6bb04343f60f6850d3ffd56376584e127`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 13.6 MB (13572746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cec773ac8fce78f9e43c85101520fcc9a1dfd15d5ae6b0086a53ed446c44e83`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c49e3ab1eba1efe295397f466820586f5b4c820bf03494c07afc622cb0d4b80`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 20.4 MB (20379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f558eac651d11a18dc2c9e83c547cfe4241937c5dc84ca0e2f00d0fcc438eb`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec25731eb581dc3064873d8a03e05f5820ff6c09af884fce4b25f79b77d6f34e`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 19.4 KB (19426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7fe1a5fdee0abebec8c80d0770c46acf11edac729c491803ec919a7373c8c`  
		Last Modified: Thu, 21 Nov 2024 22:17:56 GMT  
		Size: 30.9 MB (30879490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0fda769fb77685ab9ff0bd8069d8c4670c1a85af4283162afa7524a8124d45`  
		Last Modified: Thu, 21 Nov 2024 22:17:55 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df9080391afa561614604f21c0161c8bad69d4bc52915415b7c1c65f1bf527a`  
		Last Modified: Thu, 21 Nov 2024 22:19:26 GMT  
		Size: 1.1 MB (1091147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54549015f1d85f07424904365c45002761ecb1f1ed4c44d30ad38297de2a6ebb`  
		Last Modified: Thu, 21 Nov 2024 22:19:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c835e644aa517172a0c42a44439508bef9c61bc21a4f1d5b5adb2285038ce2`  
		Last Modified: Thu, 21 Nov 2024 22:19:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:fd81fa9ab08837460f0bfd44ad469400783f6dd4999ddaf52faf5f9f51b241d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e780c631b16e7f52966897fff323da2a156189b610aae94c8a0a2d4e63eb18`

```dockerfile
```

-	Layers:
	-	`sha256:c5abcc231fd8648f0ce4567486331a77eb7892aaaed996a3a02e655bedbd92c1`  
		Last Modified: Thu, 21 Nov 2024 22:19:26 GMT  
		Size: 2.1 MB (2147938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4482946d0eecf5bd8d0b027fef05ac9b3378a4e06e4b379f48e4c15dc881a886`  
		Last Modified: Thu, 21 Nov 2024 22:19:25 GMT  
		Size: 31.1 KB (31095 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; 386

```console
$ docker pull composer@sha256:5895b27fa42c598668b64122527f1f2aed8003aff127fa28729e1e845ea5c115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56186940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785154b0de710a50fc157f346144c8a62d0b24f291fde96abe6e995b1b34687d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e11d2a2a48dac61e9ac66af5a5b296591c6a200cf9944fd4df55e48749cce57`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 5.5 MB (5468335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3858fed08c63431ed26286b0317883b23277e3ce014a38a3ca7392c05f0e669a`  
		Last Modified: Thu, 21 Nov 2024 18:00:49 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d4c27ab44c7e13de299ad07b09e18b7c98dee3c34fbee400448997573becdb`  
		Last Modified: Thu, 21 Nov 2024 18:00:49 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b25b38e344c1ca4be9ca4235d6cde628e170971af37a03e30f897cf5a758c`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 13.6 MB (13572753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1764d36b8a53c825b53731114444100b7e1bf8a517ab182b4dab438333bee585`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6444425964f24bb27686445f1e394678dae6d912247a4b8f26e4d7b57e90f54`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 21.3 MB (21300265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2465ec415dcb964fc8b6deb3edeeddfb60a77336ebafdeeff9780a230562a2`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b021291a02d8b49460ff1ff13393725cf6e1616dbb1b2a1ef9c7a69fdeab5b4`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 19.6 KB (19644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8aabe33271ab76e9f0a0e14600b67129c22b6376b9ac5691140b583e58214`  
		Last Modified: Thu, 21 Nov 2024 18:10:39 GMT  
		Size: 11.3 MB (11281350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91db55eda861b506210850850e90775ccb8a5505fd86fc292beade07dfeb2c7`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e53d342f08d79d0e95d5cb9b8fdac226218ccd7ac8bfb85a3f8be83b4ca0ec9`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 1.1 MB (1070507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab1b7d6b2a7b5eaffc0c95c278d0bb7c18b20204b2b5eae520c71c7090c6f4a`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb0c74b28b1a5cf47e26e8fec2c840aca547b64a308d1f713a87c93c3561567`  
		Last Modified: Thu, 21 Nov 2024 18:10:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:25307faf2d420c206138ef2b318e90ed0512a70e815b45eda1e66c22d7de7870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.4 KB (452381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f11fa5495a188f46f0b1773d57cd753fb004f768200c8b8c087c3d2872b9cff3`

```dockerfile
```

-	Layers:
	-	`sha256:1adf3a09467edab2b6efdb58c8ac6149ca0ff37d945ac99bb7cf5e9979fbada9`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 421.5 KB (421456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b888a5c47580083cfe521b71b5f008ccfc23b0bfbaae5e6aab7398e655f2374e`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 30.9 KB (30925 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; ppc64le

```console
$ docker pull composer@sha256:b31a01870fb72277be00f9566c0fe6d607c86cb57bdc3c1cb0ead0e0d3fd6e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76958826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7777a78f24315baa2ef132135d753c98210a852f450bcc815b8cb9472767bc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2473147d3bc2923a26c8ba560c425ef2674fbae2edbc29833bb5790c2c94db2`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 5.6 MB (5572572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53975073457162c05af82756884811d86cf52d05953b0589749a216a80864431`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58037573bd03f9687676a3398cb715ac628a3bc280f63aa990e8171ef59ce1c9`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f80183c138cedf9dc24420caf7f9769369bf61c8db0eb09729c4303c31ba1b`  
		Last Modified: Thu, 21 Nov 2024 18:14:28 GMT  
		Size: 13.6 MB (13572757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1746563bd5a8883ee2e1758e12423a999df46412bbeb663f9f774dc595e96ed`  
		Last Modified: Thu, 21 Nov 2024 18:14:27 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3428ebe5f2568169c292765c92b0cc55c0ef85fc46ab1c4d0b60b2d86970b4b3`  
		Last Modified: Thu, 21 Nov 2024 18:14:29 GMT  
		Size: 21.7 MB (21712721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f8424c24e908ec0192f8ff40322e44264734608539de7427be91c3398884dc`  
		Last Modified: Thu, 21 Nov 2024 18:14:27 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef3b5629726f19111a47ee6dc86f22265d0002270ef68da5bb572a2fa8a6d04`  
		Last Modified: Thu, 21 Nov 2024 18:14:28 GMT  
		Size: 19.4 KB (19424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf7d67a2a72f10bea3ee74b2250affb6d2de6aac3751149e9003e6b4ff24a2e`  
		Last Modified: Thu, 21 Nov 2024 21:22:37 GMT  
		Size: 31.4 MB (31402451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011cd0419150962df2f83f6c5e96043ca7df1ddb5a812e226d6f2b98814c7fc0`  
		Last Modified: Thu, 21 Nov 2024 21:22:35 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac37fe451ac8534aca4e4e40851e92cc0468a5064576179550c5594bf87157e4`  
		Last Modified: Thu, 21 Nov 2024 21:24:48 GMT  
		Size: 1.1 MB (1101560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14909c3d44cb9216423277a8fff5ce20356c2f7170dff5ae30ad76fa2fe58235`  
		Last Modified: Thu, 21 Nov 2024 21:24:47 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d2063201f1a57cceae80e31658ce1e97b597798722a7ce1a5b6bcf68c9b206`  
		Last Modified: Thu, 21 Nov 2024 21:24:47 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:abcbb063050d224d69d1489b752b0227a8f5e4144d73f0b691f10f5296f85514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b35bdb873177e2ab223c603904bbaca948a7a86b161653ed30eec8a261bc67`

```dockerfile
```

-	Layers:
	-	`sha256:c725c209387c0493e239864a94db3246df808fee3270bc3de3c86bc19e6a398e`  
		Last Modified: Thu, 21 Nov 2024 21:24:48 GMT  
		Size: 2.1 MB (2146342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a73619b309ab318681d8ac6c230f818f2b6cc6f8475cef18f95a964e7b2c8b1`  
		Last Modified: Thu, 21 Nov 2024 21:24:47 GMT  
		Size: 31.0 KB (31007 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; riscv64

```console
$ docker pull composer@sha256:ed8bec923846612aeec9d7c5b4e37d4c27b46e61083ef994d73edacc353eb451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70713138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bbd153b3fff08b930c02c40db9c3bede384367eb09e013935beca56ef232ae`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8ca85c9d20c6f76d0a8087ac3a4ddd6a1e40652d189dc8dad7ca6b0737c4b0`  
		Last Modified: Tue, 12 Nov 2024 06:14:49 GMT  
		Size: 5.4 MB (5382174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d2dfe107b4bddcc389bedcee9ca3fc81f02dc0799e313c21f307ddb454b4dc`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df7310166e795cb48e721a885b92af688db981613ad6597943011293aca738c`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626cc5aa152e22cd453ede74c922b963a3bc8a4bcf66d8a4763c977a36db9bbf`  
		Last Modified: Tue, 12 Nov 2024 11:38:11 GMT  
		Size: 12.5 MB (12504597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e68d6f9ff3ad2f5f92d5d2e1da7c8e8e8c7acf26714c65fb1634379b0ceabea`  
		Last Modified: Tue, 12 Nov 2024 11:38:08 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7ef4ac959dd31d8a66fcf270291f1312424b277d8adec2eded58a835d3130c`  
		Last Modified: Tue, 12 Nov 2024 11:38:11 GMT  
		Size: 16.8 MB (16791439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f9910ad73e6186422edca968a56743133f52309ae7e8fbfaeba5689ec14ce1`  
		Last Modified: Tue, 12 Nov 2024 11:38:08 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cccb83ba6c8bd3926d00dba2c6475d1639c61ec7b4dc48a094f44e9ef2d363f`  
		Last Modified: Tue, 12 Nov 2024 11:38:10 GMT  
		Size: 19.4 KB (19444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1184794faa4cb72388841b6ca5edd801726298f1bc7a901384a6611a072b84d`  
		Last Modified: Wed, 13 Nov 2024 13:17:47 GMT  
		Size: 30.8 MB (30811150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0835e0d761497dfe92dfd2f01937792ca5c678bba375a232324b9fbb0ba5120`  
		Last Modified: Wed, 13 Nov 2024 13:17:42 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07c683546f1dbb73a401c02ec6169c6db9a2e1163a15f184d5c634965a1e5db`  
		Last Modified: Mon, 18 Nov 2024 19:11:38 GMT  
		Size: 1.8 MB (1827970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db5e9fa9e94a1dfd1dbce4db1c03e977d7ef88c4265803e7fb16536ce3901bb`  
		Last Modified: Mon, 18 Nov 2024 19:11:38 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bb7be447bc29d4901509e73b2e709bbfe7daf883f9dc94e2f83ca774cdf247`  
		Last Modified: Mon, 18 Nov 2024 19:11:38 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:699f6536b8af5d06e22a6567155fa157b1c7ee6de20657fe2bfb50c733e9138c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07826998165fa93f84ac501d6a553f14a3c873f356bcdbd20cdb0d1875832fca`

```dockerfile
```

-	Layers:
	-	`sha256:ff4fae5f5ec59bf9f691ec534e5babfe3171a3fe2db50fe20bfe894d62bbc67f`  
		Last Modified: Mon, 18 Nov 2024 19:11:37 GMT  
		Size: 2.1 MB (2145960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e221ef006b10f92faeefea08445fba63054cfdf42a7de63decab79954c796f3`  
		Last Modified: Mon, 18 Nov 2024 19:11:37 GMT  
		Size: 31.0 KB (31018 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; s390x

```console
$ docker pull composer@sha256:e21dca9bf0b9c7065a2aef60fc6a0e3a03a86445503700c9eff2f48792a80f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76278627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0683d3d3b3aceba01f85e8de7138bb8723ea04c6b816570cce7dc9310f0a4973`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26915a92034b18e2de9232a415d1ad92dc1c7a9f9e2b5bb9c590ce4c503ab73e`  
		Last Modified: Tue, 12 Nov 2024 03:39:27 GMT  
		Size: 5.5 MB (5532119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4041b6d620078267a8ee6dd6b9c31735d82dee5f22aa96467865a8134d616c`  
		Last Modified: Tue, 12 Nov 2024 03:39:26 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5555efb309fc5275c2fd44eabaaf4ca859f01b510ef24cbad6009d7ed6dc4696`  
		Last Modified: Tue, 12 Nov 2024 03:39:26 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ebcb70bd65f646a0a9f4f475ec50ab3b189c26c5453f7261bc927c566c16f4`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 13.6 MB (13572754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1fe669f736130225879d8f3a94b1a2dc84c8a542232c1010d5c0efdfb490ab`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ebb202afe7221a69abb8b0e5dd9a734085f863f2a450dd0794f4e1c6bc5189`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 21.3 MB (21250100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7a60154e6bcac48ec5bae22b14f7b46c6200a532944883ccb70d97a5f9ff15`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76035e400728cb3a6c7bd01204127072929a705a4be9f5ab31588ec5dce5bd70`  
		Last Modified: Thu, 21 Nov 2024 18:24:27 GMT  
		Size: 19.4 KB (19435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391e13c55cb9dd9b3adaa2c815b5a344bfd110a0afc12b82e71ba8af9327a7a3`  
		Last Modified: Thu, 21 Nov 2024 21:24:03 GMT  
		Size: 31.3 MB (31338617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d1aea81c97d878724863520afce631476bbf2f86f4eaf2a4b781b5d4f855ba`  
		Last Modified: Thu, 21 Nov 2024 21:24:02 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec41f417f32df8d6b29087fb50d7165f6ba5622272536044aad8346263321cd`  
		Last Modified: Thu, 21 Nov 2024 21:25:56 GMT  
		Size: 1.1 MB (1099124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d41623169f490a3c4b3ad708f3715985370d656560af18567d32dad796bd601`  
		Last Modified: Thu, 21 Nov 2024 21:25:56 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103104b2577b229e90d735ad3b6db3d300d26fd3f7bd0aa3cacbcaf87380344b`  
		Last Modified: Thu, 21 Nov 2024 21:25:56 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:fd2bbd770d3c98acb45d0ea2760f1f299ef68190c3ee369a618a74f8008cab4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ec6c9d823e50f933620ebd04ef4de684361b80bd7821ee35d672f7c6349d57`

```dockerfile
```

-	Layers:
	-	`sha256:f718eb8ddf8df0e06b8bf814924ded8904373825b635c0fd316aac4860492380`  
		Last Modified: Thu, 21 Nov 2024 21:25:55 GMT  
		Size: 2.1 MB (2145738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f05d0590058fbabd4f7c681b6947c6efbf8ba4a06a51353d3354d9ce6a0898e9`  
		Last Modified: Thu, 21 Nov 2024 21:25:55 GMT  
		Size: 31.0 KB (30960 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2`

```console
$ docker pull composer@sha256:866ce87175721248614af82d38ec0283d5a4ebe482597a4c934a17f39665ff31
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
$ docker pull composer@sha256:dc762de077b409c57a93053b4c9303c9df0013dc2e0cf8caec8e7a98304d098a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74873742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8389298d00edb2bcb0b6243707d46a3c8ab03c563603743a6a5243275044d0ea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
ENV COMPOSER_VERSION=2.2.24
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4026d1cc5245f59e156bffd596323974be67dd48771842c57ace1b9fcb840`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 5.6 MB (5583566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca19f9a3dd1a82729217796a0e8ef626bd25c881db51316ae1d7b6baca3c979`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d429435d57d0d3420a2bb847cb1a04a76483e18d14ae4486b653e998810c2dc8`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22359169dee3cb23309dde8b4845f0a26d5ced82572690f0ec5de9aa5c37df6b`  
		Last Modified: Thu, 21 Nov 2024 18:00:31 GMT  
		Size: 13.6 MB (13572755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60636de7ac448f3bfc52c2d3f3fbdd7e572b65b45a980647e217005c89f46ddd`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6574e97188f3a55184dd55cbc3377b5b1826fe8ac69257fc044d8d1826cf62a`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 20.8 MB (20763608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0db01ff42c14dc52ac7bd7aad09e0a0e2b0050a0ad2796a55eb92246ce39d2`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e12f7079c7bc22fa3df852b4eebe6e7b01a834b3924a0f365f1b0f3437b7eab`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 19.7 KB (19661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a51e94714c8707792f4fe23ad049a8c12d8c33818884fed28112530e7679ee`  
		Last Modified: Thu, 21 Nov 2024 18:10:43 GMT  
		Size: 30.4 MB (30368546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a05dba902617c5f7d56484efb2943e96ba560201b89894283f4d43629c97e65`  
		Last Modified: Thu, 21 Nov 2024 18:10:42 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134c7a64e8423974fb4f1b7984b0947b14c8c0098961eaaa880f6113b57ee2e4`  
		Last Modified: Thu, 21 Nov 2024 18:10:42 GMT  
		Size: 936.8 KB (936842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab1b7d6b2a7b5eaffc0c95c278d0bb7c18b20204b2b5eae520c71c7090c6f4a`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530ddf2e2ea7376256a341344b97cc0f2b1396e7f8f5a1296888287563aa6963`  
		Last Modified: Thu, 21 Nov 2024 18:10:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:427486cb9a9cc4770140df4a865ac9bdcbebbddca4187b8afbfe43e421e51b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24a49d1b9b079f6b20225dfeec273cf989e2a364f038c07efdf39d1d3b7da57`

```dockerfile
```

-	Layers:
	-	`sha256:5fbc3c664e2d90fbc69a9f92c84bcad5b769bceb74bbc163a02db1af37d5a02b`  
		Last Modified: Thu, 21 Nov 2024 18:10:42 GMT  
		Size: 2.1 MB (2147493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4f6ce00b6b55144638e0c8b483672b5fb6e6a070f49ad3661bffd5bdd73c46e`  
		Last Modified: Thu, 21 Nov 2024 18:10:42 GMT  
		Size: 30.7 KB (30652 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v6

```console
$ docker pull composer@sha256:5d3fddde44dd2cd61f0d23563881c665ebc0367cac5324307be2ff2668c9d71c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97eb5a11a9dcc19751c3533f8d6ac939b83e0370fa4e1cbaed86ee4b9d7571ba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
ENV COMPOSER_VERSION=2.2.24
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
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdae56950198dea1248e6f62d7e9ef311c976d55790449240dfa46ad43351f7`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 5.2 MB (5236002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773d98c98ade13dc692eaf9700be32a03220033d99905be410eda923ce054fb9`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ae964d3deb57dca49dadfc5c487d64a372e3df3db6ef51b58087c318beb33d`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851605dfb3d928a53fef3860db97edb0f94316d382df472a9f36d31603ae85dc`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 13.6 MB (13572750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb476219577608ba4633ce4f2bf10a95d8fd1bd1bb56c2fb972587e5207cb3f`  
		Last Modified: Thu, 21 Nov 2024 17:58:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698c845cc5fd3760e20d315377bdca792a2b899c35f1288b5ddf2bf66c3e10d4`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 19.0 MB (19027128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7c3d46b7180237d2a402261f2cb181901e0149fed38e5a97d2214f64ba90ac`  
		Last Modified: Thu, 21 Nov 2024 17:58:04 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72176ade970c8f4af9d251ca5d0fc1aefd6e0fa47866d9d792bf9e85a4ac16c`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 19.4 KB (19437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487dce5effb993971148992fe8918fe413df14e91c1a17c2d7a26c254d6a7b29`  
		Last Modified: Thu, 21 Nov 2024 19:21:58 GMT  
		Size: 29.2 MB (29169296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812056dc604d2f3d588dcb3b1441239d4f3a938f21cabe40a0c26a26245a6f23`  
		Last Modified: Thu, 21 Nov 2024 19:21:57 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7497c4d4ec772fa3b0fe4c24787719f3009da03a55d3e2519d0318541a2b33`  
		Last Modified: Thu, 21 Nov 2024 19:21:57 GMT  
		Size: 936.6 KB (936627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfd7c969e59b509cbb25d238f775b14f1f6de06c8c50f7b1c7b89909f9e76f3`  
		Last Modified: Thu, 14 Nov 2024 17:27:32 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f195f1c45af65d274b33527994a259f4b7a050670692edb404032c41ff63f11`  
		Last Modified: Thu, 21 Nov 2024 19:21:57 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:b454fc6978324f0e883d0bb957b0068c82dae159d4d129ec6ac6db2d34a44707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76189ed6a5eecb149a77520fe8706d4c4907ededeb6abb684ee878077978e24`

```dockerfile
```

-	Layers:
	-	`sha256:adffb95fbb5eedc669bf68d35ba3f4f66ea43d23b83cf287e0329552b301a55d`  
		Last Modified: Thu, 21 Nov 2024 19:21:57 GMT  
		Size: 30.5 KB (30533 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v7

```console
$ docker pull composer@sha256:f8e498f2e26f567fcb79922e01ba79a45e49e7d9262646c2ecaecccc443a73d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69228978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1e7b630fcfdc911cb231185a630a3faf1d8ddc258a1ce889ae74b8968bc620`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
ENV COMPOSER_VERSION=2.2.24
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
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2878563f55378e5cb0d2e6fc051acec0bad59706b4c55d991502e489d45f15b9`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 4.9 MB (4894482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1da599409a1b1b855c6d69889b78470128711398dd127ceb61f803c590c9c39`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fec221aedc472ddb77d24345957296ec946aab0b124953af99b1b103ca464d6`  
		Last Modified: Tue, 12 Nov 2024 03:55:37 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46d0dd0a80f3bfa93fe376e12f14d3cf1bf7c86c9c039106b233b8584ec9aac`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 13.6 MB (13572743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d138265234b8809a223e845ff20a559fa757eebafc98f9e9bf724fe8e7dc8b6c`  
		Last Modified: Thu, 21 Nov 2024 18:28:27 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b99f01624e25d17567cb4316e05b197890eaf269e39da90cf62573fc75f8dab`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 17.9 MB (17928178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc46c2ae1e666fefa71dcffefd35978d65be61640f7a3dae1293e1c413955d01`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4995aff739b8938a9a1f51923b6e970cc4d974c131fb8f2f8be37bd64c89bf1e`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 19.5 KB (19454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8371af98339513b427681640d9952ffda9674c0a7837c1f5e1ca4b91fa04e1`  
		Last Modified: Thu, 21 Nov 2024 22:48:27 GMT  
		Size: 28.8 MB (28798173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7861e6ac85a5be9e606f1a0b1ed4b0869e26847132c16ba05c326da3b82f1fb`  
		Last Modified: Thu, 21 Nov 2024 22:48:26 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493012c5a6547efbc494430af25dc80173bdee3d4f60c42496ec50457df6ee8e`  
		Last Modified: Thu, 21 Nov 2024 22:48:26 GMT  
		Size: 915.6 KB (915587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4392e1df0c627db8659fec8b11584d88798ed80206abb5707f07ac537fdec26f`  
		Last Modified: Thu, 21 Nov 2024 22:48:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a877678fb5fdddb712b0d3f125aa9c71483cd9a72e87d956cbc6d3c1a0d43003`  
		Last Modified: Thu, 21 Nov 2024 22:48:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:93a5382e61fae1a22af7feaf5926451001d52b6ee69b48f3cd02656650c8905f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be5cfbbb520154ede402a8b2bce4eeb128b5983b98576b83b1be1f431273049`

```dockerfile
```

-	Layers:
	-	`sha256:6e70796a377912ba45dc355bf19d5f930f74024d0f0a96d058461b113b885846`  
		Last Modified: Thu, 21 Nov 2024 22:48:26 GMT  
		Size: 2.1 MB (2147806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94eb33295a673f22586e4880fb2c8b1bc5a7d9074c7d77a3a4feb1331ccb44f8`  
		Last Modified: Thu, 21 Nov 2024 22:48:26 GMT  
		Size: 30.7 KB (30748 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:6a7a0690deae00e521fbdc9abc37d053db84f33c37f60bbd2a76542f81a4ae20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75938195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c09cf1b1acc463d7d133b00d9026e35b99fb7074d7631b64aebff8f07d60a45`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
ENV COMPOSER_VERSION=2.2.24
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8484336630ebb870b45fd46b300831768da17cae91aa6a615fe97d849bf7d9`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 6.0 MB (6047382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f0bf50f7dfd6864235893d3a770f2748c511f29a319b959cd61ab88719f191`  
		Last Modified: Thu, 21 Nov 2024 18:25:40 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4094551f517548ba326fd9610784089231cb5fe7b32fb0fd484b4ef62a06ec4e`  
		Last Modified: Thu, 21 Nov 2024 18:25:40 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f3a19954028229594dc87f84401ff6bb04343f60f6850d3ffd56376584e127`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 13.6 MB (13572746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cec773ac8fce78f9e43c85101520fcc9a1dfd15d5ae6b0086a53ed446c44e83`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c49e3ab1eba1efe295397f466820586f5b4c820bf03494c07afc622cb0d4b80`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 20.4 MB (20379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f558eac651d11a18dc2c9e83c547cfe4241937c5dc84ca0e2f00d0fcc438eb`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec25731eb581dc3064873d8a03e05f5820ff6c09af884fce4b25f79b77d6f34e`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 19.4 KB (19426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7fe1a5fdee0abebec8c80d0770c46acf11edac729c491803ec919a7373c8c`  
		Last Modified: Thu, 21 Nov 2024 22:17:56 GMT  
		Size: 30.9 MB (30879490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0fda769fb77685ab9ff0bd8069d8c4670c1a85af4283162afa7524a8124d45`  
		Last Modified: Thu, 21 Nov 2024 22:17:55 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f33051432a42a11aba731651d6de55d39d9cdd3cc6a9ee26fe125092bbab68`  
		Last Modified: Thu, 21 Nov 2024 22:17:55 GMT  
		Size: 947.5 KB (947547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98c7eaba8d2c0a247642ab1c9e0449c3cc021987330f4a78cf55ae835d29b8e`  
		Last Modified: Thu, 21 Nov 2024 22:17:55 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e561633f2696555e9d601463322eacf04773b731ea444ab8e0e6160cc0418c1a`  
		Last Modified: Thu, 21 Nov 2024 22:17:56 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:529a741ae63ece5d98a696c6b61c47a843e189793224c089e0670d874e4dcca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3aecefe174e213dcaed558732318f846414c8383d7f9393ec4bbc8ad995df3a`

```dockerfile
```

-	Layers:
	-	`sha256:c0f692a03747088c081f0800650c9c02867608bdad123c81327dd94eb8f36d70`  
		Last Modified: Thu, 21 Nov 2024 22:17:55 GMT  
		Size: 2.1 MB (2147632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4daafc04a8ce3d201a57dff3ff09817354cc6c17883846c105b4a5e84266d191`  
		Last Modified: Thu, 21 Nov 2024 22:17:54 GMT  
		Size: 30.8 KB (30776 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; 386

```console
$ docker pull composer@sha256:26ecdb5228c9c79d03ae95862c22f997a5431202e354672b511b39d06256f0ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56040857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b97a1ae6ba8ad901380c00b3583a29d2db0eda0d322697b1fa14a259d64055`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
ENV COMPOSER_VERSION=2.2.24
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
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e11d2a2a48dac61e9ac66af5a5b296591c6a200cf9944fd4df55e48749cce57`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 5.5 MB (5468335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3858fed08c63431ed26286b0317883b23277e3ce014a38a3ca7392c05f0e669a`  
		Last Modified: Thu, 21 Nov 2024 18:00:49 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d4c27ab44c7e13de299ad07b09e18b7c98dee3c34fbee400448997573becdb`  
		Last Modified: Thu, 21 Nov 2024 18:00:49 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b25b38e344c1ca4be9ca4235d6cde628e170971af37a03e30f897cf5a758c`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 13.6 MB (13572753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1764d36b8a53c825b53731114444100b7e1bf8a517ab182b4dab438333bee585`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6444425964f24bb27686445f1e394678dae6d912247a4b8f26e4d7b57e90f54`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 21.3 MB (21300265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2465ec415dcb964fc8b6deb3edeeddfb60a77336ebafdeeff9780a230562a2`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b021291a02d8b49460ff1ff13393725cf6e1616dbb1b2a1ef9c7a69fdeab5b4`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 19.6 KB (19644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8aabe33271ab76e9f0a0e14600b67129c22b6376b9ac5691140b583e58214`  
		Last Modified: Thu, 21 Nov 2024 18:10:39 GMT  
		Size: 11.3 MB (11281350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91db55eda861b506210850850e90775ccb8a5505fd86fc292beade07dfeb2c7`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c53d73674dfa5d4b800403e9b1074300aa872923a0c9a430947bb23e7e169c`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 924.4 KB (924424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84b9390ed421034bdf6edeb19bc83a8d787f4901717254b650b67efe6ca93f2`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb0c74b28b1a5cf47e26e8fec2c840aca547b64a308d1f713a87c93c3561567`  
		Last Modified: Thu, 21 Nov 2024 18:10:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:5a2d48203435ea9b05d1087dd9768863722f2a77305e6f836cb4b74c9d66e6e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.8 KB (451790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b9ac7e897bad079a57c6656ba0079217b3d28729d975aa9eaf191ba42e18ed`

```dockerfile
```

-	Layers:
	-	`sha256:9b26e2ba6aa29a86cf02b0a9b2a3c5457147c9cdd03e915b3b132b74977f595f`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 421.2 KB (421167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6f68dfe539c0913cdec1a101a80c7ce9850e0ce82e81fcca23972e41de1fdae`  
		Last Modified: Thu, 21 Nov 2024 18:10:37 GMT  
		Size: 30.6 KB (30623 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; ppc64le

```console
$ docker pull composer@sha256:273ef0b791c27b94c856cdf8854312e8f1fee0a8533ea12299bd033053aee9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76814960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89dedefde6c35d833333272a0f72fd082f233bbc63f2260b86fee1fbf2a05fc4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
ENV COMPOSER_VERSION=2.2.24
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
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2473147d3bc2923a26c8ba560c425ef2674fbae2edbc29833bb5790c2c94db2`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 5.6 MB (5572572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53975073457162c05af82756884811d86cf52d05953b0589749a216a80864431`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58037573bd03f9687676a3398cb715ac628a3bc280f63aa990e8171ef59ce1c9`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f80183c138cedf9dc24420caf7f9769369bf61c8db0eb09729c4303c31ba1b`  
		Last Modified: Thu, 21 Nov 2024 18:14:28 GMT  
		Size: 13.6 MB (13572757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1746563bd5a8883ee2e1758e12423a999df46412bbeb663f9f774dc595e96ed`  
		Last Modified: Thu, 21 Nov 2024 18:14:27 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3428ebe5f2568169c292765c92b0cc55c0ef85fc46ab1c4d0b60b2d86970b4b3`  
		Last Modified: Thu, 21 Nov 2024 18:14:29 GMT  
		Size: 21.7 MB (21712721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f8424c24e908ec0192f8ff40322e44264734608539de7427be91c3398884dc`  
		Last Modified: Thu, 21 Nov 2024 18:14:27 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef3b5629726f19111a47ee6dc86f22265d0002270ef68da5bb572a2fa8a6d04`  
		Last Modified: Thu, 21 Nov 2024 18:14:28 GMT  
		Size: 19.4 KB (19424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf7d67a2a72f10bea3ee74b2250affb6d2de6aac3751149e9003e6b4ff24a2e`  
		Last Modified: Thu, 21 Nov 2024 21:22:37 GMT  
		Size: 31.4 MB (31402451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011cd0419150962df2f83f6c5e96043ca7df1ddb5a812e226d6f2b98814c7fc0`  
		Last Modified: Thu, 21 Nov 2024 21:22:35 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f739c523c65801d9bf3a3512b64f2a819fb4533b819d382f1b5236a2ab0fb79`  
		Last Modified: Thu, 21 Nov 2024 21:22:36 GMT  
		Size: 957.7 KB (957693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ee41244fae528c8ba994c3f0c062d5063890d34b2b13f37417073f4e4abb20`  
		Last Modified: Thu, 21 Nov 2024 21:22:36 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb5d18c4f4e6134f2c4406383a1debea61cefc8dd4a5da7a59075c1ada07832`  
		Last Modified: Thu, 21 Nov 2024 21:22:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:5aa5e9f65405cd9a12eb9dd2b99fe48646e40b7aefdb630ddc0e0f75997e7a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80f49cfb840ebf4f850dba9467d0efb1d6b82b91f1586b93a7df1f84500413b`

```dockerfile
```

-	Layers:
	-	`sha256:d07b44100f7897664a442a7aff9c544144d8bc29a038de7cba4329f3d908f62b`  
		Last Modified: Thu, 21 Nov 2024 21:22:36 GMT  
		Size: 2.1 MB (2146042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:917db0d38ca1fa32a3425dd85715d616780fa2374048dd32b9c01757c2601999`  
		Last Modified: Thu, 21 Nov 2024 21:22:35 GMT  
		Size: 30.7 KB (30696 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; riscv64

```console
$ docker pull composer@sha256:3ddd4f307e73eb3bcde94c20848064553bd21d845bfd4b7ff551d8f352aad3bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69829962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10f76d711de731796de0a4a395f77b1447f8431b1d58b8fdb2c3cce859ee3fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
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
ENV COMPOSER_VERSION=2.2.24
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
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8ca85c9d20c6f76d0a8087ac3a4ddd6a1e40652d189dc8dad7ca6b0737c4b0`  
		Last Modified: Tue, 12 Nov 2024 06:14:49 GMT  
		Size: 5.4 MB (5382174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d2dfe107b4bddcc389bedcee9ca3fc81f02dc0799e313c21f307ddb454b4dc`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df7310166e795cb48e721a885b92af688db981613ad6597943011293aca738c`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626cc5aa152e22cd453ede74c922b963a3bc8a4bcf66d8a4763c977a36db9bbf`  
		Last Modified: Tue, 12 Nov 2024 11:38:11 GMT  
		Size: 12.5 MB (12504597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e68d6f9ff3ad2f5f92d5d2e1da7c8e8e8c7acf26714c65fb1634379b0ceabea`  
		Last Modified: Tue, 12 Nov 2024 11:38:08 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7ef4ac959dd31d8a66fcf270291f1312424b277d8adec2eded58a835d3130c`  
		Last Modified: Tue, 12 Nov 2024 11:38:11 GMT  
		Size: 16.8 MB (16791439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f9910ad73e6186422edca968a56743133f52309ae7e8fbfaeba5689ec14ce1`  
		Last Modified: Tue, 12 Nov 2024 11:38:08 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cccb83ba6c8bd3926d00dba2c6475d1639c61ec7b4dc48a094f44e9ef2d363f`  
		Last Modified: Tue, 12 Nov 2024 11:38:10 GMT  
		Size: 19.4 KB (19444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1184794faa4cb72388841b6ca5edd801726298f1bc7a901384a6611a072b84d`  
		Last Modified: Wed, 13 Nov 2024 13:17:47 GMT  
		Size: 30.8 MB (30811150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0835e0d761497dfe92dfd2f01937792ca5c678bba375a232324b9fbb0ba5120`  
		Last Modified: Wed, 13 Nov 2024 13:17:42 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c554724d42fde604b2c035bae323f605a4cc0c9636d7bdfcbd0f7314063855c`  
		Last Modified: Thu, 14 Nov 2024 17:31:54 GMT  
		Size: 944.8 KB (944794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f996300435f6471be064e050bb5d21dbc2a9d7e12bfb48c5581ffb7091600e`  
		Last Modified: Thu, 14 Nov 2024 17:31:53 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd23ffb62d5751d22ddc4bfc9f5abe311dd9d793f5b461d065fb0f50fe4e9d2e`  
		Last Modified: Thu, 14 Nov 2024 17:31:53 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:2d88e8f1faac4e0669dfc54e81e569dd1591b97c410c04f461aed8935e8e7a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf3466f3664bd0ac8832b3717e606b2c1acbb35c1ffff936f34501c3ffabfb5`

```dockerfile
```

-	Layers:
	-	`sha256:ef84f869596117d88e713b7a48ac2a4701961f87f93ecca1a1616ec550b671f1`  
		Last Modified: Thu, 14 Nov 2024 17:31:53 GMT  
		Size: 2.1 MB (2145659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e828aa65c76f40f9e116367e305f3d9196b226f3824fe9e59c2ec1836e46489e`  
		Last Modified: Thu, 14 Nov 2024 17:31:53 GMT  
		Size: 30.7 KB (30705 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; s390x

```console
$ docker pull composer@sha256:0b741a73b3c522adafb8efb5dd9991126e70a4192f5e2055ccb7f1db027117f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76135045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffebc5d710dc20bfb62fe4a32c3df2b531aed5feecb67ac1d8f2d058dcf31485`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
ENV COMPOSER_VERSION=2.2.24
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
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26915a92034b18e2de9232a415d1ad92dc1c7a9f9e2b5bb9c590ce4c503ab73e`  
		Last Modified: Tue, 12 Nov 2024 03:39:27 GMT  
		Size: 5.5 MB (5532119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4041b6d620078267a8ee6dd6b9c31735d82dee5f22aa96467865a8134d616c`  
		Last Modified: Tue, 12 Nov 2024 03:39:26 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5555efb309fc5275c2fd44eabaaf4ca859f01b510ef24cbad6009d7ed6dc4696`  
		Last Modified: Tue, 12 Nov 2024 03:39:26 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ebcb70bd65f646a0a9f4f475ec50ab3b189c26c5453f7261bc927c566c16f4`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 13.6 MB (13572754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1fe669f736130225879d8f3a94b1a2dc84c8a542232c1010d5c0efdfb490ab`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ebb202afe7221a69abb8b0e5dd9a734085f863f2a450dd0794f4e1c6bc5189`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 21.3 MB (21250100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7a60154e6bcac48ec5bae22b14f7b46c6200a532944883ccb70d97a5f9ff15`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76035e400728cb3a6c7bd01204127072929a705a4be9f5ab31588ec5dce5bd70`  
		Last Modified: Thu, 21 Nov 2024 18:24:27 GMT  
		Size: 19.4 KB (19435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391e13c55cb9dd9b3adaa2c815b5a344bfd110a0afc12b82e71ba8af9327a7a3`  
		Last Modified: Thu, 21 Nov 2024 21:24:03 GMT  
		Size: 31.3 MB (31338617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d1aea81c97d878724863520afce631476bbf2f86f4eaf2a4b781b5d4f855ba`  
		Last Modified: Thu, 21 Nov 2024 21:24:02 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4b1710f0705434f4bdcfd8d31140ef64468bb215062f4232b1b6b2b71deb62`  
		Last Modified: Thu, 21 Nov 2024 21:24:03 GMT  
		Size: 955.5 KB (955542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2795ba63978bfd04dfd9f48b1785eee03271dc472997f51d05ef1849ec33eda`  
		Last Modified: Thu, 21 Nov 2024 21:24:03 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda486a2686c7739a4087ac185e265c1bbe289f9a216ae45f54d2fa1d70b166b`  
		Last Modified: Thu, 21 Nov 2024 21:24:03 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:c2dbb513828951cee5931de5174febf1f6f07891e09131182da48b5269dacca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e69f8a7720a8658448cb346da5858583df53531e480d6571ecfe8a889bf8acc4`

```dockerfile
```

-	Layers:
	-	`sha256:434bb7bdf557e614bb7a8c41785a7d34764404cbc3e97f086f9765241b008839`  
		Last Modified: Thu, 21 Nov 2024 21:24:02 GMT  
		Size: 2.1 MB (2145444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3942678f500c80f758b086ace61ac759e021e60b71716fa73621828abae3ac09`  
		Last Modified: Thu, 21 Nov 2024 21:24:02 GMT  
		Size: 30.7 KB (30654 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2.24`

```console
$ docker pull composer@sha256:866ce87175721248614af82d38ec0283d5a4ebe482597a4c934a17f39665ff31
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

### `composer:2.2.24` - linux; amd64

```console
$ docker pull composer@sha256:dc762de077b409c57a93053b4c9303c9df0013dc2e0cf8caec8e7a98304d098a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74873742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8389298d00edb2bcb0b6243707d46a3c8ab03c563603743a6a5243275044d0ea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
ENV COMPOSER_VERSION=2.2.24
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4026d1cc5245f59e156bffd596323974be67dd48771842c57ace1b9fcb840`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 5.6 MB (5583566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca19f9a3dd1a82729217796a0e8ef626bd25c881db51316ae1d7b6baca3c979`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d429435d57d0d3420a2bb847cb1a04a76483e18d14ae4486b653e998810c2dc8`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22359169dee3cb23309dde8b4845f0a26d5ced82572690f0ec5de9aa5c37df6b`  
		Last Modified: Thu, 21 Nov 2024 18:00:31 GMT  
		Size: 13.6 MB (13572755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60636de7ac448f3bfc52c2d3f3fbdd7e572b65b45a980647e217005c89f46ddd`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6574e97188f3a55184dd55cbc3377b5b1826fe8ac69257fc044d8d1826cf62a`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 20.8 MB (20763608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0db01ff42c14dc52ac7bd7aad09e0a0e2b0050a0ad2796a55eb92246ce39d2`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e12f7079c7bc22fa3df852b4eebe6e7b01a834b3924a0f365f1b0f3437b7eab`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 19.7 KB (19661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a51e94714c8707792f4fe23ad049a8c12d8c33818884fed28112530e7679ee`  
		Last Modified: Thu, 21 Nov 2024 18:10:43 GMT  
		Size: 30.4 MB (30368546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a05dba902617c5f7d56484efb2943e96ba560201b89894283f4d43629c97e65`  
		Last Modified: Thu, 21 Nov 2024 18:10:42 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134c7a64e8423974fb4f1b7984b0947b14c8c0098961eaaa880f6113b57ee2e4`  
		Last Modified: Thu, 21 Nov 2024 18:10:42 GMT  
		Size: 936.8 KB (936842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab1b7d6b2a7b5eaffc0c95c278d0bb7c18b20204b2b5eae520c71c7090c6f4a`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530ddf2e2ea7376256a341344b97cc0f2b1396e7f8f5a1296888287563aa6963`  
		Last Modified: Thu, 21 Nov 2024 18:10:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.24` - unknown; unknown

```console
$ docker pull composer@sha256:427486cb9a9cc4770140df4a865ac9bdcbebbddca4187b8afbfe43e421e51b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24a49d1b9b079f6b20225dfeec273cf989e2a364f038c07efdf39d1d3b7da57`

```dockerfile
```

-	Layers:
	-	`sha256:5fbc3c664e2d90fbc69a9f92c84bcad5b769bceb74bbc163a02db1af37d5a02b`  
		Last Modified: Thu, 21 Nov 2024 18:10:42 GMT  
		Size: 2.1 MB (2147493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4f6ce00b6b55144638e0c8b483672b5fb6e6a070f49ad3661bffd5bdd73c46e`  
		Last Modified: Thu, 21 Nov 2024 18:10:42 GMT  
		Size: 30.7 KB (30652 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.24` - linux; arm variant v6

```console
$ docker pull composer@sha256:5d3fddde44dd2cd61f0d23563881c665ebc0367cac5324307be2ff2668c9d71c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97eb5a11a9dcc19751c3533f8d6ac939b83e0370fa4e1cbaed86ee4b9d7571ba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
ENV COMPOSER_VERSION=2.2.24
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
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdae56950198dea1248e6f62d7e9ef311c976d55790449240dfa46ad43351f7`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 5.2 MB (5236002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773d98c98ade13dc692eaf9700be32a03220033d99905be410eda923ce054fb9`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ae964d3deb57dca49dadfc5c487d64a372e3df3db6ef51b58087c318beb33d`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851605dfb3d928a53fef3860db97edb0f94316d382df472a9f36d31603ae85dc`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 13.6 MB (13572750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb476219577608ba4633ce4f2bf10a95d8fd1bd1bb56c2fb972587e5207cb3f`  
		Last Modified: Thu, 21 Nov 2024 17:58:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698c845cc5fd3760e20d315377bdca792a2b899c35f1288b5ddf2bf66c3e10d4`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 19.0 MB (19027128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7c3d46b7180237d2a402261f2cb181901e0149fed38e5a97d2214f64ba90ac`  
		Last Modified: Thu, 21 Nov 2024 17:58:04 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72176ade970c8f4af9d251ca5d0fc1aefd6e0fa47866d9d792bf9e85a4ac16c`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 19.4 KB (19437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487dce5effb993971148992fe8918fe413df14e91c1a17c2d7a26c254d6a7b29`  
		Last Modified: Thu, 21 Nov 2024 19:21:58 GMT  
		Size: 29.2 MB (29169296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812056dc604d2f3d588dcb3b1441239d4f3a938f21cabe40a0c26a26245a6f23`  
		Last Modified: Thu, 21 Nov 2024 19:21:57 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7497c4d4ec772fa3b0fe4c24787719f3009da03a55d3e2519d0318541a2b33`  
		Last Modified: Thu, 21 Nov 2024 19:21:57 GMT  
		Size: 936.6 KB (936627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfd7c969e59b509cbb25d238f775b14f1f6de06c8c50f7b1c7b89909f9e76f3`  
		Last Modified: Thu, 14 Nov 2024 17:27:32 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f195f1c45af65d274b33527994a259f4b7a050670692edb404032c41ff63f11`  
		Last Modified: Thu, 21 Nov 2024 19:21:57 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.24` - unknown; unknown

```console
$ docker pull composer@sha256:b454fc6978324f0e883d0bb957b0068c82dae159d4d129ec6ac6db2d34a44707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76189ed6a5eecb149a77520fe8706d4c4907ededeb6abb684ee878077978e24`

```dockerfile
```

-	Layers:
	-	`sha256:adffb95fbb5eedc669bf68d35ba3f4f66ea43d23b83cf287e0329552b301a55d`  
		Last Modified: Thu, 21 Nov 2024 19:21:57 GMT  
		Size: 30.5 KB (30533 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.24` - linux; arm variant v7

```console
$ docker pull composer@sha256:f8e498f2e26f567fcb79922e01ba79a45e49e7d9262646c2ecaecccc443a73d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69228978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1e7b630fcfdc911cb231185a630a3faf1d8ddc258a1ce889ae74b8968bc620`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
ENV COMPOSER_VERSION=2.2.24
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
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2878563f55378e5cb0d2e6fc051acec0bad59706b4c55d991502e489d45f15b9`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 4.9 MB (4894482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1da599409a1b1b855c6d69889b78470128711398dd127ceb61f803c590c9c39`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fec221aedc472ddb77d24345957296ec946aab0b124953af99b1b103ca464d6`  
		Last Modified: Tue, 12 Nov 2024 03:55:37 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46d0dd0a80f3bfa93fe376e12f14d3cf1bf7c86c9c039106b233b8584ec9aac`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 13.6 MB (13572743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d138265234b8809a223e845ff20a559fa757eebafc98f9e9bf724fe8e7dc8b6c`  
		Last Modified: Thu, 21 Nov 2024 18:28:27 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b99f01624e25d17567cb4316e05b197890eaf269e39da90cf62573fc75f8dab`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 17.9 MB (17928178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc46c2ae1e666fefa71dcffefd35978d65be61640f7a3dae1293e1c413955d01`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4995aff739b8938a9a1f51923b6e970cc4d974c131fb8f2f8be37bd64c89bf1e`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 19.5 KB (19454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8371af98339513b427681640d9952ffda9674c0a7837c1f5e1ca4b91fa04e1`  
		Last Modified: Thu, 21 Nov 2024 22:48:27 GMT  
		Size: 28.8 MB (28798173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7861e6ac85a5be9e606f1a0b1ed4b0869e26847132c16ba05c326da3b82f1fb`  
		Last Modified: Thu, 21 Nov 2024 22:48:26 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493012c5a6547efbc494430af25dc80173bdee3d4f60c42496ec50457df6ee8e`  
		Last Modified: Thu, 21 Nov 2024 22:48:26 GMT  
		Size: 915.6 KB (915587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4392e1df0c627db8659fec8b11584d88798ed80206abb5707f07ac537fdec26f`  
		Last Modified: Thu, 21 Nov 2024 22:48:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a877678fb5fdddb712b0d3f125aa9c71483cd9a72e87d956cbc6d3c1a0d43003`  
		Last Modified: Thu, 21 Nov 2024 22:48:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.24` - unknown; unknown

```console
$ docker pull composer@sha256:93a5382e61fae1a22af7feaf5926451001d52b6ee69b48f3cd02656650c8905f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be5cfbbb520154ede402a8b2bce4eeb128b5983b98576b83b1be1f431273049`

```dockerfile
```

-	Layers:
	-	`sha256:6e70796a377912ba45dc355bf19d5f930f74024d0f0a96d058461b113b885846`  
		Last Modified: Thu, 21 Nov 2024 22:48:26 GMT  
		Size: 2.1 MB (2147806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94eb33295a673f22586e4880fb2c8b1bc5a7d9074c7d77a3a4feb1331ccb44f8`  
		Last Modified: Thu, 21 Nov 2024 22:48:26 GMT  
		Size: 30.7 KB (30748 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.24` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:6a7a0690deae00e521fbdc9abc37d053db84f33c37f60bbd2a76542f81a4ae20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75938195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c09cf1b1acc463d7d133b00d9026e35b99fb7074d7631b64aebff8f07d60a45`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
ENV COMPOSER_VERSION=2.2.24
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8484336630ebb870b45fd46b300831768da17cae91aa6a615fe97d849bf7d9`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 6.0 MB (6047382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f0bf50f7dfd6864235893d3a770f2748c511f29a319b959cd61ab88719f191`  
		Last Modified: Thu, 21 Nov 2024 18:25:40 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4094551f517548ba326fd9610784089231cb5fe7b32fb0fd484b4ef62a06ec4e`  
		Last Modified: Thu, 21 Nov 2024 18:25:40 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f3a19954028229594dc87f84401ff6bb04343f60f6850d3ffd56376584e127`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 13.6 MB (13572746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cec773ac8fce78f9e43c85101520fcc9a1dfd15d5ae6b0086a53ed446c44e83`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c49e3ab1eba1efe295397f466820586f5b4c820bf03494c07afc622cb0d4b80`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 20.4 MB (20379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f558eac651d11a18dc2c9e83c547cfe4241937c5dc84ca0e2f00d0fcc438eb`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec25731eb581dc3064873d8a03e05f5820ff6c09af884fce4b25f79b77d6f34e`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 19.4 KB (19426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7fe1a5fdee0abebec8c80d0770c46acf11edac729c491803ec919a7373c8c`  
		Last Modified: Thu, 21 Nov 2024 22:17:56 GMT  
		Size: 30.9 MB (30879490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0fda769fb77685ab9ff0bd8069d8c4670c1a85af4283162afa7524a8124d45`  
		Last Modified: Thu, 21 Nov 2024 22:17:55 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f33051432a42a11aba731651d6de55d39d9cdd3cc6a9ee26fe125092bbab68`  
		Last Modified: Thu, 21 Nov 2024 22:17:55 GMT  
		Size: 947.5 KB (947547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98c7eaba8d2c0a247642ab1c9e0449c3cc021987330f4a78cf55ae835d29b8e`  
		Last Modified: Thu, 21 Nov 2024 22:17:55 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e561633f2696555e9d601463322eacf04773b731ea444ab8e0e6160cc0418c1a`  
		Last Modified: Thu, 21 Nov 2024 22:17:56 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.24` - unknown; unknown

```console
$ docker pull composer@sha256:529a741ae63ece5d98a696c6b61c47a843e189793224c089e0670d874e4dcca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3aecefe174e213dcaed558732318f846414c8383d7f9393ec4bbc8ad995df3a`

```dockerfile
```

-	Layers:
	-	`sha256:c0f692a03747088c081f0800650c9c02867608bdad123c81327dd94eb8f36d70`  
		Last Modified: Thu, 21 Nov 2024 22:17:55 GMT  
		Size: 2.1 MB (2147632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4daafc04a8ce3d201a57dff3ff09817354cc6c17883846c105b4a5e84266d191`  
		Last Modified: Thu, 21 Nov 2024 22:17:54 GMT  
		Size: 30.8 KB (30776 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.24` - linux; 386

```console
$ docker pull composer@sha256:26ecdb5228c9c79d03ae95862c22f997a5431202e354672b511b39d06256f0ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56040857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b97a1ae6ba8ad901380c00b3583a29d2db0eda0d322697b1fa14a259d64055`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
ENV COMPOSER_VERSION=2.2.24
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
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e11d2a2a48dac61e9ac66af5a5b296591c6a200cf9944fd4df55e48749cce57`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 5.5 MB (5468335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3858fed08c63431ed26286b0317883b23277e3ce014a38a3ca7392c05f0e669a`  
		Last Modified: Thu, 21 Nov 2024 18:00:49 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d4c27ab44c7e13de299ad07b09e18b7c98dee3c34fbee400448997573becdb`  
		Last Modified: Thu, 21 Nov 2024 18:00:49 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b25b38e344c1ca4be9ca4235d6cde628e170971af37a03e30f897cf5a758c`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 13.6 MB (13572753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1764d36b8a53c825b53731114444100b7e1bf8a517ab182b4dab438333bee585`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6444425964f24bb27686445f1e394678dae6d912247a4b8f26e4d7b57e90f54`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 21.3 MB (21300265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2465ec415dcb964fc8b6deb3edeeddfb60a77336ebafdeeff9780a230562a2`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b021291a02d8b49460ff1ff13393725cf6e1616dbb1b2a1ef9c7a69fdeab5b4`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 19.6 KB (19644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8aabe33271ab76e9f0a0e14600b67129c22b6376b9ac5691140b583e58214`  
		Last Modified: Thu, 21 Nov 2024 18:10:39 GMT  
		Size: 11.3 MB (11281350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91db55eda861b506210850850e90775ccb8a5505fd86fc292beade07dfeb2c7`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c53d73674dfa5d4b800403e9b1074300aa872923a0c9a430947bb23e7e169c`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 924.4 KB (924424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84b9390ed421034bdf6edeb19bc83a8d787f4901717254b650b67efe6ca93f2`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb0c74b28b1a5cf47e26e8fec2c840aca547b64a308d1f713a87c93c3561567`  
		Last Modified: Thu, 21 Nov 2024 18:10:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.24` - unknown; unknown

```console
$ docker pull composer@sha256:5a2d48203435ea9b05d1087dd9768863722f2a77305e6f836cb4b74c9d66e6e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.8 KB (451790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b9ac7e897bad079a57c6656ba0079217b3d28729d975aa9eaf191ba42e18ed`

```dockerfile
```

-	Layers:
	-	`sha256:9b26e2ba6aa29a86cf02b0a9b2a3c5457147c9cdd03e915b3b132b74977f595f`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 421.2 KB (421167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6f68dfe539c0913cdec1a101a80c7ce9850e0ce82e81fcca23972e41de1fdae`  
		Last Modified: Thu, 21 Nov 2024 18:10:37 GMT  
		Size: 30.6 KB (30623 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.24` - linux; ppc64le

```console
$ docker pull composer@sha256:273ef0b791c27b94c856cdf8854312e8f1fee0a8533ea12299bd033053aee9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76814960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89dedefde6c35d833333272a0f72fd082f233bbc63f2260b86fee1fbf2a05fc4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
ENV COMPOSER_VERSION=2.2.24
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
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2473147d3bc2923a26c8ba560c425ef2674fbae2edbc29833bb5790c2c94db2`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 5.6 MB (5572572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53975073457162c05af82756884811d86cf52d05953b0589749a216a80864431`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58037573bd03f9687676a3398cb715ac628a3bc280f63aa990e8171ef59ce1c9`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f80183c138cedf9dc24420caf7f9769369bf61c8db0eb09729c4303c31ba1b`  
		Last Modified: Thu, 21 Nov 2024 18:14:28 GMT  
		Size: 13.6 MB (13572757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1746563bd5a8883ee2e1758e12423a999df46412bbeb663f9f774dc595e96ed`  
		Last Modified: Thu, 21 Nov 2024 18:14:27 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3428ebe5f2568169c292765c92b0cc55c0ef85fc46ab1c4d0b60b2d86970b4b3`  
		Last Modified: Thu, 21 Nov 2024 18:14:29 GMT  
		Size: 21.7 MB (21712721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f8424c24e908ec0192f8ff40322e44264734608539de7427be91c3398884dc`  
		Last Modified: Thu, 21 Nov 2024 18:14:27 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef3b5629726f19111a47ee6dc86f22265d0002270ef68da5bb572a2fa8a6d04`  
		Last Modified: Thu, 21 Nov 2024 18:14:28 GMT  
		Size: 19.4 KB (19424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf7d67a2a72f10bea3ee74b2250affb6d2de6aac3751149e9003e6b4ff24a2e`  
		Last Modified: Thu, 21 Nov 2024 21:22:37 GMT  
		Size: 31.4 MB (31402451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011cd0419150962df2f83f6c5e96043ca7df1ddb5a812e226d6f2b98814c7fc0`  
		Last Modified: Thu, 21 Nov 2024 21:22:35 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f739c523c65801d9bf3a3512b64f2a819fb4533b819d382f1b5236a2ab0fb79`  
		Last Modified: Thu, 21 Nov 2024 21:22:36 GMT  
		Size: 957.7 KB (957693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ee41244fae528c8ba994c3f0c062d5063890d34b2b13f37417073f4e4abb20`  
		Last Modified: Thu, 21 Nov 2024 21:22:36 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb5d18c4f4e6134f2c4406383a1debea61cefc8dd4a5da7a59075c1ada07832`  
		Last Modified: Thu, 21 Nov 2024 21:22:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.24` - unknown; unknown

```console
$ docker pull composer@sha256:5aa5e9f65405cd9a12eb9dd2b99fe48646e40b7aefdb630ddc0e0f75997e7a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80f49cfb840ebf4f850dba9467d0efb1d6b82b91f1586b93a7df1f84500413b`

```dockerfile
```

-	Layers:
	-	`sha256:d07b44100f7897664a442a7aff9c544144d8bc29a038de7cba4329f3d908f62b`  
		Last Modified: Thu, 21 Nov 2024 21:22:36 GMT  
		Size: 2.1 MB (2146042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:917db0d38ca1fa32a3425dd85715d616780fa2374048dd32b9c01757c2601999`  
		Last Modified: Thu, 21 Nov 2024 21:22:35 GMT  
		Size: 30.7 KB (30696 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.24` - linux; riscv64

```console
$ docker pull composer@sha256:3ddd4f307e73eb3bcde94c20848064553bd21d845bfd4b7ff551d8f352aad3bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69829962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10f76d711de731796de0a4a395f77b1447f8431b1d58b8fdb2c3cce859ee3fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
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
ENV COMPOSER_VERSION=2.2.24
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
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8ca85c9d20c6f76d0a8087ac3a4ddd6a1e40652d189dc8dad7ca6b0737c4b0`  
		Last Modified: Tue, 12 Nov 2024 06:14:49 GMT  
		Size: 5.4 MB (5382174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d2dfe107b4bddcc389bedcee9ca3fc81f02dc0799e313c21f307ddb454b4dc`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df7310166e795cb48e721a885b92af688db981613ad6597943011293aca738c`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626cc5aa152e22cd453ede74c922b963a3bc8a4bcf66d8a4763c977a36db9bbf`  
		Last Modified: Tue, 12 Nov 2024 11:38:11 GMT  
		Size: 12.5 MB (12504597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e68d6f9ff3ad2f5f92d5d2e1da7c8e8e8c7acf26714c65fb1634379b0ceabea`  
		Last Modified: Tue, 12 Nov 2024 11:38:08 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7ef4ac959dd31d8a66fcf270291f1312424b277d8adec2eded58a835d3130c`  
		Last Modified: Tue, 12 Nov 2024 11:38:11 GMT  
		Size: 16.8 MB (16791439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f9910ad73e6186422edca968a56743133f52309ae7e8fbfaeba5689ec14ce1`  
		Last Modified: Tue, 12 Nov 2024 11:38:08 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cccb83ba6c8bd3926d00dba2c6475d1639c61ec7b4dc48a094f44e9ef2d363f`  
		Last Modified: Tue, 12 Nov 2024 11:38:10 GMT  
		Size: 19.4 KB (19444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1184794faa4cb72388841b6ca5edd801726298f1bc7a901384a6611a072b84d`  
		Last Modified: Wed, 13 Nov 2024 13:17:47 GMT  
		Size: 30.8 MB (30811150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0835e0d761497dfe92dfd2f01937792ca5c678bba375a232324b9fbb0ba5120`  
		Last Modified: Wed, 13 Nov 2024 13:17:42 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c554724d42fde604b2c035bae323f605a4cc0c9636d7bdfcbd0f7314063855c`  
		Last Modified: Thu, 14 Nov 2024 17:31:54 GMT  
		Size: 944.8 KB (944794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f996300435f6471be064e050bb5d21dbc2a9d7e12bfb48c5581ffb7091600e`  
		Last Modified: Thu, 14 Nov 2024 17:31:53 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd23ffb62d5751d22ddc4bfc9f5abe311dd9d793f5b461d065fb0f50fe4e9d2e`  
		Last Modified: Thu, 14 Nov 2024 17:31:53 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.24` - unknown; unknown

```console
$ docker pull composer@sha256:2d88e8f1faac4e0669dfc54e81e569dd1591b97c410c04f461aed8935e8e7a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf3466f3664bd0ac8832b3717e606b2c1acbb35c1ffff936f34501c3ffabfb5`

```dockerfile
```

-	Layers:
	-	`sha256:ef84f869596117d88e713b7a48ac2a4701961f87f93ecca1a1616ec550b671f1`  
		Last Modified: Thu, 14 Nov 2024 17:31:53 GMT  
		Size: 2.1 MB (2145659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e828aa65c76f40f9e116367e305f3d9196b226f3824fe9e59c2ec1836e46489e`  
		Last Modified: Thu, 14 Nov 2024 17:31:53 GMT  
		Size: 30.7 KB (30705 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.24` - linux; s390x

```console
$ docker pull composer@sha256:0b741a73b3c522adafb8efb5dd9991126e70a4192f5e2055ccb7f1db027117f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76135045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffebc5d710dc20bfb62fe4a32c3df2b531aed5feecb67ac1d8f2d058dcf31485`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
ENV COMPOSER_VERSION=2.2.24
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
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26915a92034b18e2de9232a415d1ad92dc1c7a9f9e2b5bb9c590ce4c503ab73e`  
		Last Modified: Tue, 12 Nov 2024 03:39:27 GMT  
		Size: 5.5 MB (5532119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4041b6d620078267a8ee6dd6b9c31735d82dee5f22aa96467865a8134d616c`  
		Last Modified: Tue, 12 Nov 2024 03:39:26 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5555efb309fc5275c2fd44eabaaf4ca859f01b510ef24cbad6009d7ed6dc4696`  
		Last Modified: Tue, 12 Nov 2024 03:39:26 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ebcb70bd65f646a0a9f4f475ec50ab3b189c26c5453f7261bc927c566c16f4`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 13.6 MB (13572754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1fe669f736130225879d8f3a94b1a2dc84c8a542232c1010d5c0efdfb490ab`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ebb202afe7221a69abb8b0e5dd9a734085f863f2a450dd0794f4e1c6bc5189`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 21.3 MB (21250100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7a60154e6bcac48ec5bae22b14f7b46c6200a532944883ccb70d97a5f9ff15`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76035e400728cb3a6c7bd01204127072929a705a4be9f5ab31588ec5dce5bd70`  
		Last Modified: Thu, 21 Nov 2024 18:24:27 GMT  
		Size: 19.4 KB (19435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391e13c55cb9dd9b3adaa2c815b5a344bfd110a0afc12b82e71ba8af9327a7a3`  
		Last Modified: Thu, 21 Nov 2024 21:24:03 GMT  
		Size: 31.3 MB (31338617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d1aea81c97d878724863520afce631476bbf2f86f4eaf2a4b781b5d4f855ba`  
		Last Modified: Thu, 21 Nov 2024 21:24:02 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4b1710f0705434f4bdcfd8d31140ef64468bb215062f4232b1b6b2b71deb62`  
		Last Modified: Thu, 21 Nov 2024 21:24:03 GMT  
		Size: 955.5 KB (955542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2795ba63978bfd04dfd9f48b1785eee03271dc472997f51d05ef1849ec33eda`  
		Last Modified: Thu, 21 Nov 2024 21:24:03 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda486a2686c7739a4087ac185e265c1bbe289f9a216ae45f54d2fa1d70b166b`  
		Last Modified: Thu, 21 Nov 2024 21:24:03 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.24` - unknown; unknown

```console
$ docker pull composer@sha256:c2dbb513828951cee5931de5174febf1f6f07891e09131182da48b5269dacca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e69f8a7720a8658448cb346da5858583df53531e480d6571ecfe8a889bf8acc4`

```dockerfile
```

-	Layers:
	-	`sha256:434bb7bdf557e614bb7a8c41785a7d34764404cbc3e97f086f9765241b008839`  
		Last Modified: Thu, 21 Nov 2024 21:24:02 GMT  
		Size: 2.1 MB (2145444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3942678f500c80f758b086ace61ac759e021e60b71716fa73621828abae3ac09`  
		Last Modified: Thu, 21 Nov 2024 21:24:02 GMT  
		Size: 30.7 KB (30654 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8`

```console
$ docker pull composer@sha256:8bbdf5ccb6c6ddd23c578cf0e80243b42addabc07f9d421f617a166e9afe84f5
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
$ docker pull composer@sha256:4e059cb2b0bc5a68edf1cc4d310072f47831855a417f492cb5a18a82e49cf76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75020361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3f4c1ff4e156cfeb9f0ef1bc602bce75485db306c03438e390874f6589216f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4026d1cc5245f59e156bffd596323974be67dd48771842c57ace1b9fcb840`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 5.6 MB (5583566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca19f9a3dd1a82729217796a0e8ef626bd25c881db51316ae1d7b6baca3c979`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d429435d57d0d3420a2bb847cb1a04a76483e18d14ae4486b653e998810c2dc8`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22359169dee3cb23309dde8b4845f0a26d5ced82572690f0ec5de9aa5c37df6b`  
		Last Modified: Thu, 21 Nov 2024 18:00:31 GMT  
		Size: 13.6 MB (13572755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60636de7ac448f3bfc52c2d3f3fbdd7e572b65b45a980647e217005c89f46ddd`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6574e97188f3a55184dd55cbc3377b5b1826fe8ac69257fc044d8d1826cf62a`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 20.8 MB (20763608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0db01ff42c14dc52ac7bd7aad09e0a0e2b0050a0ad2796a55eb92246ce39d2`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e12f7079c7bc22fa3df852b4eebe6e7b01a834b3924a0f365f1b0f3437b7eab`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 19.7 KB (19661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa4e2f4bc7afd1f94a77567f83ba03777652ce81c4c159b7b5a3fd802f9a07f`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 30.4 MB (30368666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f00e6d7d58a0de384fb60d6cae9d9e89e93999483637376e44408cd5568bfb`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d38d791dd39b847b0d2fca9f88e1f9e5a32deabf8d1db6f92e7ebb1e8e43a9`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 1.1 MB (1083341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30cdbc582e7a47a26c3d2987f21b875b06c7e908768493752631cdd9d6c620e`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f722a00c1e03183935b573019373cf60f3ec25db1c4eee7ca88b9f9b04d218`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:ae44f042feb54af530dcaede39a40f1c6e061dbb0cee268407a9e5542014a307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6565fd02e5ace02440f1e5fd8f5bb2b3a3b5cb7ceeddacca1956af65a4fe5f4c`

```dockerfile
```

-	Layers:
	-	`sha256:bf003505388f520b1732b29b58a5b2a33d4f01c44c01adc95b5a51dfea808f43`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 2.1 MB (2147787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f5510ab4926f7df0fd363daf31833ba811e31f90655736c575847e831f23e82`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 31.0 KB (30961 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v6

```console
$ docker pull composer@sha256:a1a8aa8dedf34d24825ed172fbc10989ee1d018f39755c722050e86662dc6710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71478643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a3debd87b60e1a417ef9aa4a09488eb547162846824c7816e0ef13e96b7175`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdae56950198dea1248e6f62d7e9ef311c976d55790449240dfa46ad43351f7`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 5.2 MB (5236002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773d98c98ade13dc692eaf9700be32a03220033d99905be410eda923ce054fb9`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ae964d3deb57dca49dadfc5c487d64a372e3df3db6ef51b58087c318beb33d`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851605dfb3d928a53fef3860db97edb0f94316d382df472a9f36d31603ae85dc`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 13.6 MB (13572750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb476219577608ba4633ce4f2bf10a95d8fd1bd1bb56c2fb972587e5207cb3f`  
		Last Modified: Thu, 21 Nov 2024 17:58:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698c845cc5fd3760e20d315377bdca792a2b899c35f1288b5ddf2bf66c3e10d4`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 19.0 MB (19027128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7c3d46b7180237d2a402261f2cb181901e0149fed38e5a97d2214f64ba90ac`  
		Last Modified: Thu, 21 Nov 2024 17:58:04 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72176ade970c8f4af9d251ca5d0fc1aefd6e0fa47866d9d792bf9e85a4ac16c`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 19.4 KB (19437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487dce5effb993971148992fe8918fe413df14e91c1a17c2d7a26c254d6a7b29`  
		Last Modified: Thu, 21 Nov 2024 19:21:58 GMT  
		Size: 29.2 MB (29169296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812056dc604d2f3d588dcb3b1441239d4f3a938f21cabe40a0c26a26245a6f23`  
		Last Modified: Thu, 21 Nov 2024 19:21:57 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c30396d8c38d03f44a9669abfdcb1464e3752bb97120d8313ce5f23687a2197`  
		Last Modified: Thu, 21 Nov 2024 19:23:22 GMT  
		Size: 1.1 MB (1082560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb0c3ba98f312cc7166562cc003a0957dda83f716dde5bfda8830ad7379374b`  
		Last Modified: Mon, 18 Nov 2024 19:48:06 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46386c7251234ca16cef7ef7981829cec1c68a31f633038fae82f6fa4bea6548`  
		Last Modified: Thu, 21 Nov 2024 19:23:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:60e2c0bf91ca903330a7cceee1b41c2a1bbdb267bf7b5e4cc9e5a1c2d822c321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:460c835358535ff48139328c022972640ebc869facb7cf89d3ee604273a63765`

```dockerfile
```

-	Layers:
	-	`sha256:8c21f2e4345b18b3fe6f8b8efa0f6ed566833b64e77ca88d1600710a2bfd87fd`  
		Last Modified: Thu, 21 Nov 2024 19:23:21 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v7

```console
$ docker pull composer@sha256:2a2fda30bd0a71491f52d5f8ba6fd1c8b75128d4f453e41948f7d4b6d449b33d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69375719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd54441d7ac9c328c06b46add65b2869b5cf1eba49739aa76e0dbef1e2c8fb51`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2878563f55378e5cb0d2e6fc051acec0bad59706b4c55d991502e489d45f15b9`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 4.9 MB (4894482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1da599409a1b1b855c6d69889b78470128711398dd127ceb61f803c590c9c39`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fec221aedc472ddb77d24345957296ec946aab0b124953af99b1b103ca464d6`  
		Last Modified: Tue, 12 Nov 2024 03:55:37 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46d0dd0a80f3bfa93fe376e12f14d3cf1bf7c86c9c039106b233b8584ec9aac`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 13.6 MB (13572743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d138265234b8809a223e845ff20a559fa757eebafc98f9e9bf724fe8e7dc8b6c`  
		Last Modified: Thu, 21 Nov 2024 18:28:27 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b99f01624e25d17567cb4316e05b197890eaf269e39da90cf62573fc75f8dab`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 17.9 MB (17928178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc46c2ae1e666fefa71dcffefd35978d65be61640f7a3dae1293e1c413955d01`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4995aff739b8938a9a1f51923b6e970cc4d974c131fb8f2f8be37bd64c89bf1e`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 19.5 KB (19454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8371af98339513b427681640d9952ffda9674c0a7837c1f5e1ca4b91fa04e1`  
		Last Modified: Thu, 21 Nov 2024 22:48:27 GMT  
		Size: 28.8 MB (28798173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7861e6ac85a5be9e606f1a0b1ed4b0869e26847132c16ba05c326da3b82f1fb`  
		Last Modified: Thu, 21 Nov 2024 22:48:26 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685e48610c1b40acc2e7489adf5cd45075bc17f1989f32ff40ec88bab369412e`  
		Last Modified: Thu, 21 Nov 2024 22:51:00 GMT  
		Size: 1.1 MB (1062327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f436ad28fae8c9b37d0931ddc038b6260d88038cc84c5bac52a80de62e584f`  
		Last Modified: Mon, 18 Nov 2024 20:23:42 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b313c209ec4a8a313770caaea8ce391741ccc849671d0a07bcca4cba673646`  
		Last Modified: Thu, 21 Nov 2024 22:50:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:7fc4bb9deae034836057b0de9d2cd6e75dd5b12a05fca77bfaa86b783e7219ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a837dc411a94406d400408f2f1e540fc9d76247dfafcc1cbd167c8025c31b39`

```dockerfile
```

-	Layers:
	-	`sha256:e7520a751b99b025d4a994bb6fc0fdb2eec68fd15549efc4ef455996369d7149`  
		Last Modified: Thu, 21 Nov 2024 22:50:59 GMT  
		Size: 2.1 MB (2148108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:568ebb246b0ab7809dc7d276c7da38d3d728e1928d445eab02832dbe5a4493f6`  
		Last Modified: Thu, 21 Nov 2024 22:50:59 GMT  
		Size: 31.1 KB (31062 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:4b882bdbb24c6e89273dc14535bcbd6dab179fc237347ff42a8d62c866bf401f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76081794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7595d594af7fee7f4faf35786a3cb54cbbeeae63a9412e75ee8ce6dc7290c3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8484336630ebb870b45fd46b300831768da17cae91aa6a615fe97d849bf7d9`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 6.0 MB (6047382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f0bf50f7dfd6864235893d3a770f2748c511f29a319b959cd61ab88719f191`  
		Last Modified: Thu, 21 Nov 2024 18:25:40 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4094551f517548ba326fd9610784089231cb5fe7b32fb0fd484b4ef62a06ec4e`  
		Last Modified: Thu, 21 Nov 2024 18:25:40 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f3a19954028229594dc87f84401ff6bb04343f60f6850d3ffd56376584e127`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 13.6 MB (13572746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cec773ac8fce78f9e43c85101520fcc9a1dfd15d5ae6b0086a53ed446c44e83`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c49e3ab1eba1efe295397f466820586f5b4c820bf03494c07afc622cb0d4b80`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 20.4 MB (20379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f558eac651d11a18dc2c9e83c547cfe4241937c5dc84ca0e2f00d0fcc438eb`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec25731eb581dc3064873d8a03e05f5820ff6c09af884fce4b25f79b77d6f34e`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 19.4 KB (19426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7fe1a5fdee0abebec8c80d0770c46acf11edac729c491803ec919a7373c8c`  
		Last Modified: Thu, 21 Nov 2024 22:17:56 GMT  
		Size: 30.9 MB (30879490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0fda769fb77685ab9ff0bd8069d8c4670c1a85af4283162afa7524a8124d45`  
		Last Modified: Thu, 21 Nov 2024 22:17:55 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df9080391afa561614604f21c0161c8bad69d4bc52915415b7c1c65f1bf527a`  
		Last Modified: Thu, 21 Nov 2024 22:19:26 GMT  
		Size: 1.1 MB (1091147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54549015f1d85f07424904365c45002761ecb1f1ed4c44d30ad38297de2a6ebb`  
		Last Modified: Thu, 21 Nov 2024 22:19:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c835e644aa517172a0c42a44439508bef9c61bc21a4f1d5b5adb2285038ce2`  
		Last Modified: Thu, 21 Nov 2024 22:19:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:fd81fa9ab08837460f0bfd44ad469400783f6dd4999ddaf52faf5f9f51b241d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e780c631b16e7f52966897fff323da2a156189b610aae94c8a0a2d4e63eb18`

```dockerfile
```

-	Layers:
	-	`sha256:c5abcc231fd8648f0ce4567486331a77eb7892aaaed996a3a02e655bedbd92c1`  
		Last Modified: Thu, 21 Nov 2024 22:19:26 GMT  
		Size: 2.1 MB (2147938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4482946d0eecf5bd8d0b027fef05ac9b3378a4e06e4b379f48e4c15dc881a886`  
		Last Modified: Thu, 21 Nov 2024 22:19:25 GMT  
		Size: 31.1 KB (31095 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; 386

```console
$ docker pull composer@sha256:5895b27fa42c598668b64122527f1f2aed8003aff127fa28729e1e845ea5c115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56186940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785154b0de710a50fc157f346144c8a62d0b24f291fde96abe6e995b1b34687d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e11d2a2a48dac61e9ac66af5a5b296591c6a200cf9944fd4df55e48749cce57`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 5.5 MB (5468335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3858fed08c63431ed26286b0317883b23277e3ce014a38a3ca7392c05f0e669a`  
		Last Modified: Thu, 21 Nov 2024 18:00:49 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d4c27ab44c7e13de299ad07b09e18b7c98dee3c34fbee400448997573becdb`  
		Last Modified: Thu, 21 Nov 2024 18:00:49 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b25b38e344c1ca4be9ca4235d6cde628e170971af37a03e30f897cf5a758c`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 13.6 MB (13572753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1764d36b8a53c825b53731114444100b7e1bf8a517ab182b4dab438333bee585`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6444425964f24bb27686445f1e394678dae6d912247a4b8f26e4d7b57e90f54`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 21.3 MB (21300265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2465ec415dcb964fc8b6deb3edeeddfb60a77336ebafdeeff9780a230562a2`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b021291a02d8b49460ff1ff13393725cf6e1616dbb1b2a1ef9c7a69fdeab5b4`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 19.6 KB (19644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8aabe33271ab76e9f0a0e14600b67129c22b6376b9ac5691140b583e58214`  
		Last Modified: Thu, 21 Nov 2024 18:10:39 GMT  
		Size: 11.3 MB (11281350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91db55eda861b506210850850e90775ccb8a5505fd86fc292beade07dfeb2c7`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e53d342f08d79d0e95d5cb9b8fdac226218ccd7ac8bfb85a3f8be83b4ca0ec9`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 1.1 MB (1070507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab1b7d6b2a7b5eaffc0c95c278d0bb7c18b20204b2b5eae520c71c7090c6f4a`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb0c74b28b1a5cf47e26e8fec2c840aca547b64a308d1f713a87c93c3561567`  
		Last Modified: Thu, 21 Nov 2024 18:10:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:25307faf2d420c206138ef2b318e90ed0512a70e815b45eda1e66c22d7de7870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.4 KB (452381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f11fa5495a188f46f0b1773d57cd753fb004f768200c8b8c087c3d2872b9cff3`

```dockerfile
```

-	Layers:
	-	`sha256:1adf3a09467edab2b6efdb58c8ac6149ca0ff37d945ac99bb7cf5e9979fbada9`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 421.5 KB (421456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b888a5c47580083cfe521b71b5f008ccfc23b0bfbaae5e6aab7398e655f2374e`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 30.9 KB (30925 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; ppc64le

```console
$ docker pull composer@sha256:b31a01870fb72277be00f9566c0fe6d607c86cb57bdc3c1cb0ead0e0d3fd6e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76958826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7777a78f24315baa2ef132135d753c98210a852f450bcc815b8cb9472767bc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2473147d3bc2923a26c8ba560c425ef2674fbae2edbc29833bb5790c2c94db2`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 5.6 MB (5572572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53975073457162c05af82756884811d86cf52d05953b0589749a216a80864431`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58037573bd03f9687676a3398cb715ac628a3bc280f63aa990e8171ef59ce1c9`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f80183c138cedf9dc24420caf7f9769369bf61c8db0eb09729c4303c31ba1b`  
		Last Modified: Thu, 21 Nov 2024 18:14:28 GMT  
		Size: 13.6 MB (13572757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1746563bd5a8883ee2e1758e12423a999df46412bbeb663f9f774dc595e96ed`  
		Last Modified: Thu, 21 Nov 2024 18:14:27 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3428ebe5f2568169c292765c92b0cc55c0ef85fc46ab1c4d0b60b2d86970b4b3`  
		Last Modified: Thu, 21 Nov 2024 18:14:29 GMT  
		Size: 21.7 MB (21712721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f8424c24e908ec0192f8ff40322e44264734608539de7427be91c3398884dc`  
		Last Modified: Thu, 21 Nov 2024 18:14:27 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef3b5629726f19111a47ee6dc86f22265d0002270ef68da5bb572a2fa8a6d04`  
		Last Modified: Thu, 21 Nov 2024 18:14:28 GMT  
		Size: 19.4 KB (19424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf7d67a2a72f10bea3ee74b2250affb6d2de6aac3751149e9003e6b4ff24a2e`  
		Last Modified: Thu, 21 Nov 2024 21:22:37 GMT  
		Size: 31.4 MB (31402451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011cd0419150962df2f83f6c5e96043ca7df1ddb5a812e226d6f2b98814c7fc0`  
		Last Modified: Thu, 21 Nov 2024 21:22:35 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac37fe451ac8534aca4e4e40851e92cc0468a5064576179550c5594bf87157e4`  
		Last Modified: Thu, 21 Nov 2024 21:24:48 GMT  
		Size: 1.1 MB (1101560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14909c3d44cb9216423277a8fff5ce20356c2f7170dff5ae30ad76fa2fe58235`  
		Last Modified: Thu, 21 Nov 2024 21:24:47 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d2063201f1a57cceae80e31658ce1e97b597798722a7ce1a5b6bcf68c9b206`  
		Last Modified: Thu, 21 Nov 2024 21:24:47 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:abcbb063050d224d69d1489b752b0227a8f5e4144d73f0b691f10f5296f85514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b35bdb873177e2ab223c603904bbaca948a7a86b161653ed30eec8a261bc67`

```dockerfile
```

-	Layers:
	-	`sha256:c725c209387c0493e239864a94db3246df808fee3270bc3de3c86bc19e6a398e`  
		Last Modified: Thu, 21 Nov 2024 21:24:48 GMT  
		Size: 2.1 MB (2146342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a73619b309ab318681d8ac6c230f818f2b6cc6f8475cef18f95a964e7b2c8b1`  
		Last Modified: Thu, 21 Nov 2024 21:24:47 GMT  
		Size: 31.0 KB (31007 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; riscv64

```console
$ docker pull composer@sha256:ed8bec923846612aeec9d7c5b4e37d4c27b46e61083ef994d73edacc353eb451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70713138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bbd153b3fff08b930c02c40db9c3bede384367eb09e013935beca56ef232ae`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8ca85c9d20c6f76d0a8087ac3a4ddd6a1e40652d189dc8dad7ca6b0737c4b0`  
		Last Modified: Tue, 12 Nov 2024 06:14:49 GMT  
		Size: 5.4 MB (5382174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d2dfe107b4bddcc389bedcee9ca3fc81f02dc0799e313c21f307ddb454b4dc`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df7310166e795cb48e721a885b92af688db981613ad6597943011293aca738c`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626cc5aa152e22cd453ede74c922b963a3bc8a4bcf66d8a4763c977a36db9bbf`  
		Last Modified: Tue, 12 Nov 2024 11:38:11 GMT  
		Size: 12.5 MB (12504597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e68d6f9ff3ad2f5f92d5d2e1da7c8e8e8c7acf26714c65fb1634379b0ceabea`  
		Last Modified: Tue, 12 Nov 2024 11:38:08 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7ef4ac959dd31d8a66fcf270291f1312424b277d8adec2eded58a835d3130c`  
		Last Modified: Tue, 12 Nov 2024 11:38:11 GMT  
		Size: 16.8 MB (16791439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f9910ad73e6186422edca968a56743133f52309ae7e8fbfaeba5689ec14ce1`  
		Last Modified: Tue, 12 Nov 2024 11:38:08 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cccb83ba6c8bd3926d00dba2c6475d1639c61ec7b4dc48a094f44e9ef2d363f`  
		Last Modified: Tue, 12 Nov 2024 11:38:10 GMT  
		Size: 19.4 KB (19444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1184794faa4cb72388841b6ca5edd801726298f1bc7a901384a6611a072b84d`  
		Last Modified: Wed, 13 Nov 2024 13:17:47 GMT  
		Size: 30.8 MB (30811150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0835e0d761497dfe92dfd2f01937792ca5c678bba375a232324b9fbb0ba5120`  
		Last Modified: Wed, 13 Nov 2024 13:17:42 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07c683546f1dbb73a401c02ec6169c6db9a2e1163a15f184d5c634965a1e5db`  
		Last Modified: Mon, 18 Nov 2024 19:11:38 GMT  
		Size: 1.8 MB (1827970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db5e9fa9e94a1dfd1dbce4db1c03e977d7ef88c4265803e7fb16536ce3901bb`  
		Last Modified: Mon, 18 Nov 2024 19:11:38 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bb7be447bc29d4901509e73b2e709bbfe7daf883f9dc94e2f83ca774cdf247`  
		Last Modified: Mon, 18 Nov 2024 19:11:38 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:699f6536b8af5d06e22a6567155fa157b1c7ee6de20657fe2bfb50c733e9138c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07826998165fa93f84ac501d6a553f14a3c873f356bcdbd20cdb0d1875832fca`

```dockerfile
```

-	Layers:
	-	`sha256:ff4fae5f5ec59bf9f691ec534e5babfe3171a3fe2db50fe20bfe894d62bbc67f`  
		Last Modified: Mon, 18 Nov 2024 19:11:37 GMT  
		Size: 2.1 MB (2145960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e221ef006b10f92faeefea08445fba63054cfdf42a7de63decab79954c796f3`  
		Last Modified: Mon, 18 Nov 2024 19:11:37 GMT  
		Size: 31.0 KB (31018 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; s390x

```console
$ docker pull composer@sha256:e21dca9bf0b9c7065a2aef60fc6a0e3a03a86445503700c9eff2f48792a80f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76278627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0683d3d3b3aceba01f85e8de7138bb8723ea04c6b816570cce7dc9310f0a4973`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26915a92034b18e2de9232a415d1ad92dc1c7a9f9e2b5bb9c590ce4c503ab73e`  
		Last Modified: Tue, 12 Nov 2024 03:39:27 GMT  
		Size: 5.5 MB (5532119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4041b6d620078267a8ee6dd6b9c31735d82dee5f22aa96467865a8134d616c`  
		Last Modified: Tue, 12 Nov 2024 03:39:26 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5555efb309fc5275c2fd44eabaaf4ca859f01b510ef24cbad6009d7ed6dc4696`  
		Last Modified: Tue, 12 Nov 2024 03:39:26 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ebcb70bd65f646a0a9f4f475ec50ab3b189c26c5453f7261bc927c566c16f4`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 13.6 MB (13572754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1fe669f736130225879d8f3a94b1a2dc84c8a542232c1010d5c0efdfb490ab`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ebb202afe7221a69abb8b0e5dd9a734085f863f2a450dd0794f4e1c6bc5189`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 21.3 MB (21250100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7a60154e6bcac48ec5bae22b14f7b46c6200a532944883ccb70d97a5f9ff15`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76035e400728cb3a6c7bd01204127072929a705a4be9f5ab31588ec5dce5bd70`  
		Last Modified: Thu, 21 Nov 2024 18:24:27 GMT  
		Size: 19.4 KB (19435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391e13c55cb9dd9b3adaa2c815b5a344bfd110a0afc12b82e71ba8af9327a7a3`  
		Last Modified: Thu, 21 Nov 2024 21:24:03 GMT  
		Size: 31.3 MB (31338617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d1aea81c97d878724863520afce631476bbf2f86f4eaf2a4b781b5d4f855ba`  
		Last Modified: Thu, 21 Nov 2024 21:24:02 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec41f417f32df8d6b29087fb50d7165f6ba5622272536044aad8346263321cd`  
		Last Modified: Thu, 21 Nov 2024 21:25:56 GMT  
		Size: 1.1 MB (1099124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d41623169f490a3c4b3ad708f3715985370d656560af18567d32dad796bd601`  
		Last Modified: Thu, 21 Nov 2024 21:25:56 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103104b2577b229e90d735ad3b6db3d300d26fd3f7bd0aa3cacbcaf87380344b`  
		Last Modified: Thu, 21 Nov 2024 21:25:56 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:fd2bbd770d3c98acb45d0ea2760f1f299ef68190c3ee369a618a74f8008cab4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ec6c9d823e50f933620ebd04ef4de684361b80bd7821ee35d672f7c6349d57`

```dockerfile
```

-	Layers:
	-	`sha256:f718eb8ddf8df0e06b8bf814924ded8904373825b635c0fd316aac4860492380`  
		Last Modified: Thu, 21 Nov 2024 21:25:55 GMT  
		Size: 2.1 MB (2145738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f05d0590058fbabd4f7c681b6947c6efbf8ba4a06a51353d3354d9ce6a0898e9`  
		Last Modified: Thu, 21 Nov 2024 21:25:55 GMT  
		Size: 31.0 KB (30960 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8.3`

```console
$ docker pull composer@sha256:8bbdf5ccb6c6ddd23c578cf0e80243b42addabc07f9d421f617a166e9afe84f5
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

### `composer:2.8.3` - linux; amd64

```console
$ docker pull composer@sha256:4e059cb2b0bc5a68edf1cc4d310072f47831855a417f492cb5a18a82e49cf76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75020361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3f4c1ff4e156cfeb9f0ef1bc602bce75485db306c03438e390874f6589216f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4026d1cc5245f59e156bffd596323974be67dd48771842c57ace1b9fcb840`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 5.6 MB (5583566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca19f9a3dd1a82729217796a0e8ef626bd25c881db51316ae1d7b6baca3c979`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d429435d57d0d3420a2bb847cb1a04a76483e18d14ae4486b653e998810c2dc8`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22359169dee3cb23309dde8b4845f0a26d5ced82572690f0ec5de9aa5c37df6b`  
		Last Modified: Thu, 21 Nov 2024 18:00:31 GMT  
		Size: 13.6 MB (13572755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60636de7ac448f3bfc52c2d3f3fbdd7e572b65b45a980647e217005c89f46ddd`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6574e97188f3a55184dd55cbc3377b5b1826fe8ac69257fc044d8d1826cf62a`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 20.8 MB (20763608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0db01ff42c14dc52ac7bd7aad09e0a0e2b0050a0ad2796a55eb92246ce39d2`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e12f7079c7bc22fa3df852b4eebe6e7b01a834b3924a0f365f1b0f3437b7eab`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 19.7 KB (19661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa4e2f4bc7afd1f94a77567f83ba03777652ce81c4c159b7b5a3fd802f9a07f`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 30.4 MB (30368666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f00e6d7d58a0de384fb60d6cae9d9e89e93999483637376e44408cd5568bfb`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d38d791dd39b847b0d2fca9f88e1f9e5a32deabf8d1db6f92e7ebb1e8e43a9`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 1.1 MB (1083341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30cdbc582e7a47a26c3d2987f21b875b06c7e908768493752631cdd9d6c620e`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f722a00c1e03183935b573019373cf60f3ec25db1c4eee7ca88b9f9b04d218`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.3` - unknown; unknown

```console
$ docker pull composer@sha256:ae44f042feb54af530dcaede39a40f1c6e061dbb0cee268407a9e5542014a307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6565fd02e5ace02440f1e5fd8f5bb2b3a3b5cb7ceeddacca1956af65a4fe5f4c`

```dockerfile
```

-	Layers:
	-	`sha256:bf003505388f520b1732b29b58a5b2a33d4f01c44c01adc95b5a51dfea808f43`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 2.1 MB (2147787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f5510ab4926f7df0fd363daf31833ba811e31f90655736c575847e831f23e82`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 31.0 KB (30961 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.3` - linux; arm variant v6

```console
$ docker pull composer@sha256:a1a8aa8dedf34d24825ed172fbc10989ee1d018f39755c722050e86662dc6710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71478643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a3debd87b60e1a417ef9aa4a09488eb547162846824c7816e0ef13e96b7175`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdae56950198dea1248e6f62d7e9ef311c976d55790449240dfa46ad43351f7`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 5.2 MB (5236002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773d98c98ade13dc692eaf9700be32a03220033d99905be410eda923ce054fb9`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ae964d3deb57dca49dadfc5c487d64a372e3df3db6ef51b58087c318beb33d`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851605dfb3d928a53fef3860db97edb0f94316d382df472a9f36d31603ae85dc`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 13.6 MB (13572750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb476219577608ba4633ce4f2bf10a95d8fd1bd1bb56c2fb972587e5207cb3f`  
		Last Modified: Thu, 21 Nov 2024 17:58:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698c845cc5fd3760e20d315377bdca792a2b899c35f1288b5ddf2bf66c3e10d4`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 19.0 MB (19027128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7c3d46b7180237d2a402261f2cb181901e0149fed38e5a97d2214f64ba90ac`  
		Last Modified: Thu, 21 Nov 2024 17:58:04 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72176ade970c8f4af9d251ca5d0fc1aefd6e0fa47866d9d792bf9e85a4ac16c`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 19.4 KB (19437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487dce5effb993971148992fe8918fe413df14e91c1a17c2d7a26c254d6a7b29`  
		Last Modified: Thu, 21 Nov 2024 19:21:58 GMT  
		Size: 29.2 MB (29169296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812056dc604d2f3d588dcb3b1441239d4f3a938f21cabe40a0c26a26245a6f23`  
		Last Modified: Thu, 21 Nov 2024 19:21:57 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c30396d8c38d03f44a9669abfdcb1464e3752bb97120d8313ce5f23687a2197`  
		Last Modified: Thu, 21 Nov 2024 19:23:22 GMT  
		Size: 1.1 MB (1082560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb0c3ba98f312cc7166562cc003a0957dda83f716dde5bfda8830ad7379374b`  
		Last Modified: Mon, 18 Nov 2024 19:48:06 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46386c7251234ca16cef7ef7981829cec1c68a31f633038fae82f6fa4bea6548`  
		Last Modified: Thu, 21 Nov 2024 19:23:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.3` - unknown; unknown

```console
$ docker pull composer@sha256:60e2c0bf91ca903330a7cceee1b41c2a1bbdb267bf7b5e4cc9e5a1c2d822c321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:460c835358535ff48139328c022972640ebc869facb7cf89d3ee604273a63765`

```dockerfile
```

-	Layers:
	-	`sha256:8c21f2e4345b18b3fe6f8b8efa0f6ed566833b64e77ca88d1600710a2bfd87fd`  
		Last Modified: Thu, 21 Nov 2024 19:23:21 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.3` - linux; arm variant v7

```console
$ docker pull composer@sha256:2a2fda30bd0a71491f52d5f8ba6fd1c8b75128d4f453e41948f7d4b6d449b33d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69375719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd54441d7ac9c328c06b46add65b2869b5cf1eba49739aa76e0dbef1e2c8fb51`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2878563f55378e5cb0d2e6fc051acec0bad59706b4c55d991502e489d45f15b9`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 4.9 MB (4894482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1da599409a1b1b855c6d69889b78470128711398dd127ceb61f803c590c9c39`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fec221aedc472ddb77d24345957296ec946aab0b124953af99b1b103ca464d6`  
		Last Modified: Tue, 12 Nov 2024 03:55:37 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46d0dd0a80f3bfa93fe376e12f14d3cf1bf7c86c9c039106b233b8584ec9aac`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 13.6 MB (13572743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d138265234b8809a223e845ff20a559fa757eebafc98f9e9bf724fe8e7dc8b6c`  
		Last Modified: Thu, 21 Nov 2024 18:28:27 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b99f01624e25d17567cb4316e05b197890eaf269e39da90cf62573fc75f8dab`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 17.9 MB (17928178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc46c2ae1e666fefa71dcffefd35978d65be61640f7a3dae1293e1c413955d01`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4995aff739b8938a9a1f51923b6e970cc4d974c131fb8f2f8be37bd64c89bf1e`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 19.5 KB (19454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8371af98339513b427681640d9952ffda9674c0a7837c1f5e1ca4b91fa04e1`  
		Last Modified: Thu, 21 Nov 2024 22:48:27 GMT  
		Size: 28.8 MB (28798173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7861e6ac85a5be9e606f1a0b1ed4b0869e26847132c16ba05c326da3b82f1fb`  
		Last Modified: Thu, 21 Nov 2024 22:48:26 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685e48610c1b40acc2e7489adf5cd45075bc17f1989f32ff40ec88bab369412e`  
		Last Modified: Thu, 21 Nov 2024 22:51:00 GMT  
		Size: 1.1 MB (1062327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f436ad28fae8c9b37d0931ddc038b6260d88038cc84c5bac52a80de62e584f`  
		Last Modified: Mon, 18 Nov 2024 20:23:42 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b313c209ec4a8a313770caaea8ce391741ccc849671d0a07bcca4cba673646`  
		Last Modified: Thu, 21 Nov 2024 22:50:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.3` - unknown; unknown

```console
$ docker pull composer@sha256:7fc4bb9deae034836057b0de9d2cd6e75dd5b12a05fca77bfaa86b783e7219ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a837dc411a94406d400408f2f1e540fc9d76247dfafcc1cbd167c8025c31b39`

```dockerfile
```

-	Layers:
	-	`sha256:e7520a751b99b025d4a994bb6fc0fdb2eec68fd15549efc4ef455996369d7149`  
		Last Modified: Thu, 21 Nov 2024 22:50:59 GMT  
		Size: 2.1 MB (2148108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:568ebb246b0ab7809dc7d276c7da38d3d728e1928d445eab02832dbe5a4493f6`  
		Last Modified: Thu, 21 Nov 2024 22:50:59 GMT  
		Size: 31.1 KB (31062 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.3` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:4b882bdbb24c6e89273dc14535bcbd6dab179fc237347ff42a8d62c866bf401f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76081794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7595d594af7fee7f4faf35786a3cb54cbbeeae63a9412e75ee8ce6dc7290c3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8484336630ebb870b45fd46b300831768da17cae91aa6a615fe97d849bf7d9`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 6.0 MB (6047382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f0bf50f7dfd6864235893d3a770f2748c511f29a319b959cd61ab88719f191`  
		Last Modified: Thu, 21 Nov 2024 18:25:40 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4094551f517548ba326fd9610784089231cb5fe7b32fb0fd484b4ef62a06ec4e`  
		Last Modified: Thu, 21 Nov 2024 18:25:40 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f3a19954028229594dc87f84401ff6bb04343f60f6850d3ffd56376584e127`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 13.6 MB (13572746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cec773ac8fce78f9e43c85101520fcc9a1dfd15d5ae6b0086a53ed446c44e83`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c49e3ab1eba1efe295397f466820586f5b4c820bf03494c07afc622cb0d4b80`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 20.4 MB (20379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f558eac651d11a18dc2c9e83c547cfe4241937c5dc84ca0e2f00d0fcc438eb`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec25731eb581dc3064873d8a03e05f5820ff6c09af884fce4b25f79b77d6f34e`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 19.4 KB (19426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7fe1a5fdee0abebec8c80d0770c46acf11edac729c491803ec919a7373c8c`  
		Last Modified: Thu, 21 Nov 2024 22:17:56 GMT  
		Size: 30.9 MB (30879490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0fda769fb77685ab9ff0bd8069d8c4670c1a85af4283162afa7524a8124d45`  
		Last Modified: Thu, 21 Nov 2024 22:17:55 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df9080391afa561614604f21c0161c8bad69d4bc52915415b7c1c65f1bf527a`  
		Last Modified: Thu, 21 Nov 2024 22:19:26 GMT  
		Size: 1.1 MB (1091147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54549015f1d85f07424904365c45002761ecb1f1ed4c44d30ad38297de2a6ebb`  
		Last Modified: Thu, 21 Nov 2024 22:19:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c835e644aa517172a0c42a44439508bef9c61bc21a4f1d5b5adb2285038ce2`  
		Last Modified: Thu, 21 Nov 2024 22:19:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.3` - unknown; unknown

```console
$ docker pull composer@sha256:fd81fa9ab08837460f0bfd44ad469400783f6dd4999ddaf52faf5f9f51b241d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e780c631b16e7f52966897fff323da2a156189b610aae94c8a0a2d4e63eb18`

```dockerfile
```

-	Layers:
	-	`sha256:c5abcc231fd8648f0ce4567486331a77eb7892aaaed996a3a02e655bedbd92c1`  
		Last Modified: Thu, 21 Nov 2024 22:19:26 GMT  
		Size: 2.1 MB (2147938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4482946d0eecf5bd8d0b027fef05ac9b3378a4e06e4b379f48e4c15dc881a886`  
		Last Modified: Thu, 21 Nov 2024 22:19:25 GMT  
		Size: 31.1 KB (31095 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.3` - linux; 386

```console
$ docker pull composer@sha256:5895b27fa42c598668b64122527f1f2aed8003aff127fa28729e1e845ea5c115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56186940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785154b0de710a50fc157f346144c8a62d0b24f291fde96abe6e995b1b34687d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e11d2a2a48dac61e9ac66af5a5b296591c6a200cf9944fd4df55e48749cce57`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 5.5 MB (5468335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3858fed08c63431ed26286b0317883b23277e3ce014a38a3ca7392c05f0e669a`  
		Last Modified: Thu, 21 Nov 2024 18:00:49 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d4c27ab44c7e13de299ad07b09e18b7c98dee3c34fbee400448997573becdb`  
		Last Modified: Thu, 21 Nov 2024 18:00:49 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b25b38e344c1ca4be9ca4235d6cde628e170971af37a03e30f897cf5a758c`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 13.6 MB (13572753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1764d36b8a53c825b53731114444100b7e1bf8a517ab182b4dab438333bee585`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6444425964f24bb27686445f1e394678dae6d912247a4b8f26e4d7b57e90f54`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 21.3 MB (21300265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2465ec415dcb964fc8b6deb3edeeddfb60a77336ebafdeeff9780a230562a2`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b021291a02d8b49460ff1ff13393725cf6e1616dbb1b2a1ef9c7a69fdeab5b4`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 19.6 KB (19644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8aabe33271ab76e9f0a0e14600b67129c22b6376b9ac5691140b583e58214`  
		Last Modified: Thu, 21 Nov 2024 18:10:39 GMT  
		Size: 11.3 MB (11281350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91db55eda861b506210850850e90775ccb8a5505fd86fc292beade07dfeb2c7`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e53d342f08d79d0e95d5cb9b8fdac226218ccd7ac8bfb85a3f8be83b4ca0ec9`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 1.1 MB (1070507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab1b7d6b2a7b5eaffc0c95c278d0bb7c18b20204b2b5eae520c71c7090c6f4a`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb0c74b28b1a5cf47e26e8fec2c840aca547b64a308d1f713a87c93c3561567`  
		Last Modified: Thu, 21 Nov 2024 18:10:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.3` - unknown; unknown

```console
$ docker pull composer@sha256:25307faf2d420c206138ef2b318e90ed0512a70e815b45eda1e66c22d7de7870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.4 KB (452381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f11fa5495a188f46f0b1773d57cd753fb004f768200c8b8c087c3d2872b9cff3`

```dockerfile
```

-	Layers:
	-	`sha256:1adf3a09467edab2b6efdb58c8ac6149ca0ff37d945ac99bb7cf5e9979fbada9`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 421.5 KB (421456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b888a5c47580083cfe521b71b5f008ccfc23b0bfbaae5e6aab7398e655f2374e`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 30.9 KB (30925 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.3` - linux; ppc64le

```console
$ docker pull composer@sha256:b31a01870fb72277be00f9566c0fe6d607c86cb57bdc3c1cb0ead0e0d3fd6e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76958826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7777a78f24315baa2ef132135d753c98210a852f450bcc815b8cb9472767bc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2473147d3bc2923a26c8ba560c425ef2674fbae2edbc29833bb5790c2c94db2`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 5.6 MB (5572572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53975073457162c05af82756884811d86cf52d05953b0589749a216a80864431`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58037573bd03f9687676a3398cb715ac628a3bc280f63aa990e8171ef59ce1c9`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f80183c138cedf9dc24420caf7f9769369bf61c8db0eb09729c4303c31ba1b`  
		Last Modified: Thu, 21 Nov 2024 18:14:28 GMT  
		Size: 13.6 MB (13572757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1746563bd5a8883ee2e1758e12423a999df46412bbeb663f9f774dc595e96ed`  
		Last Modified: Thu, 21 Nov 2024 18:14:27 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3428ebe5f2568169c292765c92b0cc55c0ef85fc46ab1c4d0b60b2d86970b4b3`  
		Last Modified: Thu, 21 Nov 2024 18:14:29 GMT  
		Size: 21.7 MB (21712721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f8424c24e908ec0192f8ff40322e44264734608539de7427be91c3398884dc`  
		Last Modified: Thu, 21 Nov 2024 18:14:27 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef3b5629726f19111a47ee6dc86f22265d0002270ef68da5bb572a2fa8a6d04`  
		Last Modified: Thu, 21 Nov 2024 18:14:28 GMT  
		Size: 19.4 KB (19424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf7d67a2a72f10bea3ee74b2250affb6d2de6aac3751149e9003e6b4ff24a2e`  
		Last Modified: Thu, 21 Nov 2024 21:22:37 GMT  
		Size: 31.4 MB (31402451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011cd0419150962df2f83f6c5e96043ca7df1ddb5a812e226d6f2b98814c7fc0`  
		Last Modified: Thu, 21 Nov 2024 21:22:35 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac37fe451ac8534aca4e4e40851e92cc0468a5064576179550c5594bf87157e4`  
		Last Modified: Thu, 21 Nov 2024 21:24:48 GMT  
		Size: 1.1 MB (1101560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14909c3d44cb9216423277a8fff5ce20356c2f7170dff5ae30ad76fa2fe58235`  
		Last Modified: Thu, 21 Nov 2024 21:24:47 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d2063201f1a57cceae80e31658ce1e97b597798722a7ce1a5b6bcf68c9b206`  
		Last Modified: Thu, 21 Nov 2024 21:24:47 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.3` - unknown; unknown

```console
$ docker pull composer@sha256:abcbb063050d224d69d1489b752b0227a8f5e4144d73f0b691f10f5296f85514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b35bdb873177e2ab223c603904bbaca948a7a86b161653ed30eec8a261bc67`

```dockerfile
```

-	Layers:
	-	`sha256:c725c209387c0493e239864a94db3246df808fee3270bc3de3c86bc19e6a398e`  
		Last Modified: Thu, 21 Nov 2024 21:24:48 GMT  
		Size: 2.1 MB (2146342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a73619b309ab318681d8ac6c230f818f2b6cc6f8475cef18f95a964e7b2c8b1`  
		Last Modified: Thu, 21 Nov 2024 21:24:47 GMT  
		Size: 31.0 KB (31007 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.3` - linux; riscv64

```console
$ docker pull composer@sha256:ed8bec923846612aeec9d7c5b4e37d4c27b46e61083ef994d73edacc353eb451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70713138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bbd153b3fff08b930c02c40db9c3bede384367eb09e013935beca56ef232ae`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8ca85c9d20c6f76d0a8087ac3a4ddd6a1e40652d189dc8dad7ca6b0737c4b0`  
		Last Modified: Tue, 12 Nov 2024 06:14:49 GMT  
		Size: 5.4 MB (5382174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d2dfe107b4bddcc389bedcee9ca3fc81f02dc0799e313c21f307ddb454b4dc`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df7310166e795cb48e721a885b92af688db981613ad6597943011293aca738c`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626cc5aa152e22cd453ede74c922b963a3bc8a4bcf66d8a4763c977a36db9bbf`  
		Last Modified: Tue, 12 Nov 2024 11:38:11 GMT  
		Size: 12.5 MB (12504597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e68d6f9ff3ad2f5f92d5d2e1da7c8e8e8c7acf26714c65fb1634379b0ceabea`  
		Last Modified: Tue, 12 Nov 2024 11:38:08 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7ef4ac959dd31d8a66fcf270291f1312424b277d8adec2eded58a835d3130c`  
		Last Modified: Tue, 12 Nov 2024 11:38:11 GMT  
		Size: 16.8 MB (16791439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f9910ad73e6186422edca968a56743133f52309ae7e8fbfaeba5689ec14ce1`  
		Last Modified: Tue, 12 Nov 2024 11:38:08 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cccb83ba6c8bd3926d00dba2c6475d1639c61ec7b4dc48a094f44e9ef2d363f`  
		Last Modified: Tue, 12 Nov 2024 11:38:10 GMT  
		Size: 19.4 KB (19444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1184794faa4cb72388841b6ca5edd801726298f1bc7a901384a6611a072b84d`  
		Last Modified: Wed, 13 Nov 2024 13:17:47 GMT  
		Size: 30.8 MB (30811150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0835e0d761497dfe92dfd2f01937792ca5c678bba375a232324b9fbb0ba5120`  
		Last Modified: Wed, 13 Nov 2024 13:17:42 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07c683546f1dbb73a401c02ec6169c6db9a2e1163a15f184d5c634965a1e5db`  
		Last Modified: Mon, 18 Nov 2024 19:11:38 GMT  
		Size: 1.8 MB (1827970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db5e9fa9e94a1dfd1dbce4db1c03e977d7ef88c4265803e7fb16536ce3901bb`  
		Last Modified: Mon, 18 Nov 2024 19:11:38 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bb7be447bc29d4901509e73b2e709bbfe7daf883f9dc94e2f83ca774cdf247`  
		Last Modified: Mon, 18 Nov 2024 19:11:38 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.3` - unknown; unknown

```console
$ docker pull composer@sha256:699f6536b8af5d06e22a6567155fa157b1c7ee6de20657fe2bfb50c733e9138c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07826998165fa93f84ac501d6a553f14a3c873f356bcdbd20cdb0d1875832fca`

```dockerfile
```

-	Layers:
	-	`sha256:ff4fae5f5ec59bf9f691ec534e5babfe3171a3fe2db50fe20bfe894d62bbc67f`  
		Last Modified: Mon, 18 Nov 2024 19:11:37 GMT  
		Size: 2.1 MB (2145960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e221ef006b10f92faeefea08445fba63054cfdf42a7de63decab79954c796f3`  
		Last Modified: Mon, 18 Nov 2024 19:11:37 GMT  
		Size: 31.0 KB (31018 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.3` - linux; s390x

```console
$ docker pull composer@sha256:e21dca9bf0b9c7065a2aef60fc6a0e3a03a86445503700c9eff2f48792a80f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76278627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0683d3d3b3aceba01f85e8de7138bb8723ea04c6b816570cce7dc9310f0a4973`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26915a92034b18e2de9232a415d1ad92dc1c7a9f9e2b5bb9c590ce4c503ab73e`  
		Last Modified: Tue, 12 Nov 2024 03:39:27 GMT  
		Size: 5.5 MB (5532119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4041b6d620078267a8ee6dd6b9c31735d82dee5f22aa96467865a8134d616c`  
		Last Modified: Tue, 12 Nov 2024 03:39:26 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5555efb309fc5275c2fd44eabaaf4ca859f01b510ef24cbad6009d7ed6dc4696`  
		Last Modified: Tue, 12 Nov 2024 03:39:26 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ebcb70bd65f646a0a9f4f475ec50ab3b189c26c5453f7261bc927c566c16f4`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 13.6 MB (13572754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1fe669f736130225879d8f3a94b1a2dc84c8a542232c1010d5c0efdfb490ab`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ebb202afe7221a69abb8b0e5dd9a734085f863f2a450dd0794f4e1c6bc5189`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 21.3 MB (21250100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7a60154e6bcac48ec5bae22b14f7b46c6200a532944883ccb70d97a5f9ff15`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76035e400728cb3a6c7bd01204127072929a705a4be9f5ab31588ec5dce5bd70`  
		Last Modified: Thu, 21 Nov 2024 18:24:27 GMT  
		Size: 19.4 KB (19435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391e13c55cb9dd9b3adaa2c815b5a344bfd110a0afc12b82e71ba8af9327a7a3`  
		Last Modified: Thu, 21 Nov 2024 21:24:03 GMT  
		Size: 31.3 MB (31338617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d1aea81c97d878724863520afce631476bbf2f86f4eaf2a4b781b5d4f855ba`  
		Last Modified: Thu, 21 Nov 2024 21:24:02 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec41f417f32df8d6b29087fb50d7165f6ba5622272536044aad8346263321cd`  
		Last Modified: Thu, 21 Nov 2024 21:25:56 GMT  
		Size: 1.1 MB (1099124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d41623169f490a3c4b3ad708f3715985370d656560af18567d32dad796bd601`  
		Last Modified: Thu, 21 Nov 2024 21:25:56 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103104b2577b229e90d735ad3b6db3d300d26fd3f7bd0aa3cacbcaf87380344b`  
		Last Modified: Thu, 21 Nov 2024 21:25:56 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.3` - unknown; unknown

```console
$ docker pull composer@sha256:fd2bbd770d3c98acb45d0ea2760f1f299ef68190c3ee369a618a74f8008cab4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ec6c9d823e50f933620ebd04ef4de684361b80bd7821ee35d672f7c6349d57`

```dockerfile
```

-	Layers:
	-	`sha256:f718eb8ddf8df0e06b8bf814924ded8904373825b635c0fd316aac4860492380`  
		Last Modified: Thu, 21 Nov 2024 21:25:55 GMT  
		Size: 2.1 MB (2145738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f05d0590058fbabd4f7c681b6947c6efbf8ba4a06a51353d3354d9ce6a0898e9`  
		Last Modified: Thu, 21 Nov 2024 21:25:55 GMT  
		Size: 31.0 KB (30960 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:latest`

```console
$ docker pull composer@sha256:8bbdf5ccb6c6ddd23c578cf0e80243b42addabc07f9d421f617a166e9afe84f5
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
$ docker pull composer@sha256:4e059cb2b0bc5a68edf1cc4d310072f47831855a417f492cb5a18a82e49cf76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75020361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3f4c1ff4e156cfeb9f0ef1bc602bce75485db306c03438e390874f6589216f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4026d1cc5245f59e156bffd596323974be67dd48771842c57ace1b9fcb840`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 5.6 MB (5583566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca19f9a3dd1a82729217796a0e8ef626bd25c881db51316ae1d7b6baca3c979`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d429435d57d0d3420a2bb847cb1a04a76483e18d14ae4486b653e998810c2dc8`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22359169dee3cb23309dde8b4845f0a26d5ced82572690f0ec5de9aa5c37df6b`  
		Last Modified: Thu, 21 Nov 2024 18:00:31 GMT  
		Size: 13.6 MB (13572755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60636de7ac448f3bfc52c2d3f3fbdd7e572b65b45a980647e217005c89f46ddd`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6574e97188f3a55184dd55cbc3377b5b1826fe8ac69257fc044d8d1826cf62a`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 20.8 MB (20763608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0db01ff42c14dc52ac7bd7aad09e0a0e2b0050a0ad2796a55eb92246ce39d2`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e12f7079c7bc22fa3df852b4eebe6e7b01a834b3924a0f365f1b0f3437b7eab`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 19.7 KB (19661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa4e2f4bc7afd1f94a77567f83ba03777652ce81c4c159b7b5a3fd802f9a07f`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 30.4 MB (30368666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f00e6d7d58a0de384fb60d6cae9d9e89e93999483637376e44408cd5568bfb`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d38d791dd39b847b0d2fca9f88e1f9e5a32deabf8d1db6f92e7ebb1e8e43a9`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 1.1 MB (1083341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30cdbc582e7a47a26c3d2987f21b875b06c7e908768493752631cdd9d6c620e`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f722a00c1e03183935b573019373cf60f3ec25db1c4eee7ca88b9f9b04d218`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:ae44f042feb54af530dcaede39a40f1c6e061dbb0cee268407a9e5542014a307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6565fd02e5ace02440f1e5fd8f5bb2b3a3b5cb7ceeddacca1956af65a4fe5f4c`

```dockerfile
```

-	Layers:
	-	`sha256:bf003505388f520b1732b29b58a5b2a33d4f01c44c01adc95b5a51dfea808f43`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 2.1 MB (2147787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f5510ab4926f7df0fd363daf31833ba811e31f90655736c575847e831f23e82`  
		Last Modified: Thu, 21 Nov 2024 18:10:33 GMT  
		Size: 31.0 KB (30961 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:a1a8aa8dedf34d24825ed172fbc10989ee1d018f39755c722050e86662dc6710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71478643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a3debd87b60e1a417ef9aa4a09488eb547162846824c7816e0ef13e96b7175`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdae56950198dea1248e6f62d7e9ef311c976d55790449240dfa46ad43351f7`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 5.2 MB (5236002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773d98c98ade13dc692eaf9700be32a03220033d99905be410eda923ce054fb9`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ae964d3deb57dca49dadfc5c487d64a372e3df3db6ef51b58087c318beb33d`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851605dfb3d928a53fef3860db97edb0f94316d382df472a9f36d31603ae85dc`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 13.6 MB (13572750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb476219577608ba4633ce4f2bf10a95d8fd1bd1bb56c2fb972587e5207cb3f`  
		Last Modified: Thu, 21 Nov 2024 17:58:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698c845cc5fd3760e20d315377bdca792a2b899c35f1288b5ddf2bf66c3e10d4`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 19.0 MB (19027128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7c3d46b7180237d2a402261f2cb181901e0149fed38e5a97d2214f64ba90ac`  
		Last Modified: Thu, 21 Nov 2024 17:58:04 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72176ade970c8f4af9d251ca5d0fc1aefd6e0fa47866d9d792bf9e85a4ac16c`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 19.4 KB (19437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487dce5effb993971148992fe8918fe413df14e91c1a17c2d7a26c254d6a7b29`  
		Last Modified: Thu, 21 Nov 2024 19:21:58 GMT  
		Size: 29.2 MB (29169296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812056dc604d2f3d588dcb3b1441239d4f3a938f21cabe40a0c26a26245a6f23`  
		Last Modified: Thu, 21 Nov 2024 19:21:57 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c30396d8c38d03f44a9669abfdcb1464e3752bb97120d8313ce5f23687a2197`  
		Last Modified: Thu, 21 Nov 2024 19:23:22 GMT  
		Size: 1.1 MB (1082560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb0c3ba98f312cc7166562cc003a0957dda83f716dde5bfda8830ad7379374b`  
		Last Modified: Mon, 18 Nov 2024 19:48:06 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46386c7251234ca16cef7ef7981829cec1c68a31f633038fae82f6fa4bea6548`  
		Last Modified: Thu, 21 Nov 2024 19:23:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:60e2c0bf91ca903330a7cceee1b41c2a1bbdb267bf7b5e4cc9e5a1c2d822c321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:460c835358535ff48139328c022972640ebc869facb7cf89d3ee604273a63765`

```dockerfile
```

-	Layers:
	-	`sha256:8c21f2e4345b18b3fe6f8b8efa0f6ed566833b64e77ca88d1600710a2bfd87fd`  
		Last Modified: Thu, 21 Nov 2024 19:23:21 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:2a2fda30bd0a71491f52d5f8ba6fd1c8b75128d4f453e41948f7d4b6d449b33d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69375719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd54441d7ac9c328c06b46add65b2869b5cf1eba49739aa76e0dbef1e2c8fb51`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2878563f55378e5cb0d2e6fc051acec0bad59706b4c55d991502e489d45f15b9`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 4.9 MB (4894482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1da599409a1b1b855c6d69889b78470128711398dd127ceb61f803c590c9c39`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fec221aedc472ddb77d24345957296ec946aab0b124953af99b1b103ca464d6`  
		Last Modified: Tue, 12 Nov 2024 03:55:37 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46d0dd0a80f3bfa93fe376e12f14d3cf1bf7c86c9c039106b233b8584ec9aac`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 13.6 MB (13572743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d138265234b8809a223e845ff20a559fa757eebafc98f9e9bf724fe8e7dc8b6c`  
		Last Modified: Thu, 21 Nov 2024 18:28:27 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b99f01624e25d17567cb4316e05b197890eaf269e39da90cf62573fc75f8dab`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 17.9 MB (17928178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc46c2ae1e666fefa71dcffefd35978d65be61640f7a3dae1293e1c413955d01`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4995aff739b8938a9a1f51923b6e970cc4d974c131fb8f2f8be37bd64c89bf1e`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 19.5 KB (19454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8371af98339513b427681640d9952ffda9674c0a7837c1f5e1ca4b91fa04e1`  
		Last Modified: Thu, 21 Nov 2024 22:48:27 GMT  
		Size: 28.8 MB (28798173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7861e6ac85a5be9e606f1a0b1ed4b0869e26847132c16ba05c326da3b82f1fb`  
		Last Modified: Thu, 21 Nov 2024 22:48:26 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685e48610c1b40acc2e7489adf5cd45075bc17f1989f32ff40ec88bab369412e`  
		Last Modified: Thu, 21 Nov 2024 22:51:00 GMT  
		Size: 1.1 MB (1062327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f436ad28fae8c9b37d0931ddc038b6260d88038cc84c5bac52a80de62e584f`  
		Last Modified: Mon, 18 Nov 2024 20:23:42 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b313c209ec4a8a313770caaea8ce391741ccc849671d0a07bcca4cba673646`  
		Last Modified: Thu, 21 Nov 2024 22:50:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:7fc4bb9deae034836057b0de9d2cd6e75dd5b12a05fca77bfaa86b783e7219ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a837dc411a94406d400408f2f1e540fc9d76247dfafcc1cbd167c8025c31b39`

```dockerfile
```

-	Layers:
	-	`sha256:e7520a751b99b025d4a994bb6fc0fdb2eec68fd15549efc4ef455996369d7149`  
		Last Modified: Thu, 21 Nov 2024 22:50:59 GMT  
		Size: 2.1 MB (2148108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:568ebb246b0ab7809dc7d276c7da38d3d728e1928d445eab02832dbe5a4493f6`  
		Last Modified: Thu, 21 Nov 2024 22:50:59 GMT  
		Size: 31.1 KB (31062 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:4b882bdbb24c6e89273dc14535bcbd6dab179fc237347ff42a8d62c866bf401f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76081794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7595d594af7fee7f4faf35786a3cb54cbbeeae63a9412e75ee8ce6dc7290c3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8484336630ebb870b45fd46b300831768da17cae91aa6a615fe97d849bf7d9`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 6.0 MB (6047382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f0bf50f7dfd6864235893d3a770f2748c511f29a319b959cd61ab88719f191`  
		Last Modified: Thu, 21 Nov 2024 18:25:40 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4094551f517548ba326fd9610784089231cb5fe7b32fb0fd484b4ef62a06ec4e`  
		Last Modified: Thu, 21 Nov 2024 18:25:40 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f3a19954028229594dc87f84401ff6bb04343f60f6850d3ffd56376584e127`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 13.6 MB (13572746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cec773ac8fce78f9e43c85101520fcc9a1dfd15d5ae6b0086a53ed446c44e83`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c49e3ab1eba1efe295397f466820586f5b4c820bf03494c07afc622cb0d4b80`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 20.4 MB (20379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f558eac651d11a18dc2c9e83c547cfe4241937c5dc84ca0e2f00d0fcc438eb`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec25731eb581dc3064873d8a03e05f5820ff6c09af884fce4b25f79b77d6f34e`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 19.4 KB (19426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7fe1a5fdee0abebec8c80d0770c46acf11edac729c491803ec919a7373c8c`  
		Last Modified: Thu, 21 Nov 2024 22:17:56 GMT  
		Size: 30.9 MB (30879490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0fda769fb77685ab9ff0bd8069d8c4670c1a85af4283162afa7524a8124d45`  
		Last Modified: Thu, 21 Nov 2024 22:17:55 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df9080391afa561614604f21c0161c8bad69d4bc52915415b7c1c65f1bf527a`  
		Last Modified: Thu, 21 Nov 2024 22:19:26 GMT  
		Size: 1.1 MB (1091147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54549015f1d85f07424904365c45002761ecb1f1ed4c44d30ad38297de2a6ebb`  
		Last Modified: Thu, 21 Nov 2024 22:19:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c835e644aa517172a0c42a44439508bef9c61bc21a4f1d5b5adb2285038ce2`  
		Last Modified: Thu, 21 Nov 2024 22:19:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:fd81fa9ab08837460f0bfd44ad469400783f6dd4999ddaf52faf5f9f51b241d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e780c631b16e7f52966897fff323da2a156189b610aae94c8a0a2d4e63eb18`

```dockerfile
```

-	Layers:
	-	`sha256:c5abcc231fd8648f0ce4567486331a77eb7892aaaed996a3a02e655bedbd92c1`  
		Last Modified: Thu, 21 Nov 2024 22:19:26 GMT  
		Size: 2.1 MB (2147938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4482946d0eecf5bd8d0b027fef05ac9b3378a4e06e4b379f48e4c15dc881a886`  
		Last Modified: Thu, 21 Nov 2024 22:19:25 GMT  
		Size: 31.1 KB (31095 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; 386

```console
$ docker pull composer@sha256:5895b27fa42c598668b64122527f1f2aed8003aff127fa28729e1e845ea5c115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56186940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785154b0de710a50fc157f346144c8a62d0b24f291fde96abe6e995b1b34687d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e11d2a2a48dac61e9ac66af5a5b296591c6a200cf9944fd4df55e48749cce57`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 5.5 MB (5468335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3858fed08c63431ed26286b0317883b23277e3ce014a38a3ca7392c05f0e669a`  
		Last Modified: Thu, 21 Nov 2024 18:00:49 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d4c27ab44c7e13de299ad07b09e18b7c98dee3c34fbee400448997573becdb`  
		Last Modified: Thu, 21 Nov 2024 18:00:49 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b25b38e344c1ca4be9ca4235d6cde628e170971af37a03e30f897cf5a758c`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 13.6 MB (13572753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1764d36b8a53c825b53731114444100b7e1bf8a517ab182b4dab438333bee585`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6444425964f24bb27686445f1e394678dae6d912247a4b8f26e4d7b57e90f54`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 21.3 MB (21300265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2465ec415dcb964fc8b6deb3edeeddfb60a77336ebafdeeff9780a230562a2`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b021291a02d8b49460ff1ff13393725cf6e1616dbb1b2a1ef9c7a69fdeab5b4`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 19.6 KB (19644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8aabe33271ab76e9f0a0e14600b67129c22b6376b9ac5691140b583e58214`  
		Last Modified: Thu, 21 Nov 2024 18:10:39 GMT  
		Size: 11.3 MB (11281350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91db55eda861b506210850850e90775ccb8a5505fd86fc292beade07dfeb2c7`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e53d342f08d79d0e95d5cb9b8fdac226218ccd7ac8bfb85a3f8be83b4ca0ec9`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 1.1 MB (1070507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab1b7d6b2a7b5eaffc0c95c278d0bb7c18b20204b2b5eae520c71c7090c6f4a`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb0c74b28b1a5cf47e26e8fec2c840aca547b64a308d1f713a87c93c3561567`  
		Last Modified: Thu, 21 Nov 2024 18:10:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:25307faf2d420c206138ef2b318e90ed0512a70e815b45eda1e66c22d7de7870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.4 KB (452381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f11fa5495a188f46f0b1773d57cd753fb004f768200c8b8c087c3d2872b9cff3`

```dockerfile
```

-	Layers:
	-	`sha256:1adf3a09467edab2b6efdb58c8ac6149ca0ff37d945ac99bb7cf5e9979fbada9`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 421.5 KB (421456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b888a5c47580083cfe521b71b5f008ccfc23b0bfbaae5e6aab7398e655f2374e`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 30.9 KB (30925 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; ppc64le

```console
$ docker pull composer@sha256:b31a01870fb72277be00f9566c0fe6d607c86cb57bdc3c1cb0ead0e0d3fd6e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76958826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7777a78f24315baa2ef132135d753c98210a852f450bcc815b8cb9472767bc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2473147d3bc2923a26c8ba560c425ef2674fbae2edbc29833bb5790c2c94db2`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 5.6 MB (5572572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53975073457162c05af82756884811d86cf52d05953b0589749a216a80864431`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58037573bd03f9687676a3398cb715ac628a3bc280f63aa990e8171ef59ce1c9`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f80183c138cedf9dc24420caf7f9769369bf61c8db0eb09729c4303c31ba1b`  
		Last Modified: Thu, 21 Nov 2024 18:14:28 GMT  
		Size: 13.6 MB (13572757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1746563bd5a8883ee2e1758e12423a999df46412bbeb663f9f774dc595e96ed`  
		Last Modified: Thu, 21 Nov 2024 18:14:27 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3428ebe5f2568169c292765c92b0cc55c0ef85fc46ab1c4d0b60b2d86970b4b3`  
		Last Modified: Thu, 21 Nov 2024 18:14:29 GMT  
		Size: 21.7 MB (21712721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f8424c24e908ec0192f8ff40322e44264734608539de7427be91c3398884dc`  
		Last Modified: Thu, 21 Nov 2024 18:14:27 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef3b5629726f19111a47ee6dc86f22265d0002270ef68da5bb572a2fa8a6d04`  
		Last Modified: Thu, 21 Nov 2024 18:14:28 GMT  
		Size: 19.4 KB (19424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf7d67a2a72f10bea3ee74b2250affb6d2de6aac3751149e9003e6b4ff24a2e`  
		Last Modified: Thu, 21 Nov 2024 21:22:37 GMT  
		Size: 31.4 MB (31402451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011cd0419150962df2f83f6c5e96043ca7df1ddb5a812e226d6f2b98814c7fc0`  
		Last Modified: Thu, 21 Nov 2024 21:22:35 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac37fe451ac8534aca4e4e40851e92cc0468a5064576179550c5594bf87157e4`  
		Last Modified: Thu, 21 Nov 2024 21:24:48 GMT  
		Size: 1.1 MB (1101560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14909c3d44cb9216423277a8fff5ce20356c2f7170dff5ae30ad76fa2fe58235`  
		Last Modified: Thu, 21 Nov 2024 21:24:47 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d2063201f1a57cceae80e31658ce1e97b597798722a7ce1a5b6bcf68c9b206`  
		Last Modified: Thu, 21 Nov 2024 21:24:47 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:abcbb063050d224d69d1489b752b0227a8f5e4144d73f0b691f10f5296f85514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b35bdb873177e2ab223c603904bbaca948a7a86b161653ed30eec8a261bc67`

```dockerfile
```

-	Layers:
	-	`sha256:c725c209387c0493e239864a94db3246df808fee3270bc3de3c86bc19e6a398e`  
		Last Modified: Thu, 21 Nov 2024 21:24:48 GMT  
		Size: 2.1 MB (2146342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a73619b309ab318681d8ac6c230f818f2b6cc6f8475cef18f95a964e7b2c8b1`  
		Last Modified: Thu, 21 Nov 2024 21:24:47 GMT  
		Size: 31.0 KB (31007 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; riscv64

```console
$ docker pull composer@sha256:ed8bec923846612aeec9d7c5b4e37d4c27b46e61083ef994d73edacc353eb451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70713138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bbd153b3fff08b930c02c40db9c3bede384367eb09e013935beca56ef232ae`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8ca85c9d20c6f76d0a8087ac3a4ddd6a1e40652d189dc8dad7ca6b0737c4b0`  
		Last Modified: Tue, 12 Nov 2024 06:14:49 GMT  
		Size: 5.4 MB (5382174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d2dfe107b4bddcc389bedcee9ca3fc81f02dc0799e313c21f307ddb454b4dc`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df7310166e795cb48e721a885b92af688db981613ad6597943011293aca738c`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626cc5aa152e22cd453ede74c922b963a3bc8a4bcf66d8a4763c977a36db9bbf`  
		Last Modified: Tue, 12 Nov 2024 11:38:11 GMT  
		Size: 12.5 MB (12504597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e68d6f9ff3ad2f5f92d5d2e1da7c8e8e8c7acf26714c65fb1634379b0ceabea`  
		Last Modified: Tue, 12 Nov 2024 11:38:08 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7ef4ac959dd31d8a66fcf270291f1312424b277d8adec2eded58a835d3130c`  
		Last Modified: Tue, 12 Nov 2024 11:38:11 GMT  
		Size: 16.8 MB (16791439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f9910ad73e6186422edca968a56743133f52309ae7e8fbfaeba5689ec14ce1`  
		Last Modified: Tue, 12 Nov 2024 11:38:08 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cccb83ba6c8bd3926d00dba2c6475d1639c61ec7b4dc48a094f44e9ef2d363f`  
		Last Modified: Tue, 12 Nov 2024 11:38:10 GMT  
		Size: 19.4 KB (19444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1184794faa4cb72388841b6ca5edd801726298f1bc7a901384a6611a072b84d`  
		Last Modified: Wed, 13 Nov 2024 13:17:47 GMT  
		Size: 30.8 MB (30811150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0835e0d761497dfe92dfd2f01937792ca5c678bba375a232324b9fbb0ba5120`  
		Last Modified: Wed, 13 Nov 2024 13:17:42 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07c683546f1dbb73a401c02ec6169c6db9a2e1163a15f184d5c634965a1e5db`  
		Last Modified: Mon, 18 Nov 2024 19:11:38 GMT  
		Size: 1.8 MB (1827970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db5e9fa9e94a1dfd1dbce4db1c03e977d7ef88c4265803e7fb16536ce3901bb`  
		Last Modified: Mon, 18 Nov 2024 19:11:38 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bb7be447bc29d4901509e73b2e709bbfe7daf883f9dc94e2f83ca774cdf247`  
		Last Modified: Mon, 18 Nov 2024 19:11:38 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:699f6536b8af5d06e22a6567155fa157b1c7ee6de20657fe2bfb50c733e9138c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07826998165fa93f84ac501d6a553f14a3c873f356bcdbd20cdb0d1875832fca`

```dockerfile
```

-	Layers:
	-	`sha256:ff4fae5f5ec59bf9f691ec534e5babfe3171a3fe2db50fe20bfe894d62bbc67f`  
		Last Modified: Mon, 18 Nov 2024 19:11:37 GMT  
		Size: 2.1 MB (2145960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e221ef006b10f92faeefea08445fba63054cfdf42a7de63decab79954c796f3`  
		Last Modified: Mon, 18 Nov 2024 19:11:37 GMT  
		Size: 31.0 KB (31018 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; s390x

```console
$ docker pull composer@sha256:e21dca9bf0b9c7065a2aef60fc6a0e3a03a86445503700c9eff2f48792a80f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76278627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0683d3d3b3aceba01f85e8de7138bb8723ea04c6b816570cce7dc9310f0a4973`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 18 Nov 2024 08:33:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 18 Nov 2024 08:33:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_VERSION=8.4.1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Mon, 18 Nov 2024 08:33:38 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["php" "-a"]
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 18 Nov 2024 08:33:38 GMT
ENV COMPOSER_VERSION=2.8.3
# Mon, 18 Nov 2024 08:33:38 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 18 Nov 2024 08:33:38 GMT
WORKDIR /app
# Mon, 18 Nov 2024 08:33:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Nov 2024 08:33:38 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26915a92034b18e2de9232a415d1ad92dc1c7a9f9e2b5bb9c590ce4c503ab73e`  
		Last Modified: Tue, 12 Nov 2024 03:39:27 GMT  
		Size: 5.5 MB (5532119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4041b6d620078267a8ee6dd6b9c31735d82dee5f22aa96467865a8134d616c`  
		Last Modified: Tue, 12 Nov 2024 03:39:26 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5555efb309fc5275c2fd44eabaaf4ca859f01b510ef24cbad6009d7ed6dc4696`  
		Last Modified: Tue, 12 Nov 2024 03:39:26 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ebcb70bd65f646a0a9f4f475ec50ab3b189c26c5453f7261bc927c566c16f4`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 13.6 MB (13572754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1fe669f736130225879d8f3a94b1a2dc84c8a542232c1010d5c0efdfb490ab`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ebb202afe7221a69abb8b0e5dd9a734085f863f2a450dd0794f4e1c6bc5189`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 21.3 MB (21250100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7a60154e6bcac48ec5bae22b14f7b46c6200a532944883ccb70d97a5f9ff15`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76035e400728cb3a6c7bd01204127072929a705a4be9f5ab31588ec5dce5bd70`  
		Last Modified: Thu, 21 Nov 2024 18:24:27 GMT  
		Size: 19.4 KB (19435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391e13c55cb9dd9b3adaa2c815b5a344bfd110a0afc12b82e71ba8af9327a7a3`  
		Last Modified: Thu, 21 Nov 2024 21:24:03 GMT  
		Size: 31.3 MB (31338617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d1aea81c97d878724863520afce631476bbf2f86f4eaf2a4b781b5d4f855ba`  
		Last Modified: Thu, 21 Nov 2024 21:24:02 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec41f417f32df8d6b29087fb50d7165f6ba5622272536044aad8346263321cd`  
		Last Modified: Thu, 21 Nov 2024 21:25:56 GMT  
		Size: 1.1 MB (1099124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d41623169f490a3c4b3ad708f3715985370d656560af18567d32dad796bd601`  
		Last Modified: Thu, 21 Nov 2024 21:25:56 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103104b2577b229e90d735ad3b6db3d300d26fd3f7bd0aa3cacbcaf87380344b`  
		Last Modified: Thu, 21 Nov 2024 21:25:56 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:fd2bbd770d3c98acb45d0ea2760f1f299ef68190c3ee369a618a74f8008cab4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ec6c9d823e50f933620ebd04ef4de684361b80bd7821ee35d672f7c6349d57`

```dockerfile
```

-	Layers:
	-	`sha256:f718eb8ddf8df0e06b8bf814924ded8904373825b635c0fd316aac4860492380`  
		Last Modified: Thu, 21 Nov 2024 21:25:55 GMT  
		Size: 2.1 MB (2145738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f05d0590058fbabd4f7c681b6947c6efbf8ba4a06a51353d3354d9ce6a0898e9`  
		Last Modified: Thu, 21 Nov 2024 21:25:55 GMT  
		Size: 31.0 KB (30960 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:lts`

```console
$ docker pull composer@sha256:866ce87175721248614af82d38ec0283d5a4ebe482597a4c934a17f39665ff31
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
$ docker pull composer@sha256:dc762de077b409c57a93053b4c9303c9df0013dc2e0cf8caec8e7a98304d098a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74873742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8389298d00edb2bcb0b6243707d46a3c8ab03c563603743a6a5243275044d0ea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
ENV COMPOSER_VERSION=2.2.24
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4026d1cc5245f59e156bffd596323974be67dd48771842c57ace1b9fcb840`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 5.6 MB (5583566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca19f9a3dd1a82729217796a0e8ef626bd25c881db51316ae1d7b6baca3c979`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d429435d57d0d3420a2bb847cb1a04a76483e18d14ae4486b653e998810c2dc8`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22359169dee3cb23309dde8b4845f0a26d5ced82572690f0ec5de9aa5c37df6b`  
		Last Modified: Thu, 21 Nov 2024 18:00:31 GMT  
		Size: 13.6 MB (13572755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60636de7ac448f3bfc52c2d3f3fbdd7e572b65b45a980647e217005c89f46ddd`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6574e97188f3a55184dd55cbc3377b5b1826fe8ac69257fc044d8d1826cf62a`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 20.8 MB (20763608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0db01ff42c14dc52ac7bd7aad09e0a0e2b0050a0ad2796a55eb92246ce39d2`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e12f7079c7bc22fa3df852b4eebe6e7b01a834b3924a0f365f1b0f3437b7eab`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 19.7 KB (19661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a51e94714c8707792f4fe23ad049a8c12d8c33818884fed28112530e7679ee`  
		Last Modified: Thu, 21 Nov 2024 18:10:43 GMT  
		Size: 30.4 MB (30368546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a05dba902617c5f7d56484efb2943e96ba560201b89894283f4d43629c97e65`  
		Last Modified: Thu, 21 Nov 2024 18:10:42 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134c7a64e8423974fb4f1b7984b0947b14c8c0098961eaaa880f6113b57ee2e4`  
		Last Modified: Thu, 21 Nov 2024 18:10:42 GMT  
		Size: 936.8 KB (936842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab1b7d6b2a7b5eaffc0c95c278d0bb7c18b20204b2b5eae520c71c7090c6f4a`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530ddf2e2ea7376256a341344b97cc0f2b1396e7f8f5a1296888287563aa6963`  
		Last Modified: Thu, 21 Nov 2024 18:10:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:427486cb9a9cc4770140df4a865ac9bdcbebbddca4187b8afbfe43e421e51b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24a49d1b9b079f6b20225dfeec273cf989e2a364f038c07efdf39d1d3b7da57`

```dockerfile
```

-	Layers:
	-	`sha256:5fbc3c664e2d90fbc69a9f92c84bcad5b769bceb74bbc163a02db1af37d5a02b`  
		Last Modified: Thu, 21 Nov 2024 18:10:42 GMT  
		Size: 2.1 MB (2147493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4f6ce00b6b55144638e0c8b483672b5fb6e6a070f49ad3661bffd5bdd73c46e`  
		Last Modified: Thu, 21 Nov 2024 18:10:42 GMT  
		Size: 30.7 KB (30652 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v6

```console
$ docker pull composer@sha256:5d3fddde44dd2cd61f0d23563881c665ebc0367cac5324307be2ff2668c9d71c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97eb5a11a9dcc19751c3533f8d6ac939b83e0370fa4e1cbaed86ee4b9d7571ba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
ENV COMPOSER_VERSION=2.2.24
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
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdae56950198dea1248e6f62d7e9ef311c976d55790449240dfa46ad43351f7`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 5.2 MB (5236002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773d98c98ade13dc692eaf9700be32a03220033d99905be410eda923ce054fb9`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ae964d3deb57dca49dadfc5c487d64a372e3df3db6ef51b58087c318beb33d`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851605dfb3d928a53fef3860db97edb0f94316d382df472a9f36d31603ae85dc`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 13.6 MB (13572750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb476219577608ba4633ce4f2bf10a95d8fd1bd1bb56c2fb972587e5207cb3f`  
		Last Modified: Thu, 21 Nov 2024 17:58:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698c845cc5fd3760e20d315377bdca792a2b899c35f1288b5ddf2bf66c3e10d4`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 19.0 MB (19027128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7c3d46b7180237d2a402261f2cb181901e0149fed38e5a97d2214f64ba90ac`  
		Last Modified: Thu, 21 Nov 2024 17:58:04 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72176ade970c8f4af9d251ca5d0fc1aefd6e0fa47866d9d792bf9e85a4ac16c`  
		Last Modified: Thu, 21 Nov 2024 17:58:05 GMT  
		Size: 19.4 KB (19437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487dce5effb993971148992fe8918fe413df14e91c1a17c2d7a26c254d6a7b29`  
		Last Modified: Thu, 21 Nov 2024 19:21:58 GMT  
		Size: 29.2 MB (29169296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812056dc604d2f3d588dcb3b1441239d4f3a938f21cabe40a0c26a26245a6f23`  
		Last Modified: Thu, 21 Nov 2024 19:21:57 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7497c4d4ec772fa3b0fe4c24787719f3009da03a55d3e2519d0318541a2b33`  
		Last Modified: Thu, 21 Nov 2024 19:21:57 GMT  
		Size: 936.6 KB (936627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfd7c969e59b509cbb25d238f775b14f1f6de06c8c50f7b1c7b89909f9e76f3`  
		Last Modified: Thu, 14 Nov 2024 17:27:32 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f195f1c45af65d274b33527994a259f4b7a050670692edb404032c41ff63f11`  
		Last Modified: Thu, 21 Nov 2024 19:21:57 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:b454fc6978324f0e883d0bb957b0068c82dae159d4d129ec6ac6db2d34a44707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76189ed6a5eecb149a77520fe8706d4c4907ededeb6abb684ee878077978e24`

```dockerfile
```

-	Layers:
	-	`sha256:adffb95fbb5eedc669bf68d35ba3f4f66ea43d23b83cf287e0329552b301a55d`  
		Last Modified: Thu, 21 Nov 2024 19:21:57 GMT  
		Size: 30.5 KB (30533 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v7

```console
$ docker pull composer@sha256:f8e498f2e26f567fcb79922e01ba79a45e49e7d9262646c2ecaecccc443a73d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69228978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1e7b630fcfdc911cb231185a630a3faf1d8ddc258a1ce889ae74b8968bc620`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
ENV COMPOSER_VERSION=2.2.24
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
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2878563f55378e5cb0d2e6fc051acec0bad59706b4c55d991502e489d45f15b9`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 4.9 MB (4894482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1da599409a1b1b855c6d69889b78470128711398dd127ceb61f803c590c9c39`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fec221aedc472ddb77d24345957296ec946aab0b124953af99b1b103ca464d6`  
		Last Modified: Tue, 12 Nov 2024 03:55:37 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46d0dd0a80f3bfa93fe376e12f14d3cf1bf7c86c9c039106b233b8584ec9aac`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 13.6 MB (13572743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d138265234b8809a223e845ff20a559fa757eebafc98f9e9bf724fe8e7dc8b6c`  
		Last Modified: Thu, 21 Nov 2024 18:28:27 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b99f01624e25d17567cb4316e05b197890eaf269e39da90cf62573fc75f8dab`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 17.9 MB (17928178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc46c2ae1e666fefa71dcffefd35978d65be61640f7a3dae1293e1c413955d01`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4995aff739b8938a9a1f51923b6e970cc4d974c131fb8f2f8be37bd64c89bf1e`  
		Last Modified: Thu, 21 Nov 2024 18:28:28 GMT  
		Size: 19.5 KB (19454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8371af98339513b427681640d9952ffda9674c0a7837c1f5e1ca4b91fa04e1`  
		Last Modified: Thu, 21 Nov 2024 22:48:27 GMT  
		Size: 28.8 MB (28798173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7861e6ac85a5be9e606f1a0b1ed4b0869e26847132c16ba05c326da3b82f1fb`  
		Last Modified: Thu, 21 Nov 2024 22:48:26 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493012c5a6547efbc494430af25dc80173bdee3d4f60c42496ec50457df6ee8e`  
		Last Modified: Thu, 21 Nov 2024 22:48:26 GMT  
		Size: 915.6 KB (915587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4392e1df0c627db8659fec8b11584d88798ed80206abb5707f07ac537fdec26f`  
		Last Modified: Thu, 21 Nov 2024 22:48:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a877678fb5fdddb712b0d3f125aa9c71483cd9a72e87d956cbc6d3c1a0d43003`  
		Last Modified: Thu, 21 Nov 2024 22:48:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:93a5382e61fae1a22af7feaf5926451001d52b6ee69b48f3cd02656650c8905f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be5cfbbb520154ede402a8b2bce4eeb128b5983b98576b83b1be1f431273049`

```dockerfile
```

-	Layers:
	-	`sha256:6e70796a377912ba45dc355bf19d5f930f74024d0f0a96d058461b113b885846`  
		Last Modified: Thu, 21 Nov 2024 22:48:26 GMT  
		Size: 2.1 MB (2147806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94eb33295a673f22586e4880fb2c8b1bc5a7d9074c7d77a3a4feb1331ccb44f8`  
		Last Modified: Thu, 21 Nov 2024 22:48:26 GMT  
		Size: 30.7 KB (30748 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:6a7a0690deae00e521fbdc9abc37d053db84f33c37f60bbd2a76542f81a4ae20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75938195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c09cf1b1acc463d7d133b00d9026e35b99fb7074d7631b64aebff8f07d60a45`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
ENV COMPOSER_VERSION=2.2.24
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8484336630ebb870b45fd46b300831768da17cae91aa6a615fe97d849bf7d9`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 6.0 MB (6047382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f0bf50f7dfd6864235893d3a770f2748c511f29a319b959cd61ab88719f191`  
		Last Modified: Thu, 21 Nov 2024 18:25:40 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4094551f517548ba326fd9610784089231cb5fe7b32fb0fd484b4ef62a06ec4e`  
		Last Modified: Thu, 21 Nov 2024 18:25:40 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f3a19954028229594dc87f84401ff6bb04343f60f6850d3ffd56376584e127`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 13.6 MB (13572746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cec773ac8fce78f9e43c85101520fcc9a1dfd15d5ae6b0086a53ed446c44e83`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c49e3ab1eba1efe295397f466820586f5b4c820bf03494c07afc622cb0d4b80`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 20.4 MB (20379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f558eac651d11a18dc2c9e83c547cfe4241937c5dc84ca0e2f00d0fcc438eb`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec25731eb581dc3064873d8a03e05f5820ff6c09af884fce4b25f79b77d6f34e`  
		Last Modified: Thu, 21 Nov 2024 18:25:42 GMT  
		Size: 19.4 KB (19426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7fe1a5fdee0abebec8c80d0770c46acf11edac729c491803ec919a7373c8c`  
		Last Modified: Thu, 21 Nov 2024 22:17:56 GMT  
		Size: 30.9 MB (30879490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0fda769fb77685ab9ff0bd8069d8c4670c1a85af4283162afa7524a8124d45`  
		Last Modified: Thu, 21 Nov 2024 22:17:55 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f33051432a42a11aba731651d6de55d39d9cdd3cc6a9ee26fe125092bbab68`  
		Last Modified: Thu, 21 Nov 2024 22:17:55 GMT  
		Size: 947.5 KB (947547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98c7eaba8d2c0a247642ab1c9e0449c3cc021987330f4a78cf55ae835d29b8e`  
		Last Modified: Thu, 21 Nov 2024 22:17:55 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e561633f2696555e9d601463322eacf04773b731ea444ab8e0e6160cc0418c1a`  
		Last Modified: Thu, 21 Nov 2024 22:17:56 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:529a741ae63ece5d98a696c6b61c47a843e189793224c089e0670d874e4dcca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3aecefe174e213dcaed558732318f846414c8383d7f9393ec4bbc8ad995df3a`

```dockerfile
```

-	Layers:
	-	`sha256:c0f692a03747088c081f0800650c9c02867608bdad123c81327dd94eb8f36d70`  
		Last Modified: Thu, 21 Nov 2024 22:17:55 GMT  
		Size: 2.1 MB (2147632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4daafc04a8ce3d201a57dff3ff09817354cc6c17883846c105b4a5e84266d191`  
		Last Modified: Thu, 21 Nov 2024 22:17:54 GMT  
		Size: 30.8 KB (30776 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; 386

```console
$ docker pull composer@sha256:26ecdb5228c9c79d03ae95862c22f997a5431202e354672b511b39d06256f0ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56040857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b97a1ae6ba8ad901380c00b3583a29d2db0eda0d322697b1fa14a259d64055`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
ENV COMPOSER_VERSION=2.2.24
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
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e11d2a2a48dac61e9ac66af5a5b296591c6a200cf9944fd4df55e48749cce57`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 5.5 MB (5468335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3858fed08c63431ed26286b0317883b23277e3ce014a38a3ca7392c05f0e669a`  
		Last Modified: Thu, 21 Nov 2024 18:00:49 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d4c27ab44c7e13de299ad07b09e18b7c98dee3c34fbee400448997573becdb`  
		Last Modified: Thu, 21 Nov 2024 18:00:49 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b25b38e344c1ca4be9ca4235d6cde628e170971af37a03e30f897cf5a758c`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 13.6 MB (13572753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1764d36b8a53c825b53731114444100b7e1bf8a517ab182b4dab438333bee585`  
		Last Modified: Thu, 21 Nov 2024 18:00:50 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6444425964f24bb27686445f1e394678dae6d912247a4b8f26e4d7b57e90f54`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 21.3 MB (21300265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2465ec415dcb964fc8b6deb3edeeddfb60a77336ebafdeeff9780a230562a2`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b021291a02d8b49460ff1ff13393725cf6e1616dbb1b2a1ef9c7a69fdeab5b4`  
		Last Modified: Thu, 21 Nov 2024 18:00:51 GMT  
		Size: 19.6 KB (19644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8aabe33271ab76e9f0a0e14600b67129c22b6376b9ac5691140b583e58214`  
		Last Modified: Thu, 21 Nov 2024 18:10:39 GMT  
		Size: 11.3 MB (11281350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91db55eda861b506210850850e90775ccb8a5505fd86fc292beade07dfeb2c7`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c53d73674dfa5d4b800403e9b1074300aa872923a0c9a430947bb23e7e169c`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 924.4 KB (924424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84b9390ed421034bdf6edeb19bc83a8d787f4901717254b650b67efe6ca93f2`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb0c74b28b1a5cf47e26e8fec2c840aca547b64a308d1f713a87c93c3561567`  
		Last Modified: Thu, 21 Nov 2024 18:10:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:5a2d48203435ea9b05d1087dd9768863722f2a77305e6f836cb4b74c9d66e6e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.8 KB (451790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b9ac7e897bad079a57c6656ba0079217b3d28729d975aa9eaf191ba42e18ed`

```dockerfile
```

-	Layers:
	-	`sha256:9b26e2ba6aa29a86cf02b0a9b2a3c5457147c9cdd03e915b3b132b74977f595f`  
		Last Modified: Thu, 21 Nov 2024 18:10:38 GMT  
		Size: 421.2 KB (421167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6f68dfe539c0913cdec1a101a80c7ce9850e0ce82e81fcca23972e41de1fdae`  
		Last Modified: Thu, 21 Nov 2024 18:10:37 GMT  
		Size: 30.6 KB (30623 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; ppc64le

```console
$ docker pull composer@sha256:273ef0b791c27b94c856cdf8854312e8f1fee0a8533ea12299bd033053aee9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76814960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89dedefde6c35d833333272a0f72fd082f233bbc63f2260b86fee1fbf2a05fc4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
ENV COMPOSER_VERSION=2.2.24
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
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2473147d3bc2923a26c8ba560c425ef2674fbae2edbc29833bb5790c2c94db2`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 5.6 MB (5572572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53975073457162c05af82756884811d86cf52d05953b0589749a216a80864431`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58037573bd03f9687676a3398cb715ac628a3bc280f63aa990e8171ef59ce1c9`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f80183c138cedf9dc24420caf7f9769369bf61c8db0eb09729c4303c31ba1b`  
		Last Modified: Thu, 21 Nov 2024 18:14:28 GMT  
		Size: 13.6 MB (13572757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1746563bd5a8883ee2e1758e12423a999df46412bbeb663f9f774dc595e96ed`  
		Last Modified: Thu, 21 Nov 2024 18:14:27 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3428ebe5f2568169c292765c92b0cc55c0ef85fc46ab1c4d0b60b2d86970b4b3`  
		Last Modified: Thu, 21 Nov 2024 18:14:29 GMT  
		Size: 21.7 MB (21712721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f8424c24e908ec0192f8ff40322e44264734608539de7427be91c3398884dc`  
		Last Modified: Thu, 21 Nov 2024 18:14:27 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef3b5629726f19111a47ee6dc86f22265d0002270ef68da5bb572a2fa8a6d04`  
		Last Modified: Thu, 21 Nov 2024 18:14:28 GMT  
		Size: 19.4 KB (19424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf7d67a2a72f10bea3ee74b2250affb6d2de6aac3751149e9003e6b4ff24a2e`  
		Last Modified: Thu, 21 Nov 2024 21:22:37 GMT  
		Size: 31.4 MB (31402451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011cd0419150962df2f83f6c5e96043ca7df1ddb5a812e226d6f2b98814c7fc0`  
		Last Modified: Thu, 21 Nov 2024 21:22:35 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f739c523c65801d9bf3a3512b64f2a819fb4533b819d382f1b5236a2ab0fb79`  
		Last Modified: Thu, 21 Nov 2024 21:22:36 GMT  
		Size: 957.7 KB (957693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ee41244fae528c8ba994c3f0c062d5063890d34b2b13f37417073f4e4abb20`  
		Last Modified: Thu, 21 Nov 2024 21:22:36 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb5d18c4f4e6134f2c4406383a1debea61cefc8dd4a5da7a59075c1ada07832`  
		Last Modified: Thu, 21 Nov 2024 21:22:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:5aa5e9f65405cd9a12eb9dd2b99fe48646e40b7aefdb630ddc0e0f75997e7a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80f49cfb840ebf4f850dba9467d0efb1d6b82b91f1586b93a7df1f84500413b`

```dockerfile
```

-	Layers:
	-	`sha256:d07b44100f7897664a442a7aff9c544144d8bc29a038de7cba4329f3d908f62b`  
		Last Modified: Thu, 21 Nov 2024 21:22:36 GMT  
		Size: 2.1 MB (2146042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:917db0d38ca1fa32a3425dd85715d616780fa2374048dd32b9c01757c2601999`  
		Last Modified: Thu, 21 Nov 2024 21:22:35 GMT  
		Size: 30.7 KB (30696 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; riscv64

```console
$ docker pull composer@sha256:3ddd4f307e73eb3bcde94c20848064553bd21d845bfd4b7ff551d8f352aad3bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69829962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10f76d711de731796de0a4a395f77b1447f8431b1d58b8fdb2c3cce859ee3fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
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
ENV COMPOSER_VERSION=2.2.24
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
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8ca85c9d20c6f76d0a8087ac3a4ddd6a1e40652d189dc8dad7ca6b0737c4b0`  
		Last Modified: Tue, 12 Nov 2024 06:14:49 GMT  
		Size: 5.4 MB (5382174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d2dfe107b4bddcc389bedcee9ca3fc81f02dc0799e313c21f307ddb454b4dc`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df7310166e795cb48e721a885b92af688db981613ad6597943011293aca738c`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626cc5aa152e22cd453ede74c922b963a3bc8a4bcf66d8a4763c977a36db9bbf`  
		Last Modified: Tue, 12 Nov 2024 11:38:11 GMT  
		Size: 12.5 MB (12504597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e68d6f9ff3ad2f5f92d5d2e1da7c8e8e8c7acf26714c65fb1634379b0ceabea`  
		Last Modified: Tue, 12 Nov 2024 11:38:08 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7ef4ac959dd31d8a66fcf270291f1312424b277d8adec2eded58a835d3130c`  
		Last Modified: Tue, 12 Nov 2024 11:38:11 GMT  
		Size: 16.8 MB (16791439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f9910ad73e6186422edca968a56743133f52309ae7e8fbfaeba5689ec14ce1`  
		Last Modified: Tue, 12 Nov 2024 11:38:08 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cccb83ba6c8bd3926d00dba2c6475d1639c61ec7b4dc48a094f44e9ef2d363f`  
		Last Modified: Tue, 12 Nov 2024 11:38:10 GMT  
		Size: 19.4 KB (19444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1184794faa4cb72388841b6ca5edd801726298f1bc7a901384a6611a072b84d`  
		Last Modified: Wed, 13 Nov 2024 13:17:47 GMT  
		Size: 30.8 MB (30811150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0835e0d761497dfe92dfd2f01937792ca5c678bba375a232324b9fbb0ba5120`  
		Last Modified: Wed, 13 Nov 2024 13:17:42 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c554724d42fde604b2c035bae323f605a4cc0c9636d7bdfcbd0f7314063855c`  
		Last Modified: Thu, 14 Nov 2024 17:31:54 GMT  
		Size: 944.8 KB (944794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f996300435f6471be064e050bb5d21dbc2a9d7e12bfb48c5581ffb7091600e`  
		Last Modified: Thu, 14 Nov 2024 17:31:53 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd23ffb62d5751d22ddc4bfc9f5abe311dd9d793f5b461d065fb0f50fe4e9d2e`  
		Last Modified: Thu, 14 Nov 2024 17:31:53 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:2d88e8f1faac4e0669dfc54e81e569dd1591b97c410c04f461aed8935e8e7a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf3466f3664bd0ac8832b3717e606b2c1acbb35c1ffff936f34501c3ffabfb5`

```dockerfile
```

-	Layers:
	-	`sha256:ef84f869596117d88e713b7a48ac2a4701961f87f93ecca1a1616ec550b671f1`  
		Last Modified: Thu, 14 Nov 2024 17:31:53 GMT  
		Size: 2.1 MB (2145659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e828aa65c76f40f9e116367e305f3d9196b226f3824fe9e59c2ec1836e46489e`  
		Last Modified: Thu, 14 Nov 2024 17:31:53 GMT  
		Size: 30.7 KB (30705 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; s390x

```console
$ docker pull composer@sha256:0b741a73b3c522adafb8efb5dd9991126e70a4192f5e2055ccb7f1db027117f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76135045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffebc5d710dc20bfb62fe4a32c3df2b531aed5feecb67ac1d8f2d058dcf31485`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
ENV COMPOSER_VERSION=2.2.24
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
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26915a92034b18e2de9232a415d1ad92dc1c7a9f9e2b5bb9c590ce4c503ab73e`  
		Last Modified: Tue, 12 Nov 2024 03:39:27 GMT  
		Size: 5.5 MB (5532119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4041b6d620078267a8ee6dd6b9c31735d82dee5f22aa96467865a8134d616c`  
		Last Modified: Tue, 12 Nov 2024 03:39:26 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5555efb309fc5275c2fd44eabaaf4ca859f01b510ef24cbad6009d7ed6dc4696`  
		Last Modified: Tue, 12 Nov 2024 03:39:26 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ebcb70bd65f646a0a9f4f475ec50ab3b189c26c5453f7261bc927c566c16f4`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 13.6 MB (13572754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1fe669f736130225879d8f3a94b1a2dc84c8a542232c1010d5c0efdfb490ab`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ebb202afe7221a69abb8b0e5dd9a734085f863f2a450dd0794f4e1c6bc5189`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 21.3 MB (21250100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7a60154e6bcac48ec5bae22b14f7b46c6200a532944883ccb70d97a5f9ff15`  
		Last Modified: Thu, 21 Nov 2024 18:24:26 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76035e400728cb3a6c7bd01204127072929a705a4be9f5ab31588ec5dce5bd70`  
		Last Modified: Thu, 21 Nov 2024 18:24:27 GMT  
		Size: 19.4 KB (19435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391e13c55cb9dd9b3adaa2c815b5a344bfd110a0afc12b82e71ba8af9327a7a3`  
		Last Modified: Thu, 21 Nov 2024 21:24:03 GMT  
		Size: 31.3 MB (31338617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d1aea81c97d878724863520afce631476bbf2f86f4eaf2a4b781b5d4f855ba`  
		Last Modified: Thu, 21 Nov 2024 21:24:02 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4b1710f0705434f4bdcfd8d31140ef64468bb215062f4232b1b6b2b71deb62`  
		Last Modified: Thu, 21 Nov 2024 21:24:03 GMT  
		Size: 955.5 KB (955542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2795ba63978bfd04dfd9f48b1785eee03271dc472997f51d05ef1849ec33eda`  
		Last Modified: Thu, 21 Nov 2024 21:24:03 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda486a2686c7739a4087ac185e265c1bbe289f9a216ae45f54d2fa1d70b166b`  
		Last Modified: Thu, 21 Nov 2024 21:24:03 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:c2dbb513828951cee5931de5174febf1f6f07891e09131182da48b5269dacca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e69f8a7720a8658448cb346da5858583df53531e480d6571ecfe8a889bf8acc4`

```dockerfile
```

-	Layers:
	-	`sha256:434bb7bdf557e614bb7a8c41785a7d34764404cbc3e97f086f9765241b008839`  
		Last Modified: Thu, 21 Nov 2024 21:24:02 GMT  
		Size: 2.1 MB (2145444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3942678f500c80f758b086ace61ac759e021e60b71716fa73621828abae3ac09`  
		Last Modified: Thu, 21 Nov 2024 21:24:02 GMT  
		Size: 30.7 KB (30654 bytes)  
		MIME: application/vnd.in-toto+json
