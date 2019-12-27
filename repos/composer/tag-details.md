<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `composer`

-	[`composer:1`](#composer1)
-	[`composer:1.8`](#composer18)
-	[`composer:1.8.6`](#composer186)
-	[`composer:1.9`](#composer19)
-	[`composer:1.9.1`](#composer191)
-	[`composer:latest`](#composerlatest)

## `composer:1`

```console
$ docker pull composer@sha256:75a6a13680d0be7074f1c52f78f508751258d002c6e3934a7d5c332739f2b201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `composer:1` - linux; amd64

```console
$ docker pull composer@sha256:fdbee4b29a1bcca79b12fdced7d9221eb6cc28832b9e00ab2e7c6726f20ca8cc
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66206861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02efded7ec8009b7a35bf247573592efffbe0f382d3c0e3dd07becb80565505`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:47:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 21:47:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 21:47:52 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 21:47:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 21:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 21:47:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:47:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:47:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 21:47:55 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 21:47:55 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 21:47:55 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 21:47:55 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 21:47:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 21:47:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:55:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 21:55:56 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:55:58 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 21:55:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 21:55:58 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 03:48:37 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 03:48:47 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 03:48:47 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 03:48:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 03:48:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 03:48:48 GMT
ENV COMPOSER_VERSION=1.9.1
# Fri, 27 Dec 2019 03:48:49 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 03:48:49 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 03:48:49 GMT
WORKDIR /app
# Fri, 27 Dec 2019 03:48:50 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 03:48:50 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7a574e8632727fe466d1871c39e4fea951243dc9f0a56bdc55cb8720f4aac6`  
		Last Modified: Thu, 26 Dec 2019 23:05:01 GMT  
		Size: 1.4 MB (1354713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6c65f587e94ae6bd946a70d456e75c7543d38cb03271622a815f3b5398ec74`  
		Last Modified: Thu, 26 Dec 2019 23:05:00 GMT  
		Size: 1.2 KB (1227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba33e4b639bb4e1187590b34ea007a27393fbda41d6f3ad10d04c9a0bd1cde4a`  
		Last Modified: Thu, 26 Dec 2019 23:05:00 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94182f10949f8b172016cbddea1d7b4417514c40d0fd664a0895d3b0f93fcbe`  
		Last Modified: Thu, 26 Dec 2019 23:05:00 GMT  
		Size: 10.3 MB (10264403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06b2b4baeabcdc2692442b4f6a6512b1f6b20697c8ec9b984503705cc81039a`  
		Last Modified: Thu, 26 Dec 2019 23:04:59 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6abb9ac3b49074e4561b65dbf3c4beaab0b50ef72743a04656dd6e664bcdecc`  
		Last Modified: Thu, 26 Dec 2019 23:05:03 GMT  
		Size: 16.2 MB (16158246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8028c0b7a7e712cf77e535c0d109ae5bce6ae34cefcd8ebf46b640214b5c91`  
		Last Modified: Thu, 26 Dec 2019 23:04:59 GMT  
		Size: 2.2 KB (2217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cc7bad024a2e7896c445c24345d1b9226c1c7ed0adbc57145db4d8ce9aea2f`  
		Last Modified: Thu, 26 Dec 2019 23:04:59 GMT  
		Size: 73.2 KB (73165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc711a535acb29705350d1595ce40c1748951322b88a6413245a4d2a5b7f645`  
		Last Modified: Fri, 27 Dec 2019 03:49:14 GMT  
		Size: 34.8 MB (34774961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5788687df725e868549f29349dd7e546295b632f970634f2b97660aa15c10c9`  
		Last Modified: Fri, 27 Dec 2019 03:49:06 GMT  
		Size: 277.5 KB (277531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91a01e20dbd8ec111d179be5a7d9f856c2018938a07f94ce1de5f111907de97`  
		Last Modified: Fri, 27 Dec 2019 03:49:06 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c853bffcbc704b657c099fa2a3cc9c10919552af9a3e0a2d8ae4a42e6782eb`  
		Last Modified: Fri, 27 Dec 2019 03:49:06 GMT  
		Size: 497.0 KB (497005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0d79794dfc6b4b090401c350caf4bfcb0c038672d8c0a28d3d822838f9dcd2`  
		Last Modified: Fri, 27 Dec 2019 03:49:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fac451fab2e34ab918bfe33533c77b938fe2bcb55ff4680a6468d524e1c69a6`  
		Last Modified: Fri, 27 Dec 2019 03:49:06 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1` - linux; arm variant v6

```console
$ docker pull composer@sha256:dd97b87c2947f5c3a5a55e9e6153cf324920f5747918d25b6ec90cebdc44087e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64113537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fcb94b450243c8357d8679a6da332460fbcf60f735dc84e44f27f87554e02c6`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:20:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:20:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:20:18 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:20:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:20:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:20:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:20:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:20:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:20:24 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:20:25 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:20:26 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:20:27 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:20:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:20:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:24:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:24:26 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:24:30 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:24:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:24:35 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 01:32:05 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 01:32:22 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 01:32:24 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 01:32:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 01:32:26 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 01:32:26 GMT
ENV COMPOSER_VERSION=1.9.1
# Fri, 27 Dec 2019 01:32:29 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 01:32:29 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 01:32:33 GMT
WORKDIR /app
# Fri, 27 Dec 2019 01:32:36 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 01:32:39 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f2222aeb0ea56ad08de7753e2ed3f6c40f7093cda7436e94583ce0f0922072`  
		Last Modified: Thu, 26 Dec 2019 23:02:36 GMT  
		Size: 1.3 MB (1321130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f893e696ec7590309f1a77539ce734af052f1aa42c48aaf6f478453dcd7eafa`  
		Last Modified: Thu, 26 Dec 2019 23:02:35 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ad230ebfba33233fbafdd19ca2939dfd20dffdc83636c23f9285017935fca9`  
		Last Modified: Thu, 26 Dec 2019 23:02:35 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44905e88daf12c640968d3d790a02e11babe5d4f4730e6fcd3eae081f8df2f62`  
		Last Modified: Thu, 26 Dec 2019 23:02:34 GMT  
		Size: 10.3 MB (10264410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e91ff6ebef94b35989b1200b9d2564b71aa5e20f03fbc2c75bf57786cdca79`  
		Last Modified: Thu, 26 Dec 2019 23:02:34 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6b1bfceee6e3798ac6b36213aede482172b522e4c9d17635d9418419bd0672`  
		Last Modified: Thu, 26 Dec 2019 23:02:39 GMT  
		Size: 15.0 MB (14962846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6b063069fde53011cbbab0f1fc6cb9f8b02fb20f6f0e986394d971347f38c0`  
		Last Modified: Thu, 26 Dec 2019 23:02:34 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f29f685cf530bfbe1b0003111bed088314ef583a2585bb11a10d7463dfc5dd8`  
		Last Modified: Thu, 26 Dec 2019 23:02:34 GMT  
		Size: 72.7 KB (72680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa550c82c0fdd2e85ec9b9b51732a4590f1a279d6856aa6bd427e28a5571260`  
		Last Modified: Fri, 27 Dec 2019 01:33:31 GMT  
		Size: 34.1 MB (34107571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9770e9484fb6fd2b55324ba5ef682f2a2b1f08bb3dbcf502ca8ecf32cf0c8f`  
		Last Modified: Fri, 27 Dec 2019 01:33:16 GMT  
		Size: 270.7 KB (270675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1f90781495ee403d3826a9f593fde90d3657e5f87f2bc0d757d74c7b4435ab`  
		Last Modified: Fri, 27 Dec 2019 01:33:16 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5ee0bd8ba874c58e5a766515b76e4d85166155f92d996c24c3a26f0ebc5138`  
		Last Modified: Fri, 27 Dec 2019 01:33:16 GMT  
		Size: 497.0 KB (497035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c38f9121f497e45f2517272c56a59f4a5992b6274fb6d9685b1100f69512c2`  
		Last Modified: Fri, 27 Dec 2019 01:33:16 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36b2e72ff9d80d06d651f66bd8bd8f258ccf15e4c6c144bd710e16fae8aea73`  
		Last Modified: Fri, 27 Dec 2019 01:33:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1` - linux; arm variant v7

```console
$ docker pull composer@sha256:f677de2a63ff1ae9145160a6605ea45bc413e58b4bdf8d4cb91263130c945bcf
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61388895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9012e1c5224f7b7e3ec0077971ad126503067b41b3e53da4df6c6012c3aa112`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 18:59:09 GMT
ADD file:caf7ca25875eddd2bfa2d1e56663bb52d278a85f6ee1314f9ccf01dc4da8070a in / 
# Tue, 24 Dec 2019 18:59:10 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:28:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 21:28:59 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 21:29:01 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 21:29:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 21:29:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 21:29:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:29:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:29:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 21:29:05 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 21:29:05 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 21:29:06 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 21:29:06 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 21:29:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 21:29:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:31:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 21:31:34 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:31:36 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 21:31:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 21:31:38 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 00:05:43 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 00:06:02 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 00:06:04 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 00:06:04 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 00:06:05 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 00:06:06 GMT
ENV COMPOSER_VERSION=1.9.1
# Fri, 27 Dec 2019 00:06:09 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 00:06:10 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 00:06:11 GMT
WORKDIR /app
# Fri, 27 Dec 2019 00:06:13 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 00:06:15 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:3922e475e500b2739b5e74787fc80622853325822f71f8bd3de7e5b09654d60f`  
		Last Modified: Tue, 24 Dec 2019 18:59:33 GMT  
		Size: 2.4 MB (2416691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d850653ef66a74bc2f65e933df679895db53bc6e01d23076dbc532056eec8a7`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 1.2 MB (1227347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed0b2f0bcd9c23ef1f79be9d752fea5f714457c75308002cf597d596e8b1c1a`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77de73a7de2b81d6828d80578fc934edf55e039effcf2bb8555e6a0b5864080`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69dc1b35828f88798cdf411520e8541662fa44c3e21d0b46b668e5ad1ce38f24`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 10.3 MB (10264419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1ac53e078b99a6ba0cf4e8600a0ba5aa6bd3b579e0f86d78a3b18bd692976a`  
		Last Modified: Thu, 26 Dec 2019 22:01:16 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a349634f832daa7e54f052c5c5fce54336c7089c5997981c3be8552baf32c10c`  
		Last Modified: Thu, 26 Dec 2019 22:01:21 GMT  
		Size: 14.0 MB (14035302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef07c3ed8c6baead6c71677fb97b0bef1c3762881b234e8ed7aa21c0470854ed`  
		Last Modified: Thu, 26 Dec 2019 22:01:16 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01eab0467fa0094e7e35ef8de9b09468e7ae8b53efc431442a1a9af5a5be310a`  
		Last Modified: Thu, 26 Dec 2019 22:01:16 GMT  
		Size: 72.7 KB (72675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef760acfe9c6c709e6adc3e53bb918efdfbf825221903209bd82018b119c1439`  
		Last Modified: Fri, 27 Dec 2019 00:06:57 GMT  
		Size: 32.6 MB (32605578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51aade9d91ae2843e8ec23f54eea99048fa2d73d2e01cea93889e60c54b4210`  
		Last Modified: Fri, 27 Dec 2019 00:06:44 GMT  
		Size: 264.7 KB (264673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a512d9b12df16845d0df25d19e6307acb404fcf2f3a3862d47f94e2259fb0f23`  
		Last Modified: Fri, 27 Dec 2019 00:06:44 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cde7a20d9972695c743aa2a0e922361370380dbef712fea1617d181bbe4fc`  
		Last Modified: Fri, 27 Dec 2019 00:06:44 GMT  
		Size: 497.0 KB (497037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852bb277a6ed901b13ff9be031f1aa4b6a5e313dfb998b3c6c5f10055a93e3a2`  
		Last Modified: Fri, 27 Dec 2019 00:06:44 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce34df92ca04dd2bdf3e2373fc25a8a172c772c16ad3b38cfa6f9e63eddb7e46`  
		Last Modified: Fri, 27 Dec 2019 00:06:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:baf042a8b58480a86b9a613750042c985cd23d66830d12ef6dbd874cd5ff2b77
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66202831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a184fefdede0cf61596a9690935c94a10a964cdbca862d66a76da536cdbbb4c4`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 20:26:15 GMT
ADD file:d6c3db0313ab0c6201770c7248d1bac964011a1c08f1a9b434442b7c21efef87 in / 
# Tue, 24 Dec 2019 20:26:24 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:08:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:08:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:08:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:08:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:08:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:08:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:08:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:08:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:08:38 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:08:39 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:08:40 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:08:40 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:08:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:08:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:12:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:12:26 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:12:30 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:12:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:12:32 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 01:00:35 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 01:01:10 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 01:01:21 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 01:01:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 01:01:34 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 01:01:38 GMT
ENV COMPOSER_VERSION=1.9.1
# Fri, 27 Dec 2019 01:01:54 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 01:01:56 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 01:02:01 GMT
WORKDIR /app
# Fri, 27 Dec 2019 01:02:03 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 01:02:05 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cde5963f3b93eec667cad527c99d80402a5a91a7a1381f7ffe562f215aec0c50`  
		Last Modified: Tue, 24 Dec 2019 20:26:52 GMT  
		Size: 2.7 MB (2719182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36763f956175b40d2a6ca97c274d362c9a0deb76d9b7eb62e95b8ca953bb1db2`  
		Last Modified: Thu, 26 Dec 2019 22:48:41 GMT  
		Size: 1.4 MB (1359427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01374ab459ad592d2c9b91efb836df933906c6cd8c63606db7f385c084fa04d2`  
		Last Modified: Thu, 26 Dec 2019 22:48:40 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34492236b9882b05dc402fe511c10ac8463554a1223a9bd10460daeab25a98f`  
		Last Modified: Thu, 26 Dec 2019 22:48:40 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b0ab5705e600f30f4341814fc44949ef8a0595246e35d6a72d4146fd467f1e`  
		Last Modified: Thu, 26 Dec 2019 22:48:38 GMT  
		Size: 10.3 MB (10264412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8fe4aab7c71980ba6c9c10d2d41202a098e48ef491850ebc67b17a147487d88`  
		Last Modified: Thu, 26 Dec 2019 22:48:38 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f253d45c879751ce17f7944d232be8fcb0e2bc700a5a6714d97a63867aff06`  
		Last Modified: Thu, 26 Dec 2019 22:48:41 GMT  
		Size: 15.9 MB (15851650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805b37c27a0499cf4df7c736ea7581d72e1cb4a6613bda953833b79a80caac1a`  
		Last Modified: Thu, 26 Dec 2019 22:48:38 GMT  
		Size: 2.2 KB (2215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7400940d887ae822a41abe503ec76c4a6e979621ecf316d123cb0d39eb34db`  
		Last Modified: Thu, 26 Dec 2019 22:48:38 GMT  
		Size: 72.7 KB (72682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1a36a335b2a481db4a07619c7e30bdced72bc39e6b6f1ee3715a6cdc603bd1`  
		Last Modified: Fri, 27 Dec 2019 01:03:09 GMT  
		Size: 35.2 MB (35157603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ea079782c565a70581045175e15f46bb937e07e2200ea63b03bf72af221b07`  
		Last Modified: Fri, 27 Dec 2019 01:02:55 GMT  
		Size: 275.7 KB (275669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae534ca14dbc48106ee3f2e81f33b327cf7eb302898c02bb4ab7345cc44b502`  
		Last Modified: Fri, 27 Dec 2019 01:02:55 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9f707e568acdc4ac64f6df65d1da26a796d239543900581845647ae7cc94df`  
		Last Modified: Fri, 27 Dec 2019 01:02:55 GMT  
		Size: 497.0 KB (497033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38530d4206c9f562e53cadc427a46c8e2adf48db5da189fae8d33fa45f587f3`  
		Last Modified: Fri, 27 Dec 2019 01:02:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d6873676bd3565875ec532df054c50b52dc9d79b2ec8f6e43f5ce27e78b2b1`  
		Last Modified: Fri, 27 Dec 2019 01:02:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1` - linux; 386

```console
$ docker pull composer@sha256:eb104347bdbea942b571973f68326dce69ae3c92dfe7aa331d88298dc4d5c493
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68289013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb946c124f051f09f714c35fd6e2529d6707c10ec140737cf56e882111bcd82`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 19:38:57 GMT
ADD file:d0127a9692e8445993a88163cb741dbb23fa25436dd65289e76b08484264b397 in / 
# Tue, 24 Dec 2019 19:38:57 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:36:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:36:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:36:14 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:36:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:36:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:36:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:36:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:36:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:36:17 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:36:18 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:36:18 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:36:18 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:36:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:36:23 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:45:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:45:50 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:45:51 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:45:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:45:52 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 01:41:40 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 01:41:52 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 01:41:52 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 01:41:52 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 01:41:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 01:41:53 GMT
ENV COMPOSER_VERSION=1.9.1
# Fri, 27 Dec 2019 01:41:54 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 01:41:54 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 01:41:54 GMT
WORKDIR /app
# Fri, 27 Dec 2019 01:41:55 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 01:41:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:57bbc6f150623b3e4f01930af4ab2efa6ed5df02319341a08b1ce0bbd7e4afdf`  
		Last Modified: Tue, 24 Dec 2019 19:39:19 GMT  
		Size: 2.8 MB (2805146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db25e971d6f24055202f90f96d257a719817ad73623eaf02d98fb13c2dbe9a1b`  
		Last Modified: Fri, 27 Dec 2019 00:00:12 GMT  
		Size: 1.5 MB (1452611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ecdadbdbb91bc66f820e5b3077004286155b3e618cc444f493d7e73b400333`  
		Last Modified: Fri, 27 Dec 2019 00:00:12 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8331211b40f9489961b63904af5f93f96465efa4f5202ee08600fd1fe3caec6c`  
		Last Modified: Fri, 27 Dec 2019 00:00:11 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1feab22a6dc5f30ac5d6a419e21b0ad02df0633e9376cda5af697a214a1677e`  
		Last Modified: Fri, 27 Dec 2019 00:00:12 GMT  
		Size: 10.3 MB (10264412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f291e0ec174ac10d076b738bdd8d7b5a352fd362d9659a6cb4b7c5cf7e219323`  
		Last Modified: Fri, 27 Dec 2019 00:00:10 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeee04bc33533cf870952c9aab9489299215c7b4a6077fc85ded1a38354bfa34`  
		Last Modified: Fri, 27 Dec 2019 00:00:17 GMT  
		Size: 16.6 MB (16572401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4baee82eaeb4bb25b75b28052d7aec12a58e5f0b9cc3abdccdea6d742bda1e`  
		Last Modified: Fri, 27 Dec 2019 00:00:10 GMT  
		Size: 2.2 KB (2215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01721c87d29cd0ad25164e2a64d81439e2201e730353ea8a64a5324af5aaaa6`  
		Last Modified: Fri, 27 Dec 2019 00:00:10 GMT  
		Size: 72.3 KB (72336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3650f92aaf29753dc8d77c5521fe278f1fc1be26d84d5a01b2931c17fba38029`  
		Last Modified: Fri, 27 Dec 2019 01:42:21 GMT  
		Size: 36.3 MB (36327612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cabc1b7971f28befd3ee5c2117694eaaf4e7750fab49a6718b9de78c706ae4b`  
		Last Modified: Fri, 27 Dec 2019 01:42:11 GMT  
		Size: 292.4 KB (292421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a90dea8b1328167473598879d3d8ae5cd35c5b9d38f71e564048508f36f480`  
		Last Modified: Fri, 27 Dec 2019 01:42:11 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f18de3cac22e1e5f06fcdcdc7c32966859717887c9de60785ce0af29c1fd4ca`  
		Last Modified: Fri, 27 Dec 2019 01:42:11 GMT  
		Size: 497.0 KB (497009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392481b4d02274d120941ac388bec69fbb9ac1c1dc3e951b48156c2b1bb5def6`  
		Last Modified: Fri, 27 Dec 2019 01:42:11 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f279761684374c3e2dfc98ed41d387bae19d174837ef1e03e16e2c72696f126b`  
		Last Modified: Fri, 27 Dec 2019 01:42:11 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1` - linux; ppc64le

```console
$ docker pull composer@sha256:d4d9899d9faa184331bc4a29f410d7ad97c617303ddecc1cb7512d79490ec254
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68398531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058a3b17db3adc1e4a850d3509a225280c8618a5496c9cacddb5c48ef1b37da4`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 19:28:37 GMT
ADD file:4d85451a651e236d899cd849617594eb6babf24079f9b2269134ad06d89bdecc in / 
# Tue, 24 Dec 2019 19:28:38 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:21:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:21:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:21:14 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:21:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:21:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:21:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:21:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:21:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:21:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:21:31 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:21:32 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:21:34 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:21:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:21:52 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:26:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:26:57 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:27:14 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:27:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:27:22 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 01:23:47 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 01:24:07 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 01:24:11 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 01:24:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 01:24:15 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 01:24:17 GMT
ENV COMPOSER_VERSION=1.9.1
# Fri, 27 Dec 2019 01:24:22 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 01:24:24 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 01:24:25 GMT
WORKDIR /app
# Fri, 27 Dec 2019 01:24:27 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 01:24:29 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a5dee701e1e87430161d8fce67e77ee5e132bdbafe165c52490a36df654c7660`  
		Last Modified: Tue, 24 Dec 2019 19:29:09 GMT  
		Size: 2.8 MB (2816482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5787caafdab36524ef14f193793a44b3b5f54da82c98e8152770c2868fd93b11`  
		Last Modified: Thu, 26 Dec 2019 23:13:04 GMT  
		Size: 1.4 MB (1397977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691639ddfd73c88dfeda1734ababccfaed311f9d747bf07d41c6e7fed2880baf`  
		Last Modified: Thu, 26 Dec 2019 23:13:03 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2a706347c576336f1e0145755e4fa707710b3f42dc7d18903fcee51bb72842`  
		Last Modified: Thu, 26 Dec 2019 23:13:02 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c9367473ae473e3b4307b84581a68ce338708fd02c58387ea03ebbf3b336c4`  
		Last Modified: Thu, 26 Dec 2019 23:13:00 GMT  
		Size: 10.3 MB (10264430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce400ab5b594b3c37b04d8ff93ef76324ad103b89b864086646553aa374ae3a`  
		Last Modified: Thu, 26 Dec 2019 23:12:59 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df72cd13deac5a2de7a62833b97945cc48eb13a954c074f0c2ef27d321ad172`  
		Last Modified: Thu, 26 Dec 2019 23:13:09 GMT  
		Size: 17.1 MB (17073151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a993ff611f4ce5c9ad8c688b7d218dfaf24788380583d0b8ff19758b953565b`  
		Last Modified: Thu, 26 Dec 2019 23:12:59 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b2a23101f41428ee2ad1948c90b3eaf9cda596853a790ebdb59a2e5f3a4353`  
		Last Modified: Thu, 26 Dec 2019 23:12:59 GMT  
		Size: 73.0 KB (73011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c481dd45fa62f76d142285ca14edc35411b4ea549c65fa328636265afec673`  
		Last Modified: Fri, 27 Dec 2019 01:25:27 GMT  
		Size: 36.0 MB (35979323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5e3a68f6ae205b4e6572bf9337334694abcf7dfe1e953aeda6fe3d3953efaf`  
		Last Modified: Fri, 27 Dec 2019 01:25:16 GMT  
		Size: 291.9 KB (291945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cceb98b5eab7c70364129cb95652d435f2c30fa63e2235def0ca4fbd5c83fb8`  
		Last Modified: Fri, 27 Dec 2019 01:25:16 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3875e4f7132972e39b1f6f2567e1e72a74c20e0ac8200088fd0fc852dc0620a5`  
		Last Modified: Fri, 27 Dec 2019 01:25:16 GMT  
		Size: 497.0 KB (497039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9424e5c97107933298a9e864dab7c85c93b9baae4be24ad2cf5c1d4348829f`  
		Last Modified: Fri, 27 Dec 2019 01:25:16 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ed0b7e2bf3399fa8adf53702486277f2b7e4df20472dfe2d75cc0b4c3523f2`  
		Last Modified: Fri, 27 Dec 2019 01:25:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `composer:1.8`

```console
$ docker pull composer@sha256:bfdac7f094277961b6d00386129d8a54ff5173f88caef2b2f22e06055872df4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `composer:1.8` - linux; amd64

```console
$ docker pull composer@sha256:45e8d6643df9c498a057dc5df4b7e9e320870f6dce0e0f1ef36cd28260d121ee
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66201172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e4272d8577f725edc3045421292df51d8cb6805823ce1798bbc9c99e9344ce`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:47:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 21:47:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 21:47:52 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 21:47:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 21:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 21:47:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:47:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:47:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 21:47:55 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 21:47:55 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 21:47:55 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 21:47:55 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 21:47:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 21:47:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:55:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 21:55:56 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:55:58 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 21:55:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 21:55:58 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 03:48:37 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 03:48:47 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 03:48:47 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 03:48:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 03:48:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 03:48:54 GMT
ENV COMPOSER_VERSION=1.8.6
# Fri, 27 Dec 2019 03:48:55 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 03:48:55 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 03:48:55 GMT
WORKDIR /app
# Fri, 27 Dec 2019 03:48:56 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 03:48:56 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7a574e8632727fe466d1871c39e4fea951243dc9f0a56bdc55cb8720f4aac6`  
		Last Modified: Thu, 26 Dec 2019 23:05:01 GMT  
		Size: 1.4 MB (1354713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6c65f587e94ae6bd946a70d456e75c7543d38cb03271622a815f3b5398ec74`  
		Last Modified: Thu, 26 Dec 2019 23:05:00 GMT  
		Size: 1.2 KB (1227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba33e4b639bb4e1187590b34ea007a27393fbda41d6f3ad10d04c9a0bd1cde4a`  
		Last Modified: Thu, 26 Dec 2019 23:05:00 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94182f10949f8b172016cbddea1d7b4417514c40d0fd664a0895d3b0f93fcbe`  
		Last Modified: Thu, 26 Dec 2019 23:05:00 GMT  
		Size: 10.3 MB (10264403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06b2b4baeabcdc2692442b4f6a6512b1f6b20697c8ec9b984503705cc81039a`  
		Last Modified: Thu, 26 Dec 2019 23:04:59 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6abb9ac3b49074e4561b65dbf3c4beaab0b50ef72743a04656dd6e664bcdecc`  
		Last Modified: Thu, 26 Dec 2019 23:05:03 GMT  
		Size: 16.2 MB (16158246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8028c0b7a7e712cf77e535c0d109ae5bce6ae34cefcd8ebf46b640214b5c91`  
		Last Modified: Thu, 26 Dec 2019 23:04:59 GMT  
		Size: 2.2 KB (2217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cc7bad024a2e7896c445c24345d1b9226c1c7ed0adbc57145db4d8ce9aea2f`  
		Last Modified: Thu, 26 Dec 2019 23:04:59 GMT  
		Size: 73.2 KB (73165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc711a535acb29705350d1595ce40c1748951322b88a6413245a4d2a5b7f645`  
		Last Modified: Fri, 27 Dec 2019 03:49:14 GMT  
		Size: 34.8 MB (34774961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5788687df725e868549f29349dd7e546295b632f970634f2b97660aa15c10c9`  
		Last Modified: Fri, 27 Dec 2019 03:49:06 GMT  
		Size: 277.5 KB (277531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91a01e20dbd8ec111d179be5a7d9f856c2018938a07f94ce1de5f111907de97`  
		Last Modified: Fri, 27 Dec 2019 03:49:06 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90bdda6211d42845b95041bd3d4316f0c8b72436a3c51ee3389e11b163e9e3`  
		Last Modified: Fri, 27 Dec 2019 03:49:19 GMT  
		Size: 491.3 KB (491316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928b13c387920b76bc6e604910557c2215932762eca439777a64b8de83380cbc`  
		Last Modified: Fri, 27 Dec 2019 03:49:19 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d48b97065c31a6d92057bcda5eacabc4dfa96bc8881943fe66159e68e52de5`  
		Last Modified: Fri, 27 Dec 2019 03:49:19 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.8` - linux; arm variant v6

```console
$ docker pull composer@sha256:2d136210a534efda6603f0c80e6c16e1118cfce1a3056f45dc032301f182bc4d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64107864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842b3b89588e6ef46c0f56117dc5d590a8a17d84736bb93e45b73086208bc81d`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:20:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:20:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:20:18 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:20:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:20:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:20:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:20:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:20:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:20:24 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:20:25 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:20:26 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:20:27 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:20:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:20:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:24:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:24:26 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:24:30 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:24:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:24:35 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 01:32:05 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 01:32:22 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 01:32:24 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 01:32:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 01:32:26 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 01:32:51 GMT
ENV COMPOSER_VERSION=1.8.6
# Fri, 27 Dec 2019 01:32:55 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 01:32:55 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 01:32:57 GMT
WORKDIR /app
# Fri, 27 Dec 2019 01:32:58 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 01:33:01 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f2222aeb0ea56ad08de7753e2ed3f6c40f7093cda7436e94583ce0f0922072`  
		Last Modified: Thu, 26 Dec 2019 23:02:36 GMT  
		Size: 1.3 MB (1321130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f893e696ec7590309f1a77539ce734af052f1aa42c48aaf6f478453dcd7eafa`  
		Last Modified: Thu, 26 Dec 2019 23:02:35 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ad230ebfba33233fbafdd19ca2939dfd20dffdc83636c23f9285017935fca9`  
		Last Modified: Thu, 26 Dec 2019 23:02:35 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44905e88daf12c640968d3d790a02e11babe5d4f4730e6fcd3eae081f8df2f62`  
		Last Modified: Thu, 26 Dec 2019 23:02:34 GMT  
		Size: 10.3 MB (10264410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e91ff6ebef94b35989b1200b9d2564b71aa5e20f03fbc2c75bf57786cdca79`  
		Last Modified: Thu, 26 Dec 2019 23:02:34 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6b1bfceee6e3798ac6b36213aede482172b522e4c9d17635d9418419bd0672`  
		Last Modified: Thu, 26 Dec 2019 23:02:39 GMT  
		Size: 15.0 MB (14962846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6b063069fde53011cbbab0f1fc6cb9f8b02fb20f6f0e986394d971347f38c0`  
		Last Modified: Thu, 26 Dec 2019 23:02:34 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f29f685cf530bfbe1b0003111bed088314ef583a2585bb11a10d7463dfc5dd8`  
		Last Modified: Thu, 26 Dec 2019 23:02:34 GMT  
		Size: 72.7 KB (72680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa550c82c0fdd2e85ec9b9b51732a4590f1a279d6856aa6bd427e28a5571260`  
		Last Modified: Fri, 27 Dec 2019 01:33:31 GMT  
		Size: 34.1 MB (34107571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9770e9484fb6fd2b55324ba5ef682f2a2b1f08bb3dbcf502ca8ecf32cf0c8f`  
		Last Modified: Fri, 27 Dec 2019 01:33:16 GMT  
		Size: 270.7 KB (270675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1f90781495ee403d3826a9f593fde90d3657e5f87f2bc0d757d74c7b4435ab`  
		Last Modified: Fri, 27 Dec 2019 01:33:16 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5278924a8ef7ad9d80d4ce31a0c33b12e80242f38aceba375f418fd3f28c7d82`  
		Last Modified: Fri, 27 Dec 2019 01:33:41 GMT  
		Size: 491.4 KB (491363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3675101bcd4a1795bfa3c0e8b263fc5e19abc3d247975d137070868ee3f2bff0`  
		Last Modified: Fri, 27 Dec 2019 01:33:41 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb89ac22ffc978d304fb106ed408f9d09459254e5f0f0390a7c1ec5c6b94cca`  
		Last Modified: Fri, 27 Dec 2019 01:33:41 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.8` - linux; arm variant v7

```console
$ docker pull composer@sha256:c9687df66e63087f4cc85c41b4d4865d4c0f2c2b5c4917887059b37b81031f12
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61383216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bcdd5c1732e13ea3103fd5548a5be8b33f85b9a153d54860a01699679e0786`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 18:59:09 GMT
ADD file:caf7ca25875eddd2bfa2d1e56663bb52d278a85f6ee1314f9ccf01dc4da8070a in / 
# Tue, 24 Dec 2019 18:59:10 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:28:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 21:28:59 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 21:29:01 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 21:29:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 21:29:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 21:29:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:29:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:29:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 21:29:05 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 21:29:05 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 21:29:06 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 21:29:06 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 21:29:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 21:29:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:31:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 21:31:34 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:31:36 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 21:31:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 21:31:38 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 00:05:43 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 00:06:02 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 00:06:04 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 00:06:04 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 00:06:05 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 00:06:22 GMT
ENV COMPOSER_VERSION=1.8.6
# Fri, 27 Dec 2019 00:06:26 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 00:06:27 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 00:06:28 GMT
WORKDIR /app
# Fri, 27 Dec 2019 00:06:29 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 00:06:30 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:3922e475e500b2739b5e74787fc80622853325822f71f8bd3de7e5b09654d60f`  
		Last Modified: Tue, 24 Dec 2019 18:59:33 GMT  
		Size: 2.4 MB (2416691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d850653ef66a74bc2f65e933df679895db53bc6e01d23076dbc532056eec8a7`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 1.2 MB (1227347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed0b2f0bcd9c23ef1f79be9d752fea5f714457c75308002cf597d596e8b1c1a`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77de73a7de2b81d6828d80578fc934edf55e039effcf2bb8555e6a0b5864080`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69dc1b35828f88798cdf411520e8541662fa44c3e21d0b46b668e5ad1ce38f24`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 10.3 MB (10264419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1ac53e078b99a6ba0cf4e8600a0ba5aa6bd3b579e0f86d78a3b18bd692976a`  
		Last Modified: Thu, 26 Dec 2019 22:01:16 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a349634f832daa7e54f052c5c5fce54336c7089c5997981c3be8552baf32c10c`  
		Last Modified: Thu, 26 Dec 2019 22:01:21 GMT  
		Size: 14.0 MB (14035302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef07c3ed8c6baead6c71677fb97b0bef1c3762881b234e8ed7aa21c0470854ed`  
		Last Modified: Thu, 26 Dec 2019 22:01:16 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01eab0467fa0094e7e35ef8de9b09468e7ae8b53efc431442a1a9af5a5be310a`  
		Last Modified: Thu, 26 Dec 2019 22:01:16 GMT  
		Size: 72.7 KB (72675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef760acfe9c6c709e6adc3e53bb918efdfbf825221903209bd82018b119c1439`  
		Last Modified: Fri, 27 Dec 2019 00:06:57 GMT  
		Size: 32.6 MB (32605578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51aade9d91ae2843e8ec23f54eea99048fa2d73d2e01cea93889e60c54b4210`  
		Last Modified: Fri, 27 Dec 2019 00:06:44 GMT  
		Size: 264.7 KB (264673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a512d9b12df16845d0df25d19e6307acb404fcf2f3a3862d47f94e2259fb0f23`  
		Last Modified: Fri, 27 Dec 2019 00:06:44 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335b7d5f97bb02adc9d932734c7f524469ed1473ab531bc2afc2b4683e83492c`  
		Last Modified: Fri, 27 Dec 2019 00:07:10 GMT  
		Size: 491.4 KB (491358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b6bb39a91170eba2cd3765ba8c3559febd50d14e873f9785ebc9e6a99384bb`  
		Last Modified: Fri, 27 Dec 2019 00:07:10 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ce943e9a4fad64294bc3cea3c48fcdf06306a5496fa1876b8a9465612528b1`  
		Last Modified: Fri, 27 Dec 2019 00:07:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.8` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:41e45473f243c71fb05e0706b94bfa6197f7acd78cc1c083c9dfd598c37f3491
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66197161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27ec7cac3f147803cb4fa9d6b13557570cfa9671344a79accf48438f37cd3cd`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 20:26:15 GMT
ADD file:d6c3db0313ab0c6201770c7248d1bac964011a1c08f1a9b434442b7c21efef87 in / 
# Tue, 24 Dec 2019 20:26:24 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:08:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:08:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:08:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:08:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:08:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:08:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:08:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:08:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:08:38 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:08:39 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:08:40 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:08:40 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:08:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:08:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:12:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:12:26 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:12:30 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:12:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:12:32 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 01:00:35 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 01:01:10 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 01:01:21 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 01:01:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 01:01:34 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 01:02:18 GMT
ENV COMPOSER_VERSION=1.8.6
# Fri, 27 Dec 2019 01:02:22 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 01:02:25 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 01:02:29 GMT
WORKDIR /app
# Fri, 27 Dec 2019 01:02:35 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 01:02:37 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cde5963f3b93eec667cad527c99d80402a5a91a7a1381f7ffe562f215aec0c50`  
		Last Modified: Tue, 24 Dec 2019 20:26:52 GMT  
		Size: 2.7 MB (2719182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36763f956175b40d2a6ca97c274d362c9a0deb76d9b7eb62e95b8ca953bb1db2`  
		Last Modified: Thu, 26 Dec 2019 22:48:41 GMT  
		Size: 1.4 MB (1359427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01374ab459ad592d2c9b91efb836df933906c6cd8c63606db7f385c084fa04d2`  
		Last Modified: Thu, 26 Dec 2019 22:48:40 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34492236b9882b05dc402fe511c10ac8463554a1223a9bd10460daeab25a98f`  
		Last Modified: Thu, 26 Dec 2019 22:48:40 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b0ab5705e600f30f4341814fc44949ef8a0595246e35d6a72d4146fd467f1e`  
		Last Modified: Thu, 26 Dec 2019 22:48:38 GMT  
		Size: 10.3 MB (10264412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8fe4aab7c71980ba6c9c10d2d41202a098e48ef491850ebc67b17a147487d88`  
		Last Modified: Thu, 26 Dec 2019 22:48:38 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f253d45c879751ce17f7944d232be8fcb0e2bc700a5a6714d97a63867aff06`  
		Last Modified: Thu, 26 Dec 2019 22:48:41 GMT  
		Size: 15.9 MB (15851650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805b37c27a0499cf4df7c736ea7581d72e1cb4a6613bda953833b79a80caac1a`  
		Last Modified: Thu, 26 Dec 2019 22:48:38 GMT  
		Size: 2.2 KB (2215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7400940d887ae822a41abe503ec76c4a6e979621ecf316d123cb0d39eb34db`  
		Last Modified: Thu, 26 Dec 2019 22:48:38 GMT  
		Size: 72.7 KB (72682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1a36a335b2a481db4a07619c7e30bdced72bc39e6b6f1ee3715a6cdc603bd1`  
		Last Modified: Fri, 27 Dec 2019 01:03:09 GMT  
		Size: 35.2 MB (35157603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ea079782c565a70581045175e15f46bb937e07e2200ea63b03bf72af221b07`  
		Last Modified: Fri, 27 Dec 2019 01:02:55 GMT  
		Size: 275.7 KB (275669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae534ca14dbc48106ee3f2e81f33b327cf7eb302898c02bb4ab7345cc44b502`  
		Last Modified: Fri, 27 Dec 2019 01:02:55 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328144f18dce602a0069dcbfc04682831ff7c9678904c3fc21b481687a4e90c6`  
		Last Modified: Fri, 27 Dec 2019 01:03:21 GMT  
		Size: 491.4 KB (491363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fb8496f7109fe4f5452fac7aee6af6181d4bdc53a020cadeb776afc7254f4f`  
		Last Modified: Fri, 27 Dec 2019 01:03:22 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589529a410238155419258a930085987eec075a542c59da879e016ae7fcc08bb`  
		Last Modified: Fri, 27 Dec 2019 01:03:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.8` - linux; 386

```console
$ docker pull composer@sha256:08f5e4ba228346b7bb0b33ec31b3548cf530ed4e32abfb1bb6633a5f8f2defe2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68283329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be130ddb518628e342f922b553c37b33678eb475ea433d4a3fdf07845e8b06d4`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 19:38:57 GMT
ADD file:d0127a9692e8445993a88163cb741dbb23fa25436dd65289e76b08484264b397 in / 
# Tue, 24 Dec 2019 19:38:57 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:36:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:36:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:36:14 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:36:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:36:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:36:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:36:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:36:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:36:17 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:36:18 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:36:18 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:36:18 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:36:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:36:23 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:45:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:45:50 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:45:51 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:45:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:45:52 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 01:41:40 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 01:41:52 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 01:41:52 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 01:41:52 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 01:41:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 01:42:02 GMT
ENV COMPOSER_VERSION=1.8.6
# Fri, 27 Dec 2019 01:42:03 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 01:42:03 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 01:42:03 GMT
WORKDIR /app
# Fri, 27 Dec 2019 01:42:04 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 01:42:04 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:57bbc6f150623b3e4f01930af4ab2efa6ed5df02319341a08b1ce0bbd7e4afdf`  
		Last Modified: Tue, 24 Dec 2019 19:39:19 GMT  
		Size: 2.8 MB (2805146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db25e971d6f24055202f90f96d257a719817ad73623eaf02d98fb13c2dbe9a1b`  
		Last Modified: Fri, 27 Dec 2019 00:00:12 GMT  
		Size: 1.5 MB (1452611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ecdadbdbb91bc66f820e5b3077004286155b3e618cc444f493d7e73b400333`  
		Last Modified: Fri, 27 Dec 2019 00:00:12 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8331211b40f9489961b63904af5f93f96465efa4f5202ee08600fd1fe3caec6c`  
		Last Modified: Fri, 27 Dec 2019 00:00:11 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1feab22a6dc5f30ac5d6a419e21b0ad02df0633e9376cda5af697a214a1677e`  
		Last Modified: Fri, 27 Dec 2019 00:00:12 GMT  
		Size: 10.3 MB (10264412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f291e0ec174ac10d076b738bdd8d7b5a352fd362d9659a6cb4b7c5cf7e219323`  
		Last Modified: Fri, 27 Dec 2019 00:00:10 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeee04bc33533cf870952c9aab9489299215c7b4a6077fc85ded1a38354bfa34`  
		Last Modified: Fri, 27 Dec 2019 00:00:17 GMT  
		Size: 16.6 MB (16572401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4baee82eaeb4bb25b75b28052d7aec12a58e5f0b9cc3abdccdea6d742bda1e`  
		Last Modified: Fri, 27 Dec 2019 00:00:10 GMT  
		Size: 2.2 KB (2215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01721c87d29cd0ad25164e2a64d81439e2201e730353ea8a64a5324af5aaaa6`  
		Last Modified: Fri, 27 Dec 2019 00:00:10 GMT  
		Size: 72.3 KB (72336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3650f92aaf29753dc8d77c5521fe278f1fc1be26d84d5a01b2931c17fba38029`  
		Last Modified: Fri, 27 Dec 2019 01:42:21 GMT  
		Size: 36.3 MB (36327612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cabc1b7971f28befd3ee5c2117694eaaf4e7750fab49a6718b9de78c706ae4b`  
		Last Modified: Fri, 27 Dec 2019 01:42:11 GMT  
		Size: 292.4 KB (292421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a90dea8b1328167473598879d3d8ae5cd35c5b9d38f71e564048508f36f480`  
		Last Modified: Fri, 27 Dec 2019 01:42:11 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088a6d26f3541384ac6226cf8876d6800e4dc32c8df94dc0e87f64d54255bf77`  
		Last Modified: Fri, 27 Dec 2019 01:42:28 GMT  
		Size: 491.3 KB (491325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cca1db379551a860110c933ffc9f8a9b002fbe68dbd9c47b1c159bd3df5d57a`  
		Last Modified: Fri, 27 Dec 2019 01:42:28 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca725aea994408291d2b335870ac35c8c140c508af81a13a233f35ecf784552`  
		Last Modified: Fri, 27 Dec 2019 01:42:27 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.8` - linux; ppc64le

```console
$ docker pull composer@sha256:52c1d45263498bbfc18e172aaf9cd5f8592ea347ad0235a8709aa5337be110ea
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68392860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ebcce1bc94d5e980ec8ce2ccff63abea11a5e373c9db51a6daf9838738a8b3`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 19:28:37 GMT
ADD file:4d85451a651e236d899cd849617594eb6babf24079f9b2269134ad06d89bdecc in / 
# Tue, 24 Dec 2019 19:28:38 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:21:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:21:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:21:14 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:21:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:21:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:21:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:21:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:21:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:21:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:21:31 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:21:32 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:21:34 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:21:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:21:52 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:26:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:26:57 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:27:14 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:27:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:27:22 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 01:23:47 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 01:24:07 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 01:24:11 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 01:24:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 01:24:15 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 01:24:45 GMT
ENV COMPOSER_VERSION=1.8.6
# Fri, 27 Dec 2019 01:24:53 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 01:24:54 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 01:24:56 GMT
WORKDIR /app
# Fri, 27 Dec 2019 01:24:57 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 01:24:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a5dee701e1e87430161d8fce67e77ee5e132bdbafe165c52490a36df654c7660`  
		Last Modified: Tue, 24 Dec 2019 19:29:09 GMT  
		Size: 2.8 MB (2816482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5787caafdab36524ef14f193793a44b3b5f54da82c98e8152770c2868fd93b11`  
		Last Modified: Thu, 26 Dec 2019 23:13:04 GMT  
		Size: 1.4 MB (1397977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691639ddfd73c88dfeda1734ababccfaed311f9d747bf07d41c6e7fed2880baf`  
		Last Modified: Thu, 26 Dec 2019 23:13:03 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2a706347c576336f1e0145755e4fa707710b3f42dc7d18903fcee51bb72842`  
		Last Modified: Thu, 26 Dec 2019 23:13:02 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c9367473ae473e3b4307b84581a68ce338708fd02c58387ea03ebbf3b336c4`  
		Last Modified: Thu, 26 Dec 2019 23:13:00 GMT  
		Size: 10.3 MB (10264430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce400ab5b594b3c37b04d8ff93ef76324ad103b89b864086646553aa374ae3a`  
		Last Modified: Thu, 26 Dec 2019 23:12:59 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df72cd13deac5a2de7a62833b97945cc48eb13a954c074f0c2ef27d321ad172`  
		Last Modified: Thu, 26 Dec 2019 23:13:09 GMT  
		Size: 17.1 MB (17073151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a993ff611f4ce5c9ad8c688b7d218dfaf24788380583d0b8ff19758b953565b`  
		Last Modified: Thu, 26 Dec 2019 23:12:59 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b2a23101f41428ee2ad1948c90b3eaf9cda596853a790ebdb59a2e5f3a4353`  
		Last Modified: Thu, 26 Dec 2019 23:12:59 GMT  
		Size: 73.0 KB (73011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c481dd45fa62f76d142285ca14edc35411b4ea549c65fa328636265afec673`  
		Last Modified: Fri, 27 Dec 2019 01:25:27 GMT  
		Size: 36.0 MB (35979323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5e3a68f6ae205b4e6572bf9337334694abcf7dfe1e953aeda6fe3d3953efaf`  
		Last Modified: Fri, 27 Dec 2019 01:25:16 GMT  
		Size: 291.9 KB (291945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cceb98b5eab7c70364129cb95652d435f2c30fa63e2235def0ca4fbd5c83fb8`  
		Last Modified: Fri, 27 Dec 2019 01:25:16 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1544ce33f90c2e59545b36d1231bfabc9896be5e6d071f6946d94fe0fa0017b6`  
		Last Modified: Fri, 27 Dec 2019 01:25:45 GMT  
		Size: 491.4 KB (491369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8c53bfe120b53dc8d70bd44bddd9a1e59affbaec784f5682ac9d47e007e122`  
		Last Modified: Fri, 27 Dec 2019 01:25:45 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fd49c3f5e36685c8b42a520aa1fb722dbff912496279cd59177dcebc79f4f3`  
		Last Modified: Fri, 27 Dec 2019 01:25:44 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `composer:1.8.6`

```console
$ docker pull composer@sha256:bfdac7f094277961b6d00386129d8a54ff5173f88caef2b2f22e06055872df4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `composer:1.8.6` - linux; amd64

```console
$ docker pull composer@sha256:45e8d6643df9c498a057dc5df4b7e9e320870f6dce0e0f1ef36cd28260d121ee
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66201172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e4272d8577f725edc3045421292df51d8cb6805823ce1798bbc9c99e9344ce`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:47:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 21:47:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 21:47:52 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 21:47:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 21:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 21:47:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:47:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:47:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 21:47:55 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 21:47:55 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 21:47:55 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 21:47:55 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 21:47:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 21:47:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:55:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 21:55:56 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:55:58 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 21:55:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 21:55:58 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 03:48:37 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 03:48:47 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 03:48:47 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 03:48:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 03:48:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 03:48:54 GMT
ENV COMPOSER_VERSION=1.8.6
# Fri, 27 Dec 2019 03:48:55 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 03:48:55 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 03:48:55 GMT
WORKDIR /app
# Fri, 27 Dec 2019 03:48:56 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 03:48:56 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7a574e8632727fe466d1871c39e4fea951243dc9f0a56bdc55cb8720f4aac6`  
		Last Modified: Thu, 26 Dec 2019 23:05:01 GMT  
		Size: 1.4 MB (1354713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6c65f587e94ae6bd946a70d456e75c7543d38cb03271622a815f3b5398ec74`  
		Last Modified: Thu, 26 Dec 2019 23:05:00 GMT  
		Size: 1.2 KB (1227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba33e4b639bb4e1187590b34ea007a27393fbda41d6f3ad10d04c9a0bd1cde4a`  
		Last Modified: Thu, 26 Dec 2019 23:05:00 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94182f10949f8b172016cbddea1d7b4417514c40d0fd664a0895d3b0f93fcbe`  
		Last Modified: Thu, 26 Dec 2019 23:05:00 GMT  
		Size: 10.3 MB (10264403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06b2b4baeabcdc2692442b4f6a6512b1f6b20697c8ec9b984503705cc81039a`  
		Last Modified: Thu, 26 Dec 2019 23:04:59 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6abb9ac3b49074e4561b65dbf3c4beaab0b50ef72743a04656dd6e664bcdecc`  
		Last Modified: Thu, 26 Dec 2019 23:05:03 GMT  
		Size: 16.2 MB (16158246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8028c0b7a7e712cf77e535c0d109ae5bce6ae34cefcd8ebf46b640214b5c91`  
		Last Modified: Thu, 26 Dec 2019 23:04:59 GMT  
		Size: 2.2 KB (2217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cc7bad024a2e7896c445c24345d1b9226c1c7ed0adbc57145db4d8ce9aea2f`  
		Last Modified: Thu, 26 Dec 2019 23:04:59 GMT  
		Size: 73.2 KB (73165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc711a535acb29705350d1595ce40c1748951322b88a6413245a4d2a5b7f645`  
		Last Modified: Fri, 27 Dec 2019 03:49:14 GMT  
		Size: 34.8 MB (34774961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5788687df725e868549f29349dd7e546295b632f970634f2b97660aa15c10c9`  
		Last Modified: Fri, 27 Dec 2019 03:49:06 GMT  
		Size: 277.5 KB (277531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91a01e20dbd8ec111d179be5a7d9f856c2018938a07f94ce1de5f111907de97`  
		Last Modified: Fri, 27 Dec 2019 03:49:06 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90bdda6211d42845b95041bd3d4316f0c8b72436a3c51ee3389e11b163e9e3`  
		Last Modified: Fri, 27 Dec 2019 03:49:19 GMT  
		Size: 491.3 KB (491316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928b13c387920b76bc6e604910557c2215932762eca439777a64b8de83380cbc`  
		Last Modified: Fri, 27 Dec 2019 03:49:19 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d48b97065c31a6d92057bcda5eacabc4dfa96bc8881943fe66159e68e52de5`  
		Last Modified: Fri, 27 Dec 2019 03:49:19 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.8.6` - linux; arm variant v6

```console
$ docker pull composer@sha256:2d136210a534efda6603f0c80e6c16e1118cfce1a3056f45dc032301f182bc4d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64107864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842b3b89588e6ef46c0f56117dc5d590a8a17d84736bb93e45b73086208bc81d`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:20:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:20:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:20:18 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:20:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:20:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:20:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:20:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:20:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:20:24 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:20:25 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:20:26 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:20:27 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:20:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:20:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:24:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:24:26 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:24:30 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:24:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:24:35 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 01:32:05 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 01:32:22 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 01:32:24 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 01:32:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 01:32:26 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 01:32:51 GMT
ENV COMPOSER_VERSION=1.8.6
# Fri, 27 Dec 2019 01:32:55 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 01:32:55 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 01:32:57 GMT
WORKDIR /app
# Fri, 27 Dec 2019 01:32:58 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 01:33:01 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f2222aeb0ea56ad08de7753e2ed3f6c40f7093cda7436e94583ce0f0922072`  
		Last Modified: Thu, 26 Dec 2019 23:02:36 GMT  
		Size: 1.3 MB (1321130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f893e696ec7590309f1a77539ce734af052f1aa42c48aaf6f478453dcd7eafa`  
		Last Modified: Thu, 26 Dec 2019 23:02:35 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ad230ebfba33233fbafdd19ca2939dfd20dffdc83636c23f9285017935fca9`  
		Last Modified: Thu, 26 Dec 2019 23:02:35 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44905e88daf12c640968d3d790a02e11babe5d4f4730e6fcd3eae081f8df2f62`  
		Last Modified: Thu, 26 Dec 2019 23:02:34 GMT  
		Size: 10.3 MB (10264410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e91ff6ebef94b35989b1200b9d2564b71aa5e20f03fbc2c75bf57786cdca79`  
		Last Modified: Thu, 26 Dec 2019 23:02:34 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6b1bfceee6e3798ac6b36213aede482172b522e4c9d17635d9418419bd0672`  
		Last Modified: Thu, 26 Dec 2019 23:02:39 GMT  
		Size: 15.0 MB (14962846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6b063069fde53011cbbab0f1fc6cb9f8b02fb20f6f0e986394d971347f38c0`  
		Last Modified: Thu, 26 Dec 2019 23:02:34 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f29f685cf530bfbe1b0003111bed088314ef583a2585bb11a10d7463dfc5dd8`  
		Last Modified: Thu, 26 Dec 2019 23:02:34 GMT  
		Size: 72.7 KB (72680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa550c82c0fdd2e85ec9b9b51732a4590f1a279d6856aa6bd427e28a5571260`  
		Last Modified: Fri, 27 Dec 2019 01:33:31 GMT  
		Size: 34.1 MB (34107571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9770e9484fb6fd2b55324ba5ef682f2a2b1f08bb3dbcf502ca8ecf32cf0c8f`  
		Last Modified: Fri, 27 Dec 2019 01:33:16 GMT  
		Size: 270.7 KB (270675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1f90781495ee403d3826a9f593fde90d3657e5f87f2bc0d757d74c7b4435ab`  
		Last Modified: Fri, 27 Dec 2019 01:33:16 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5278924a8ef7ad9d80d4ce31a0c33b12e80242f38aceba375f418fd3f28c7d82`  
		Last Modified: Fri, 27 Dec 2019 01:33:41 GMT  
		Size: 491.4 KB (491363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3675101bcd4a1795bfa3c0e8b263fc5e19abc3d247975d137070868ee3f2bff0`  
		Last Modified: Fri, 27 Dec 2019 01:33:41 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb89ac22ffc978d304fb106ed408f9d09459254e5f0f0390a7c1ec5c6b94cca`  
		Last Modified: Fri, 27 Dec 2019 01:33:41 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.8.6` - linux; arm variant v7

```console
$ docker pull composer@sha256:c9687df66e63087f4cc85c41b4d4865d4c0f2c2b5c4917887059b37b81031f12
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61383216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bcdd5c1732e13ea3103fd5548a5be8b33f85b9a153d54860a01699679e0786`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 18:59:09 GMT
ADD file:caf7ca25875eddd2bfa2d1e56663bb52d278a85f6ee1314f9ccf01dc4da8070a in / 
# Tue, 24 Dec 2019 18:59:10 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:28:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 21:28:59 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 21:29:01 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 21:29:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 21:29:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 21:29:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:29:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:29:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 21:29:05 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 21:29:05 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 21:29:06 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 21:29:06 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 21:29:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 21:29:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:31:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 21:31:34 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:31:36 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 21:31:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 21:31:38 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 00:05:43 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 00:06:02 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 00:06:04 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 00:06:04 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 00:06:05 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 00:06:22 GMT
ENV COMPOSER_VERSION=1.8.6
# Fri, 27 Dec 2019 00:06:26 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 00:06:27 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 00:06:28 GMT
WORKDIR /app
# Fri, 27 Dec 2019 00:06:29 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 00:06:30 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:3922e475e500b2739b5e74787fc80622853325822f71f8bd3de7e5b09654d60f`  
		Last Modified: Tue, 24 Dec 2019 18:59:33 GMT  
		Size: 2.4 MB (2416691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d850653ef66a74bc2f65e933df679895db53bc6e01d23076dbc532056eec8a7`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 1.2 MB (1227347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed0b2f0bcd9c23ef1f79be9d752fea5f714457c75308002cf597d596e8b1c1a`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77de73a7de2b81d6828d80578fc934edf55e039effcf2bb8555e6a0b5864080`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69dc1b35828f88798cdf411520e8541662fa44c3e21d0b46b668e5ad1ce38f24`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 10.3 MB (10264419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1ac53e078b99a6ba0cf4e8600a0ba5aa6bd3b579e0f86d78a3b18bd692976a`  
		Last Modified: Thu, 26 Dec 2019 22:01:16 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a349634f832daa7e54f052c5c5fce54336c7089c5997981c3be8552baf32c10c`  
		Last Modified: Thu, 26 Dec 2019 22:01:21 GMT  
		Size: 14.0 MB (14035302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef07c3ed8c6baead6c71677fb97b0bef1c3762881b234e8ed7aa21c0470854ed`  
		Last Modified: Thu, 26 Dec 2019 22:01:16 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01eab0467fa0094e7e35ef8de9b09468e7ae8b53efc431442a1a9af5a5be310a`  
		Last Modified: Thu, 26 Dec 2019 22:01:16 GMT  
		Size: 72.7 KB (72675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef760acfe9c6c709e6adc3e53bb918efdfbf825221903209bd82018b119c1439`  
		Last Modified: Fri, 27 Dec 2019 00:06:57 GMT  
		Size: 32.6 MB (32605578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51aade9d91ae2843e8ec23f54eea99048fa2d73d2e01cea93889e60c54b4210`  
		Last Modified: Fri, 27 Dec 2019 00:06:44 GMT  
		Size: 264.7 KB (264673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a512d9b12df16845d0df25d19e6307acb404fcf2f3a3862d47f94e2259fb0f23`  
		Last Modified: Fri, 27 Dec 2019 00:06:44 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335b7d5f97bb02adc9d932734c7f524469ed1473ab531bc2afc2b4683e83492c`  
		Last Modified: Fri, 27 Dec 2019 00:07:10 GMT  
		Size: 491.4 KB (491358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b6bb39a91170eba2cd3765ba8c3559febd50d14e873f9785ebc9e6a99384bb`  
		Last Modified: Fri, 27 Dec 2019 00:07:10 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ce943e9a4fad64294bc3cea3c48fcdf06306a5496fa1876b8a9465612528b1`  
		Last Modified: Fri, 27 Dec 2019 00:07:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.8.6` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:41e45473f243c71fb05e0706b94bfa6197f7acd78cc1c083c9dfd598c37f3491
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66197161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27ec7cac3f147803cb4fa9d6b13557570cfa9671344a79accf48438f37cd3cd`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 20:26:15 GMT
ADD file:d6c3db0313ab0c6201770c7248d1bac964011a1c08f1a9b434442b7c21efef87 in / 
# Tue, 24 Dec 2019 20:26:24 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:08:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:08:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:08:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:08:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:08:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:08:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:08:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:08:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:08:38 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:08:39 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:08:40 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:08:40 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:08:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:08:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:12:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:12:26 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:12:30 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:12:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:12:32 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 01:00:35 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 01:01:10 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 01:01:21 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 01:01:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 01:01:34 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 01:02:18 GMT
ENV COMPOSER_VERSION=1.8.6
# Fri, 27 Dec 2019 01:02:22 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 01:02:25 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 01:02:29 GMT
WORKDIR /app
# Fri, 27 Dec 2019 01:02:35 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 01:02:37 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cde5963f3b93eec667cad527c99d80402a5a91a7a1381f7ffe562f215aec0c50`  
		Last Modified: Tue, 24 Dec 2019 20:26:52 GMT  
		Size: 2.7 MB (2719182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36763f956175b40d2a6ca97c274d362c9a0deb76d9b7eb62e95b8ca953bb1db2`  
		Last Modified: Thu, 26 Dec 2019 22:48:41 GMT  
		Size: 1.4 MB (1359427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01374ab459ad592d2c9b91efb836df933906c6cd8c63606db7f385c084fa04d2`  
		Last Modified: Thu, 26 Dec 2019 22:48:40 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34492236b9882b05dc402fe511c10ac8463554a1223a9bd10460daeab25a98f`  
		Last Modified: Thu, 26 Dec 2019 22:48:40 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b0ab5705e600f30f4341814fc44949ef8a0595246e35d6a72d4146fd467f1e`  
		Last Modified: Thu, 26 Dec 2019 22:48:38 GMT  
		Size: 10.3 MB (10264412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8fe4aab7c71980ba6c9c10d2d41202a098e48ef491850ebc67b17a147487d88`  
		Last Modified: Thu, 26 Dec 2019 22:48:38 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f253d45c879751ce17f7944d232be8fcb0e2bc700a5a6714d97a63867aff06`  
		Last Modified: Thu, 26 Dec 2019 22:48:41 GMT  
		Size: 15.9 MB (15851650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805b37c27a0499cf4df7c736ea7581d72e1cb4a6613bda953833b79a80caac1a`  
		Last Modified: Thu, 26 Dec 2019 22:48:38 GMT  
		Size: 2.2 KB (2215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7400940d887ae822a41abe503ec76c4a6e979621ecf316d123cb0d39eb34db`  
		Last Modified: Thu, 26 Dec 2019 22:48:38 GMT  
		Size: 72.7 KB (72682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1a36a335b2a481db4a07619c7e30bdced72bc39e6b6f1ee3715a6cdc603bd1`  
		Last Modified: Fri, 27 Dec 2019 01:03:09 GMT  
		Size: 35.2 MB (35157603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ea079782c565a70581045175e15f46bb937e07e2200ea63b03bf72af221b07`  
		Last Modified: Fri, 27 Dec 2019 01:02:55 GMT  
		Size: 275.7 KB (275669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae534ca14dbc48106ee3f2e81f33b327cf7eb302898c02bb4ab7345cc44b502`  
		Last Modified: Fri, 27 Dec 2019 01:02:55 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328144f18dce602a0069dcbfc04682831ff7c9678904c3fc21b481687a4e90c6`  
		Last Modified: Fri, 27 Dec 2019 01:03:21 GMT  
		Size: 491.4 KB (491363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fb8496f7109fe4f5452fac7aee6af6181d4bdc53a020cadeb776afc7254f4f`  
		Last Modified: Fri, 27 Dec 2019 01:03:22 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589529a410238155419258a930085987eec075a542c59da879e016ae7fcc08bb`  
		Last Modified: Fri, 27 Dec 2019 01:03:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.8.6` - linux; 386

```console
$ docker pull composer@sha256:08f5e4ba228346b7bb0b33ec31b3548cf530ed4e32abfb1bb6633a5f8f2defe2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68283329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be130ddb518628e342f922b553c37b33678eb475ea433d4a3fdf07845e8b06d4`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 19:38:57 GMT
ADD file:d0127a9692e8445993a88163cb741dbb23fa25436dd65289e76b08484264b397 in / 
# Tue, 24 Dec 2019 19:38:57 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:36:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:36:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:36:14 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:36:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:36:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:36:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:36:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:36:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:36:17 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:36:18 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:36:18 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:36:18 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:36:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:36:23 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:45:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:45:50 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:45:51 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:45:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:45:52 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 01:41:40 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 01:41:52 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 01:41:52 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 01:41:52 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 01:41:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 01:42:02 GMT
ENV COMPOSER_VERSION=1.8.6
# Fri, 27 Dec 2019 01:42:03 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 01:42:03 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 01:42:03 GMT
WORKDIR /app
# Fri, 27 Dec 2019 01:42:04 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 01:42:04 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:57bbc6f150623b3e4f01930af4ab2efa6ed5df02319341a08b1ce0bbd7e4afdf`  
		Last Modified: Tue, 24 Dec 2019 19:39:19 GMT  
		Size: 2.8 MB (2805146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db25e971d6f24055202f90f96d257a719817ad73623eaf02d98fb13c2dbe9a1b`  
		Last Modified: Fri, 27 Dec 2019 00:00:12 GMT  
		Size: 1.5 MB (1452611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ecdadbdbb91bc66f820e5b3077004286155b3e618cc444f493d7e73b400333`  
		Last Modified: Fri, 27 Dec 2019 00:00:12 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8331211b40f9489961b63904af5f93f96465efa4f5202ee08600fd1fe3caec6c`  
		Last Modified: Fri, 27 Dec 2019 00:00:11 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1feab22a6dc5f30ac5d6a419e21b0ad02df0633e9376cda5af697a214a1677e`  
		Last Modified: Fri, 27 Dec 2019 00:00:12 GMT  
		Size: 10.3 MB (10264412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f291e0ec174ac10d076b738bdd8d7b5a352fd362d9659a6cb4b7c5cf7e219323`  
		Last Modified: Fri, 27 Dec 2019 00:00:10 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeee04bc33533cf870952c9aab9489299215c7b4a6077fc85ded1a38354bfa34`  
		Last Modified: Fri, 27 Dec 2019 00:00:17 GMT  
		Size: 16.6 MB (16572401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4baee82eaeb4bb25b75b28052d7aec12a58e5f0b9cc3abdccdea6d742bda1e`  
		Last Modified: Fri, 27 Dec 2019 00:00:10 GMT  
		Size: 2.2 KB (2215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01721c87d29cd0ad25164e2a64d81439e2201e730353ea8a64a5324af5aaaa6`  
		Last Modified: Fri, 27 Dec 2019 00:00:10 GMT  
		Size: 72.3 KB (72336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3650f92aaf29753dc8d77c5521fe278f1fc1be26d84d5a01b2931c17fba38029`  
		Last Modified: Fri, 27 Dec 2019 01:42:21 GMT  
		Size: 36.3 MB (36327612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cabc1b7971f28befd3ee5c2117694eaaf4e7750fab49a6718b9de78c706ae4b`  
		Last Modified: Fri, 27 Dec 2019 01:42:11 GMT  
		Size: 292.4 KB (292421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a90dea8b1328167473598879d3d8ae5cd35c5b9d38f71e564048508f36f480`  
		Last Modified: Fri, 27 Dec 2019 01:42:11 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088a6d26f3541384ac6226cf8876d6800e4dc32c8df94dc0e87f64d54255bf77`  
		Last Modified: Fri, 27 Dec 2019 01:42:28 GMT  
		Size: 491.3 KB (491325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cca1db379551a860110c933ffc9f8a9b002fbe68dbd9c47b1c159bd3df5d57a`  
		Last Modified: Fri, 27 Dec 2019 01:42:28 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca725aea994408291d2b335870ac35c8c140c508af81a13a233f35ecf784552`  
		Last Modified: Fri, 27 Dec 2019 01:42:27 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.8.6` - linux; ppc64le

```console
$ docker pull composer@sha256:52c1d45263498bbfc18e172aaf9cd5f8592ea347ad0235a8709aa5337be110ea
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68392860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ebcce1bc94d5e980ec8ce2ccff63abea11a5e373c9db51a6daf9838738a8b3`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 19:28:37 GMT
ADD file:4d85451a651e236d899cd849617594eb6babf24079f9b2269134ad06d89bdecc in / 
# Tue, 24 Dec 2019 19:28:38 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:21:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:21:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:21:14 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:21:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:21:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:21:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:21:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:21:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:21:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:21:31 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:21:32 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:21:34 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:21:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:21:52 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:26:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:26:57 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:27:14 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:27:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:27:22 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 01:23:47 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 01:24:07 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 01:24:11 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 01:24:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 01:24:15 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 01:24:45 GMT
ENV COMPOSER_VERSION=1.8.6
# Fri, 27 Dec 2019 01:24:53 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 01:24:54 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 01:24:56 GMT
WORKDIR /app
# Fri, 27 Dec 2019 01:24:57 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 01:24:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a5dee701e1e87430161d8fce67e77ee5e132bdbafe165c52490a36df654c7660`  
		Last Modified: Tue, 24 Dec 2019 19:29:09 GMT  
		Size: 2.8 MB (2816482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5787caafdab36524ef14f193793a44b3b5f54da82c98e8152770c2868fd93b11`  
		Last Modified: Thu, 26 Dec 2019 23:13:04 GMT  
		Size: 1.4 MB (1397977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691639ddfd73c88dfeda1734ababccfaed311f9d747bf07d41c6e7fed2880baf`  
		Last Modified: Thu, 26 Dec 2019 23:13:03 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2a706347c576336f1e0145755e4fa707710b3f42dc7d18903fcee51bb72842`  
		Last Modified: Thu, 26 Dec 2019 23:13:02 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c9367473ae473e3b4307b84581a68ce338708fd02c58387ea03ebbf3b336c4`  
		Last Modified: Thu, 26 Dec 2019 23:13:00 GMT  
		Size: 10.3 MB (10264430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce400ab5b594b3c37b04d8ff93ef76324ad103b89b864086646553aa374ae3a`  
		Last Modified: Thu, 26 Dec 2019 23:12:59 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df72cd13deac5a2de7a62833b97945cc48eb13a954c074f0c2ef27d321ad172`  
		Last Modified: Thu, 26 Dec 2019 23:13:09 GMT  
		Size: 17.1 MB (17073151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a993ff611f4ce5c9ad8c688b7d218dfaf24788380583d0b8ff19758b953565b`  
		Last Modified: Thu, 26 Dec 2019 23:12:59 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b2a23101f41428ee2ad1948c90b3eaf9cda596853a790ebdb59a2e5f3a4353`  
		Last Modified: Thu, 26 Dec 2019 23:12:59 GMT  
		Size: 73.0 KB (73011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c481dd45fa62f76d142285ca14edc35411b4ea549c65fa328636265afec673`  
		Last Modified: Fri, 27 Dec 2019 01:25:27 GMT  
		Size: 36.0 MB (35979323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5e3a68f6ae205b4e6572bf9337334694abcf7dfe1e953aeda6fe3d3953efaf`  
		Last Modified: Fri, 27 Dec 2019 01:25:16 GMT  
		Size: 291.9 KB (291945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cceb98b5eab7c70364129cb95652d435f2c30fa63e2235def0ca4fbd5c83fb8`  
		Last Modified: Fri, 27 Dec 2019 01:25:16 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1544ce33f90c2e59545b36d1231bfabc9896be5e6d071f6946d94fe0fa0017b6`  
		Last Modified: Fri, 27 Dec 2019 01:25:45 GMT  
		Size: 491.4 KB (491369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8c53bfe120b53dc8d70bd44bddd9a1e59affbaec784f5682ac9d47e007e122`  
		Last Modified: Fri, 27 Dec 2019 01:25:45 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fd49c3f5e36685c8b42a520aa1fb722dbff912496279cd59177dcebc79f4f3`  
		Last Modified: Fri, 27 Dec 2019 01:25:44 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `composer:1.9`

```console
$ docker pull composer@sha256:75a6a13680d0be7074f1c52f78f508751258d002c6e3934a7d5c332739f2b201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `composer:1.9` - linux; amd64

```console
$ docker pull composer@sha256:fdbee4b29a1bcca79b12fdced7d9221eb6cc28832b9e00ab2e7c6726f20ca8cc
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66206861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02efded7ec8009b7a35bf247573592efffbe0f382d3c0e3dd07becb80565505`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:47:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 21:47:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 21:47:52 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 21:47:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 21:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 21:47:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:47:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:47:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 21:47:55 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 21:47:55 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 21:47:55 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 21:47:55 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 21:47:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 21:47:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:55:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 21:55:56 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:55:58 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 21:55:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 21:55:58 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 03:48:37 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 03:48:47 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 03:48:47 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 03:48:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 03:48:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 03:48:48 GMT
ENV COMPOSER_VERSION=1.9.1
# Fri, 27 Dec 2019 03:48:49 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 03:48:49 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 03:48:49 GMT
WORKDIR /app
# Fri, 27 Dec 2019 03:48:50 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 03:48:50 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7a574e8632727fe466d1871c39e4fea951243dc9f0a56bdc55cb8720f4aac6`  
		Last Modified: Thu, 26 Dec 2019 23:05:01 GMT  
		Size: 1.4 MB (1354713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6c65f587e94ae6bd946a70d456e75c7543d38cb03271622a815f3b5398ec74`  
		Last Modified: Thu, 26 Dec 2019 23:05:00 GMT  
		Size: 1.2 KB (1227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba33e4b639bb4e1187590b34ea007a27393fbda41d6f3ad10d04c9a0bd1cde4a`  
		Last Modified: Thu, 26 Dec 2019 23:05:00 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94182f10949f8b172016cbddea1d7b4417514c40d0fd664a0895d3b0f93fcbe`  
		Last Modified: Thu, 26 Dec 2019 23:05:00 GMT  
		Size: 10.3 MB (10264403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06b2b4baeabcdc2692442b4f6a6512b1f6b20697c8ec9b984503705cc81039a`  
		Last Modified: Thu, 26 Dec 2019 23:04:59 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6abb9ac3b49074e4561b65dbf3c4beaab0b50ef72743a04656dd6e664bcdecc`  
		Last Modified: Thu, 26 Dec 2019 23:05:03 GMT  
		Size: 16.2 MB (16158246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8028c0b7a7e712cf77e535c0d109ae5bce6ae34cefcd8ebf46b640214b5c91`  
		Last Modified: Thu, 26 Dec 2019 23:04:59 GMT  
		Size: 2.2 KB (2217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cc7bad024a2e7896c445c24345d1b9226c1c7ed0adbc57145db4d8ce9aea2f`  
		Last Modified: Thu, 26 Dec 2019 23:04:59 GMT  
		Size: 73.2 KB (73165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc711a535acb29705350d1595ce40c1748951322b88a6413245a4d2a5b7f645`  
		Last Modified: Fri, 27 Dec 2019 03:49:14 GMT  
		Size: 34.8 MB (34774961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5788687df725e868549f29349dd7e546295b632f970634f2b97660aa15c10c9`  
		Last Modified: Fri, 27 Dec 2019 03:49:06 GMT  
		Size: 277.5 KB (277531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91a01e20dbd8ec111d179be5a7d9f856c2018938a07f94ce1de5f111907de97`  
		Last Modified: Fri, 27 Dec 2019 03:49:06 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c853bffcbc704b657c099fa2a3cc9c10919552af9a3e0a2d8ae4a42e6782eb`  
		Last Modified: Fri, 27 Dec 2019 03:49:06 GMT  
		Size: 497.0 KB (497005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0d79794dfc6b4b090401c350caf4bfcb0c038672d8c0a28d3d822838f9dcd2`  
		Last Modified: Fri, 27 Dec 2019 03:49:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fac451fab2e34ab918bfe33533c77b938fe2bcb55ff4680a6468d524e1c69a6`  
		Last Modified: Fri, 27 Dec 2019 03:49:06 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.9` - linux; arm variant v6

```console
$ docker pull composer@sha256:dd97b87c2947f5c3a5a55e9e6153cf324920f5747918d25b6ec90cebdc44087e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64113537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fcb94b450243c8357d8679a6da332460fbcf60f735dc84e44f27f87554e02c6`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:20:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:20:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:20:18 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:20:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:20:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:20:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:20:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:20:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:20:24 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:20:25 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:20:26 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:20:27 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:20:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:20:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:24:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:24:26 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:24:30 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:24:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:24:35 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 01:32:05 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 01:32:22 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 01:32:24 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 01:32:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 01:32:26 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 01:32:26 GMT
ENV COMPOSER_VERSION=1.9.1
# Fri, 27 Dec 2019 01:32:29 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 01:32:29 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 01:32:33 GMT
WORKDIR /app
# Fri, 27 Dec 2019 01:32:36 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 01:32:39 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f2222aeb0ea56ad08de7753e2ed3f6c40f7093cda7436e94583ce0f0922072`  
		Last Modified: Thu, 26 Dec 2019 23:02:36 GMT  
		Size: 1.3 MB (1321130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f893e696ec7590309f1a77539ce734af052f1aa42c48aaf6f478453dcd7eafa`  
		Last Modified: Thu, 26 Dec 2019 23:02:35 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ad230ebfba33233fbafdd19ca2939dfd20dffdc83636c23f9285017935fca9`  
		Last Modified: Thu, 26 Dec 2019 23:02:35 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44905e88daf12c640968d3d790a02e11babe5d4f4730e6fcd3eae081f8df2f62`  
		Last Modified: Thu, 26 Dec 2019 23:02:34 GMT  
		Size: 10.3 MB (10264410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e91ff6ebef94b35989b1200b9d2564b71aa5e20f03fbc2c75bf57786cdca79`  
		Last Modified: Thu, 26 Dec 2019 23:02:34 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6b1bfceee6e3798ac6b36213aede482172b522e4c9d17635d9418419bd0672`  
		Last Modified: Thu, 26 Dec 2019 23:02:39 GMT  
		Size: 15.0 MB (14962846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6b063069fde53011cbbab0f1fc6cb9f8b02fb20f6f0e986394d971347f38c0`  
		Last Modified: Thu, 26 Dec 2019 23:02:34 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f29f685cf530bfbe1b0003111bed088314ef583a2585bb11a10d7463dfc5dd8`  
		Last Modified: Thu, 26 Dec 2019 23:02:34 GMT  
		Size: 72.7 KB (72680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa550c82c0fdd2e85ec9b9b51732a4590f1a279d6856aa6bd427e28a5571260`  
		Last Modified: Fri, 27 Dec 2019 01:33:31 GMT  
		Size: 34.1 MB (34107571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9770e9484fb6fd2b55324ba5ef682f2a2b1f08bb3dbcf502ca8ecf32cf0c8f`  
		Last Modified: Fri, 27 Dec 2019 01:33:16 GMT  
		Size: 270.7 KB (270675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1f90781495ee403d3826a9f593fde90d3657e5f87f2bc0d757d74c7b4435ab`  
		Last Modified: Fri, 27 Dec 2019 01:33:16 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5ee0bd8ba874c58e5a766515b76e4d85166155f92d996c24c3a26f0ebc5138`  
		Last Modified: Fri, 27 Dec 2019 01:33:16 GMT  
		Size: 497.0 KB (497035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c38f9121f497e45f2517272c56a59f4a5992b6274fb6d9685b1100f69512c2`  
		Last Modified: Fri, 27 Dec 2019 01:33:16 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36b2e72ff9d80d06d651f66bd8bd8f258ccf15e4c6c144bd710e16fae8aea73`  
		Last Modified: Fri, 27 Dec 2019 01:33:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.9` - linux; arm variant v7

```console
$ docker pull composer@sha256:f677de2a63ff1ae9145160a6605ea45bc413e58b4bdf8d4cb91263130c945bcf
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61388895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9012e1c5224f7b7e3ec0077971ad126503067b41b3e53da4df6c6012c3aa112`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 18:59:09 GMT
ADD file:caf7ca25875eddd2bfa2d1e56663bb52d278a85f6ee1314f9ccf01dc4da8070a in / 
# Tue, 24 Dec 2019 18:59:10 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:28:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 21:28:59 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 21:29:01 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 21:29:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 21:29:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 21:29:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:29:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:29:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 21:29:05 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 21:29:05 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 21:29:06 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 21:29:06 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 21:29:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 21:29:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:31:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 21:31:34 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:31:36 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 21:31:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 21:31:38 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 00:05:43 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 00:06:02 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 00:06:04 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 00:06:04 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 00:06:05 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 00:06:06 GMT
ENV COMPOSER_VERSION=1.9.1
# Fri, 27 Dec 2019 00:06:09 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 00:06:10 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 00:06:11 GMT
WORKDIR /app
# Fri, 27 Dec 2019 00:06:13 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 00:06:15 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:3922e475e500b2739b5e74787fc80622853325822f71f8bd3de7e5b09654d60f`  
		Last Modified: Tue, 24 Dec 2019 18:59:33 GMT  
		Size: 2.4 MB (2416691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d850653ef66a74bc2f65e933df679895db53bc6e01d23076dbc532056eec8a7`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 1.2 MB (1227347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed0b2f0bcd9c23ef1f79be9d752fea5f714457c75308002cf597d596e8b1c1a`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77de73a7de2b81d6828d80578fc934edf55e039effcf2bb8555e6a0b5864080`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69dc1b35828f88798cdf411520e8541662fa44c3e21d0b46b668e5ad1ce38f24`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 10.3 MB (10264419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1ac53e078b99a6ba0cf4e8600a0ba5aa6bd3b579e0f86d78a3b18bd692976a`  
		Last Modified: Thu, 26 Dec 2019 22:01:16 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a349634f832daa7e54f052c5c5fce54336c7089c5997981c3be8552baf32c10c`  
		Last Modified: Thu, 26 Dec 2019 22:01:21 GMT  
		Size: 14.0 MB (14035302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef07c3ed8c6baead6c71677fb97b0bef1c3762881b234e8ed7aa21c0470854ed`  
		Last Modified: Thu, 26 Dec 2019 22:01:16 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01eab0467fa0094e7e35ef8de9b09468e7ae8b53efc431442a1a9af5a5be310a`  
		Last Modified: Thu, 26 Dec 2019 22:01:16 GMT  
		Size: 72.7 KB (72675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef760acfe9c6c709e6adc3e53bb918efdfbf825221903209bd82018b119c1439`  
		Last Modified: Fri, 27 Dec 2019 00:06:57 GMT  
		Size: 32.6 MB (32605578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51aade9d91ae2843e8ec23f54eea99048fa2d73d2e01cea93889e60c54b4210`  
		Last Modified: Fri, 27 Dec 2019 00:06:44 GMT  
		Size: 264.7 KB (264673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a512d9b12df16845d0df25d19e6307acb404fcf2f3a3862d47f94e2259fb0f23`  
		Last Modified: Fri, 27 Dec 2019 00:06:44 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cde7a20d9972695c743aa2a0e922361370380dbef712fea1617d181bbe4fc`  
		Last Modified: Fri, 27 Dec 2019 00:06:44 GMT  
		Size: 497.0 KB (497037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852bb277a6ed901b13ff9be031f1aa4b6a5e313dfb998b3c6c5f10055a93e3a2`  
		Last Modified: Fri, 27 Dec 2019 00:06:44 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce34df92ca04dd2bdf3e2373fc25a8a172c772c16ad3b38cfa6f9e63eddb7e46`  
		Last Modified: Fri, 27 Dec 2019 00:06:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.9` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:baf042a8b58480a86b9a613750042c985cd23d66830d12ef6dbd874cd5ff2b77
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66202831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a184fefdede0cf61596a9690935c94a10a964cdbca862d66a76da536cdbbb4c4`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 20:26:15 GMT
ADD file:d6c3db0313ab0c6201770c7248d1bac964011a1c08f1a9b434442b7c21efef87 in / 
# Tue, 24 Dec 2019 20:26:24 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:08:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:08:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:08:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:08:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:08:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:08:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:08:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:08:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:08:38 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:08:39 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:08:40 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:08:40 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:08:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:08:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:12:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:12:26 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:12:30 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:12:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:12:32 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 01:00:35 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 01:01:10 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 01:01:21 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 01:01:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 01:01:34 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 01:01:38 GMT
ENV COMPOSER_VERSION=1.9.1
# Fri, 27 Dec 2019 01:01:54 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 01:01:56 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 01:02:01 GMT
WORKDIR /app
# Fri, 27 Dec 2019 01:02:03 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 01:02:05 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cde5963f3b93eec667cad527c99d80402a5a91a7a1381f7ffe562f215aec0c50`  
		Last Modified: Tue, 24 Dec 2019 20:26:52 GMT  
		Size: 2.7 MB (2719182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36763f956175b40d2a6ca97c274d362c9a0deb76d9b7eb62e95b8ca953bb1db2`  
		Last Modified: Thu, 26 Dec 2019 22:48:41 GMT  
		Size: 1.4 MB (1359427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01374ab459ad592d2c9b91efb836df933906c6cd8c63606db7f385c084fa04d2`  
		Last Modified: Thu, 26 Dec 2019 22:48:40 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34492236b9882b05dc402fe511c10ac8463554a1223a9bd10460daeab25a98f`  
		Last Modified: Thu, 26 Dec 2019 22:48:40 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b0ab5705e600f30f4341814fc44949ef8a0595246e35d6a72d4146fd467f1e`  
		Last Modified: Thu, 26 Dec 2019 22:48:38 GMT  
		Size: 10.3 MB (10264412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8fe4aab7c71980ba6c9c10d2d41202a098e48ef491850ebc67b17a147487d88`  
		Last Modified: Thu, 26 Dec 2019 22:48:38 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f253d45c879751ce17f7944d232be8fcb0e2bc700a5a6714d97a63867aff06`  
		Last Modified: Thu, 26 Dec 2019 22:48:41 GMT  
		Size: 15.9 MB (15851650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805b37c27a0499cf4df7c736ea7581d72e1cb4a6613bda953833b79a80caac1a`  
		Last Modified: Thu, 26 Dec 2019 22:48:38 GMT  
		Size: 2.2 KB (2215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7400940d887ae822a41abe503ec76c4a6e979621ecf316d123cb0d39eb34db`  
		Last Modified: Thu, 26 Dec 2019 22:48:38 GMT  
		Size: 72.7 KB (72682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1a36a335b2a481db4a07619c7e30bdced72bc39e6b6f1ee3715a6cdc603bd1`  
		Last Modified: Fri, 27 Dec 2019 01:03:09 GMT  
		Size: 35.2 MB (35157603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ea079782c565a70581045175e15f46bb937e07e2200ea63b03bf72af221b07`  
		Last Modified: Fri, 27 Dec 2019 01:02:55 GMT  
		Size: 275.7 KB (275669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae534ca14dbc48106ee3f2e81f33b327cf7eb302898c02bb4ab7345cc44b502`  
		Last Modified: Fri, 27 Dec 2019 01:02:55 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9f707e568acdc4ac64f6df65d1da26a796d239543900581845647ae7cc94df`  
		Last Modified: Fri, 27 Dec 2019 01:02:55 GMT  
		Size: 497.0 KB (497033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38530d4206c9f562e53cadc427a46c8e2adf48db5da189fae8d33fa45f587f3`  
		Last Modified: Fri, 27 Dec 2019 01:02:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d6873676bd3565875ec532df054c50b52dc9d79b2ec8f6e43f5ce27e78b2b1`  
		Last Modified: Fri, 27 Dec 2019 01:02:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.9` - linux; 386

```console
$ docker pull composer@sha256:eb104347bdbea942b571973f68326dce69ae3c92dfe7aa331d88298dc4d5c493
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68289013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb946c124f051f09f714c35fd6e2529d6707c10ec140737cf56e882111bcd82`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 19:38:57 GMT
ADD file:d0127a9692e8445993a88163cb741dbb23fa25436dd65289e76b08484264b397 in / 
# Tue, 24 Dec 2019 19:38:57 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:36:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:36:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:36:14 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:36:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:36:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:36:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:36:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:36:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:36:17 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:36:18 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:36:18 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:36:18 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:36:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:36:23 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:45:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:45:50 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:45:51 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:45:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:45:52 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 01:41:40 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 01:41:52 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 01:41:52 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 01:41:52 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 01:41:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 01:41:53 GMT
ENV COMPOSER_VERSION=1.9.1
# Fri, 27 Dec 2019 01:41:54 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 01:41:54 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 01:41:54 GMT
WORKDIR /app
# Fri, 27 Dec 2019 01:41:55 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 01:41:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:57bbc6f150623b3e4f01930af4ab2efa6ed5df02319341a08b1ce0bbd7e4afdf`  
		Last Modified: Tue, 24 Dec 2019 19:39:19 GMT  
		Size: 2.8 MB (2805146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db25e971d6f24055202f90f96d257a719817ad73623eaf02d98fb13c2dbe9a1b`  
		Last Modified: Fri, 27 Dec 2019 00:00:12 GMT  
		Size: 1.5 MB (1452611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ecdadbdbb91bc66f820e5b3077004286155b3e618cc444f493d7e73b400333`  
		Last Modified: Fri, 27 Dec 2019 00:00:12 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8331211b40f9489961b63904af5f93f96465efa4f5202ee08600fd1fe3caec6c`  
		Last Modified: Fri, 27 Dec 2019 00:00:11 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1feab22a6dc5f30ac5d6a419e21b0ad02df0633e9376cda5af697a214a1677e`  
		Last Modified: Fri, 27 Dec 2019 00:00:12 GMT  
		Size: 10.3 MB (10264412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f291e0ec174ac10d076b738bdd8d7b5a352fd362d9659a6cb4b7c5cf7e219323`  
		Last Modified: Fri, 27 Dec 2019 00:00:10 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeee04bc33533cf870952c9aab9489299215c7b4a6077fc85ded1a38354bfa34`  
		Last Modified: Fri, 27 Dec 2019 00:00:17 GMT  
		Size: 16.6 MB (16572401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4baee82eaeb4bb25b75b28052d7aec12a58e5f0b9cc3abdccdea6d742bda1e`  
		Last Modified: Fri, 27 Dec 2019 00:00:10 GMT  
		Size: 2.2 KB (2215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01721c87d29cd0ad25164e2a64d81439e2201e730353ea8a64a5324af5aaaa6`  
		Last Modified: Fri, 27 Dec 2019 00:00:10 GMT  
		Size: 72.3 KB (72336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3650f92aaf29753dc8d77c5521fe278f1fc1be26d84d5a01b2931c17fba38029`  
		Last Modified: Fri, 27 Dec 2019 01:42:21 GMT  
		Size: 36.3 MB (36327612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cabc1b7971f28befd3ee5c2117694eaaf4e7750fab49a6718b9de78c706ae4b`  
		Last Modified: Fri, 27 Dec 2019 01:42:11 GMT  
		Size: 292.4 KB (292421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a90dea8b1328167473598879d3d8ae5cd35c5b9d38f71e564048508f36f480`  
		Last Modified: Fri, 27 Dec 2019 01:42:11 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f18de3cac22e1e5f06fcdcdc7c32966859717887c9de60785ce0af29c1fd4ca`  
		Last Modified: Fri, 27 Dec 2019 01:42:11 GMT  
		Size: 497.0 KB (497009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392481b4d02274d120941ac388bec69fbb9ac1c1dc3e951b48156c2b1bb5def6`  
		Last Modified: Fri, 27 Dec 2019 01:42:11 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f279761684374c3e2dfc98ed41d387bae19d174837ef1e03e16e2c72696f126b`  
		Last Modified: Fri, 27 Dec 2019 01:42:11 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.9` - linux; ppc64le

```console
$ docker pull composer@sha256:d4d9899d9faa184331bc4a29f410d7ad97c617303ddecc1cb7512d79490ec254
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68398531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058a3b17db3adc1e4a850d3509a225280c8618a5496c9cacddb5c48ef1b37da4`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 19:28:37 GMT
ADD file:4d85451a651e236d899cd849617594eb6babf24079f9b2269134ad06d89bdecc in / 
# Tue, 24 Dec 2019 19:28:38 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:21:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:21:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:21:14 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:21:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:21:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:21:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:21:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:21:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:21:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:21:31 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:21:32 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:21:34 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:21:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:21:52 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:26:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:26:57 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:27:14 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:27:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:27:22 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 01:23:47 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 01:24:07 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 01:24:11 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 01:24:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 01:24:15 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 01:24:17 GMT
ENV COMPOSER_VERSION=1.9.1
# Fri, 27 Dec 2019 01:24:22 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 01:24:24 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 01:24:25 GMT
WORKDIR /app
# Fri, 27 Dec 2019 01:24:27 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 01:24:29 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a5dee701e1e87430161d8fce67e77ee5e132bdbafe165c52490a36df654c7660`  
		Last Modified: Tue, 24 Dec 2019 19:29:09 GMT  
		Size: 2.8 MB (2816482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5787caafdab36524ef14f193793a44b3b5f54da82c98e8152770c2868fd93b11`  
		Last Modified: Thu, 26 Dec 2019 23:13:04 GMT  
		Size: 1.4 MB (1397977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691639ddfd73c88dfeda1734ababccfaed311f9d747bf07d41c6e7fed2880baf`  
		Last Modified: Thu, 26 Dec 2019 23:13:03 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2a706347c576336f1e0145755e4fa707710b3f42dc7d18903fcee51bb72842`  
		Last Modified: Thu, 26 Dec 2019 23:13:02 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c9367473ae473e3b4307b84581a68ce338708fd02c58387ea03ebbf3b336c4`  
		Last Modified: Thu, 26 Dec 2019 23:13:00 GMT  
		Size: 10.3 MB (10264430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce400ab5b594b3c37b04d8ff93ef76324ad103b89b864086646553aa374ae3a`  
		Last Modified: Thu, 26 Dec 2019 23:12:59 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df72cd13deac5a2de7a62833b97945cc48eb13a954c074f0c2ef27d321ad172`  
		Last Modified: Thu, 26 Dec 2019 23:13:09 GMT  
		Size: 17.1 MB (17073151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a993ff611f4ce5c9ad8c688b7d218dfaf24788380583d0b8ff19758b953565b`  
		Last Modified: Thu, 26 Dec 2019 23:12:59 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b2a23101f41428ee2ad1948c90b3eaf9cda596853a790ebdb59a2e5f3a4353`  
		Last Modified: Thu, 26 Dec 2019 23:12:59 GMT  
		Size: 73.0 KB (73011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c481dd45fa62f76d142285ca14edc35411b4ea549c65fa328636265afec673`  
		Last Modified: Fri, 27 Dec 2019 01:25:27 GMT  
		Size: 36.0 MB (35979323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5e3a68f6ae205b4e6572bf9337334694abcf7dfe1e953aeda6fe3d3953efaf`  
		Last Modified: Fri, 27 Dec 2019 01:25:16 GMT  
		Size: 291.9 KB (291945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cceb98b5eab7c70364129cb95652d435f2c30fa63e2235def0ca4fbd5c83fb8`  
		Last Modified: Fri, 27 Dec 2019 01:25:16 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3875e4f7132972e39b1f6f2567e1e72a74c20e0ac8200088fd0fc852dc0620a5`  
		Last Modified: Fri, 27 Dec 2019 01:25:16 GMT  
		Size: 497.0 KB (497039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9424e5c97107933298a9e864dab7c85c93b9baae4be24ad2cf5c1d4348829f`  
		Last Modified: Fri, 27 Dec 2019 01:25:16 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ed0b7e2bf3399fa8adf53702486277f2b7e4df20472dfe2d75cc0b4c3523f2`  
		Last Modified: Fri, 27 Dec 2019 01:25:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `composer:1.9.1`

```console
$ docker pull composer@sha256:75a6a13680d0be7074f1c52f78f508751258d002c6e3934a7d5c332739f2b201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `composer:1.9.1` - linux; amd64

```console
$ docker pull composer@sha256:fdbee4b29a1bcca79b12fdced7d9221eb6cc28832b9e00ab2e7c6726f20ca8cc
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66206861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02efded7ec8009b7a35bf247573592efffbe0f382d3c0e3dd07becb80565505`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:47:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 21:47:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 21:47:52 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 21:47:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 21:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 21:47:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:47:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:47:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 21:47:55 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 21:47:55 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 21:47:55 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 21:47:55 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 21:47:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 21:47:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:55:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 21:55:56 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:55:58 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 21:55:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 21:55:58 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 03:48:37 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 03:48:47 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 03:48:47 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 03:48:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 03:48:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 03:48:48 GMT
ENV COMPOSER_VERSION=1.9.1
# Fri, 27 Dec 2019 03:48:49 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 03:48:49 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 03:48:49 GMT
WORKDIR /app
# Fri, 27 Dec 2019 03:48:50 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 03:48:50 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7a574e8632727fe466d1871c39e4fea951243dc9f0a56bdc55cb8720f4aac6`  
		Last Modified: Thu, 26 Dec 2019 23:05:01 GMT  
		Size: 1.4 MB (1354713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6c65f587e94ae6bd946a70d456e75c7543d38cb03271622a815f3b5398ec74`  
		Last Modified: Thu, 26 Dec 2019 23:05:00 GMT  
		Size: 1.2 KB (1227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba33e4b639bb4e1187590b34ea007a27393fbda41d6f3ad10d04c9a0bd1cde4a`  
		Last Modified: Thu, 26 Dec 2019 23:05:00 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94182f10949f8b172016cbddea1d7b4417514c40d0fd664a0895d3b0f93fcbe`  
		Last Modified: Thu, 26 Dec 2019 23:05:00 GMT  
		Size: 10.3 MB (10264403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06b2b4baeabcdc2692442b4f6a6512b1f6b20697c8ec9b984503705cc81039a`  
		Last Modified: Thu, 26 Dec 2019 23:04:59 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6abb9ac3b49074e4561b65dbf3c4beaab0b50ef72743a04656dd6e664bcdecc`  
		Last Modified: Thu, 26 Dec 2019 23:05:03 GMT  
		Size: 16.2 MB (16158246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8028c0b7a7e712cf77e535c0d109ae5bce6ae34cefcd8ebf46b640214b5c91`  
		Last Modified: Thu, 26 Dec 2019 23:04:59 GMT  
		Size: 2.2 KB (2217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cc7bad024a2e7896c445c24345d1b9226c1c7ed0adbc57145db4d8ce9aea2f`  
		Last Modified: Thu, 26 Dec 2019 23:04:59 GMT  
		Size: 73.2 KB (73165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc711a535acb29705350d1595ce40c1748951322b88a6413245a4d2a5b7f645`  
		Last Modified: Fri, 27 Dec 2019 03:49:14 GMT  
		Size: 34.8 MB (34774961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5788687df725e868549f29349dd7e546295b632f970634f2b97660aa15c10c9`  
		Last Modified: Fri, 27 Dec 2019 03:49:06 GMT  
		Size: 277.5 KB (277531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91a01e20dbd8ec111d179be5a7d9f856c2018938a07f94ce1de5f111907de97`  
		Last Modified: Fri, 27 Dec 2019 03:49:06 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c853bffcbc704b657c099fa2a3cc9c10919552af9a3e0a2d8ae4a42e6782eb`  
		Last Modified: Fri, 27 Dec 2019 03:49:06 GMT  
		Size: 497.0 KB (497005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0d79794dfc6b4b090401c350caf4bfcb0c038672d8c0a28d3d822838f9dcd2`  
		Last Modified: Fri, 27 Dec 2019 03:49:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fac451fab2e34ab918bfe33533c77b938fe2bcb55ff4680a6468d524e1c69a6`  
		Last Modified: Fri, 27 Dec 2019 03:49:06 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.9.1` - linux; arm variant v6

```console
$ docker pull composer@sha256:dd97b87c2947f5c3a5a55e9e6153cf324920f5747918d25b6ec90cebdc44087e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64113537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fcb94b450243c8357d8679a6da332460fbcf60f735dc84e44f27f87554e02c6`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:20:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:20:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:20:18 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:20:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:20:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:20:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:20:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:20:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:20:24 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:20:25 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:20:26 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:20:27 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:20:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:20:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:24:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:24:26 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:24:30 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:24:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:24:35 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 01:32:05 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 01:32:22 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 01:32:24 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 01:32:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 01:32:26 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 01:32:26 GMT
ENV COMPOSER_VERSION=1.9.1
# Fri, 27 Dec 2019 01:32:29 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 01:32:29 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 01:32:33 GMT
WORKDIR /app
# Fri, 27 Dec 2019 01:32:36 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 01:32:39 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f2222aeb0ea56ad08de7753e2ed3f6c40f7093cda7436e94583ce0f0922072`  
		Last Modified: Thu, 26 Dec 2019 23:02:36 GMT  
		Size: 1.3 MB (1321130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f893e696ec7590309f1a77539ce734af052f1aa42c48aaf6f478453dcd7eafa`  
		Last Modified: Thu, 26 Dec 2019 23:02:35 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ad230ebfba33233fbafdd19ca2939dfd20dffdc83636c23f9285017935fca9`  
		Last Modified: Thu, 26 Dec 2019 23:02:35 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44905e88daf12c640968d3d790a02e11babe5d4f4730e6fcd3eae081f8df2f62`  
		Last Modified: Thu, 26 Dec 2019 23:02:34 GMT  
		Size: 10.3 MB (10264410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e91ff6ebef94b35989b1200b9d2564b71aa5e20f03fbc2c75bf57786cdca79`  
		Last Modified: Thu, 26 Dec 2019 23:02:34 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6b1bfceee6e3798ac6b36213aede482172b522e4c9d17635d9418419bd0672`  
		Last Modified: Thu, 26 Dec 2019 23:02:39 GMT  
		Size: 15.0 MB (14962846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6b063069fde53011cbbab0f1fc6cb9f8b02fb20f6f0e986394d971347f38c0`  
		Last Modified: Thu, 26 Dec 2019 23:02:34 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f29f685cf530bfbe1b0003111bed088314ef583a2585bb11a10d7463dfc5dd8`  
		Last Modified: Thu, 26 Dec 2019 23:02:34 GMT  
		Size: 72.7 KB (72680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa550c82c0fdd2e85ec9b9b51732a4590f1a279d6856aa6bd427e28a5571260`  
		Last Modified: Fri, 27 Dec 2019 01:33:31 GMT  
		Size: 34.1 MB (34107571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9770e9484fb6fd2b55324ba5ef682f2a2b1f08bb3dbcf502ca8ecf32cf0c8f`  
		Last Modified: Fri, 27 Dec 2019 01:33:16 GMT  
		Size: 270.7 KB (270675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1f90781495ee403d3826a9f593fde90d3657e5f87f2bc0d757d74c7b4435ab`  
		Last Modified: Fri, 27 Dec 2019 01:33:16 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5ee0bd8ba874c58e5a766515b76e4d85166155f92d996c24c3a26f0ebc5138`  
		Last Modified: Fri, 27 Dec 2019 01:33:16 GMT  
		Size: 497.0 KB (497035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c38f9121f497e45f2517272c56a59f4a5992b6274fb6d9685b1100f69512c2`  
		Last Modified: Fri, 27 Dec 2019 01:33:16 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36b2e72ff9d80d06d651f66bd8bd8f258ccf15e4c6c144bd710e16fae8aea73`  
		Last Modified: Fri, 27 Dec 2019 01:33:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.9.1` - linux; arm variant v7

```console
$ docker pull composer@sha256:f677de2a63ff1ae9145160a6605ea45bc413e58b4bdf8d4cb91263130c945bcf
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61388895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9012e1c5224f7b7e3ec0077971ad126503067b41b3e53da4df6c6012c3aa112`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 18:59:09 GMT
ADD file:caf7ca25875eddd2bfa2d1e56663bb52d278a85f6ee1314f9ccf01dc4da8070a in / 
# Tue, 24 Dec 2019 18:59:10 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:28:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 21:28:59 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 21:29:01 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 21:29:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 21:29:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 21:29:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:29:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:29:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 21:29:05 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 21:29:05 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 21:29:06 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 21:29:06 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 21:29:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 21:29:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:31:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 21:31:34 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:31:36 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 21:31:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 21:31:38 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 00:05:43 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 00:06:02 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 00:06:04 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 00:06:04 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 00:06:05 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 00:06:06 GMT
ENV COMPOSER_VERSION=1.9.1
# Fri, 27 Dec 2019 00:06:09 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 00:06:10 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 00:06:11 GMT
WORKDIR /app
# Fri, 27 Dec 2019 00:06:13 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 00:06:15 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:3922e475e500b2739b5e74787fc80622853325822f71f8bd3de7e5b09654d60f`  
		Last Modified: Tue, 24 Dec 2019 18:59:33 GMT  
		Size: 2.4 MB (2416691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d850653ef66a74bc2f65e933df679895db53bc6e01d23076dbc532056eec8a7`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 1.2 MB (1227347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed0b2f0bcd9c23ef1f79be9d752fea5f714457c75308002cf597d596e8b1c1a`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77de73a7de2b81d6828d80578fc934edf55e039effcf2bb8555e6a0b5864080`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69dc1b35828f88798cdf411520e8541662fa44c3e21d0b46b668e5ad1ce38f24`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 10.3 MB (10264419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1ac53e078b99a6ba0cf4e8600a0ba5aa6bd3b579e0f86d78a3b18bd692976a`  
		Last Modified: Thu, 26 Dec 2019 22:01:16 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a349634f832daa7e54f052c5c5fce54336c7089c5997981c3be8552baf32c10c`  
		Last Modified: Thu, 26 Dec 2019 22:01:21 GMT  
		Size: 14.0 MB (14035302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef07c3ed8c6baead6c71677fb97b0bef1c3762881b234e8ed7aa21c0470854ed`  
		Last Modified: Thu, 26 Dec 2019 22:01:16 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01eab0467fa0094e7e35ef8de9b09468e7ae8b53efc431442a1a9af5a5be310a`  
		Last Modified: Thu, 26 Dec 2019 22:01:16 GMT  
		Size: 72.7 KB (72675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef760acfe9c6c709e6adc3e53bb918efdfbf825221903209bd82018b119c1439`  
		Last Modified: Fri, 27 Dec 2019 00:06:57 GMT  
		Size: 32.6 MB (32605578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51aade9d91ae2843e8ec23f54eea99048fa2d73d2e01cea93889e60c54b4210`  
		Last Modified: Fri, 27 Dec 2019 00:06:44 GMT  
		Size: 264.7 KB (264673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a512d9b12df16845d0df25d19e6307acb404fcf2f3a3862d47f94e2259fb0f23`  
		Last Modified: Fri, 27 Dec 2019 00:06:44 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cde7a20d9972695c743aa2a0e922361370380dbef712fea1617d181bbe4fc`  
		Last Modified: Fri, 27 Dec 2019 00:06:44 GMT  
		Size: 497.0 KB (497037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852bb277a6ed901b13ff9be031f1aa4b6a5e313dfb998b3c6c5f10055a93e3a2`  
		Last Modified: Fri, 27 Dec 2019 00:06:44 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce34df92ca04dd2bdf3e2373fc25a8a172c772c16ad3b38cfa6f9e63eddb7e46`  
		Last Modified: Fri, 27 Dec 2019 00:06:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.9.1` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:baf042a8b58480a86b9a613750042c985cd23d66830d12ef6dbd874cd5ff2b77
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66202831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a184fefdede0cf61596a9690935c94a10a964cdbca862d66a76da536cdbbb4c4`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 20:26:15 GMT
ADD file:d6c3db0313ab0c6201770c7248d1bac964011a1c08f1a9b434442b7c21efef87 in / 
# Tue, 24 Dec 2019 20:26:24 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:08:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:08:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:08:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:08:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:08:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:08:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:08:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:08:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:08:38 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:08:39 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:08:40 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:08:40 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:08:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:08:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:12:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:12:26 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:12:30 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:12:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:12:32 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 01:00:35 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 01:01:10 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 01:01:21 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 01:01:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 01:01:34 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 01:01:38 GMT
ENV COMPOSER_VERSION=1.9.1
# Fri, 27 Dec 2019 01:01:54 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 01:01:56 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 01:02:01 GMT
WORKDIR /app
# Fri, 27 Dec 2019 01:02:03 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 01:02:05 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cde5963f3b93eec667cad527c99d80402a5a91a7a1381f7ffe562f215aec0c50`  
		Last Modified: Tue, 24 Dec 2019 20:26:52 GMT  
		Size: 2.7 MB (2719182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36763f956175b40d2a6ca97c274d362c9a0deb76d9b7eb62e95b8ca953bb1db2`  
		Last Modified: Thu, 26 Dec 2019 22:48:41 GMT  
		Size: 1.4 MB (1359427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01374ab459ad592d2c9b91efb836df933906c6cd8c63606db7f385c084fa04d2`  
		Last Modified: Thu, 26 Dec 2019 22:48:40 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34492236b9882b05dc402fe511c10ac8463554a1223a9bd10460daeab25a98f`  
		Last Modified: Thu, 26 Dec 2019 22:48:40 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b0ab5705e600f30f4341814fc44949ef8a0595246e35d6a72d4146fd467f1e`  
		Last Modified: Thu, 26 Dec 2019 22:48:38 GMT  
		Size: 10.3 MB (10264412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8fe4aab7c71980ba6c9c10d2d41202a098e48ef491850ebc67b17a147487d88`  
		Last Modified: Thu, 26 Dec 2019 22:48:38 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f253d45c879751ce17f7944d232be8fcb0e2bc700a5a6714d97a63867aff06`  
		Last Modified: Thu, 26 Dec 2019 22:48:41 GMT  
		Size: 15.9 MB (15851650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805b37c27a0499cf4df7c736ea7581d72e1cb4a6613bda953833b79a80caac1a`  
		Last Modified: Thu, 26 Dec 2019 22:48:38 GMT  
		Size: 2.2 KB (2215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7400940d887ae822a41abe503ec76c4a6e979621ecf316d123cb0d39eb34db`  
		Last Modified: Thu, 26 Dec 2019 22:48:38 GMT  
		Size: 72.7 KB (72682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1a36a335b2a481db4a07619c7e30bdced72bc39e6b6f1ee3715a6cdc603bd1`  
		Last Modified: Fri, 27 Dec 2019 01:03:09 GMT  
		Size: 35.2 MB (35157603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ea079782c565a70581045175e15f46bb937e07e2200ea63b03bf72af221b07`  
		Last Modified: Fri, 27 Dec 2019 01:02:55 GMT  
		Size: 275.7 KB (275669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae534ca14dbc48106ee3f2e81f33b327cf7eb302898c02bb4ab7345cc44b502`  
		Last Modified: Fri, 27 Dec 2019 01:02:55 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9f707e568acdc4ac64f6df65d1da26a796d239543900581845647ae7cc94df`  
		Last Modified: Fri, 27 Dec 2019 01:02:55 GMT  
		Size: 497.0 KB (497033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38530d4206c9f562e53cadc427a46c8e2adf48db5da189fae8d33fa45f587f3`  
		Last Modified: Fri, 27 Dec 2019 01:02:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d6873676bd3565875ec532df054c50b52dc9d79b2ec8f6e43f5ce27e78b2b1`  
		Last Modified: Fri, 27 Dec 2019 01:02:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.9.1` - linux; 386

```console
$ docker pull composer@sha256:eb104347bdbea942b571973f68326dce69ae3c92dfe7aa331d88298dc4d5c493
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68289013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb946c124f051f09f714c35fd6e2529d6707c10ec140737cf56e882111bcd82`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 19:38:57 GMT
ADD file:d0127a9692e8445993a88163cb741dbb23fa25436dd65289e76b08484264b397 in / 
# Tue, 24 Dec 2019 19:38:57 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:36:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:36:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:36:14 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:36:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:36:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:36:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:36:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:36:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:36:17 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:36:18 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:36:18 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:36:18 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:36:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:36:23 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:45:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:45:50 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:45:51 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:45:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:45:52 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 01:41:40 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 01:41:52 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 01:41:52 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 01:41:52 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 01:41:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 01:41:53 GMT
ENV COMPOSER_VERSION=1.9.1
# Fri, 27 Dec 2019 01:41:54 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 01:41:54 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 01:41:54 GMT
WORKDIR /app
# Fri, 27 Dec 2019 01:41:55 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 01:41:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:57bbc6f150623b3e4f01930af4ab2efa6ed5df02319341a08b1ce0bbd7e4afdf`  
		Last Modified: Tue, 24 Dec 2019 19:39:19 GMT  
		Size: 2.8 MB (2805146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db25e971d6f24055202f90f96d257a719817ad73623eaf02d98fb13c2dbe9a1b`  
		Last Modified: Fri, 27 Dec 2019 00:00:12 GMT  
		Size: 1.5 MB (1452611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ecdadbdbb91bc66f820e5b3077004286155b3e618cc444f493d7e73b400333`  
		Last Modified: Fri, 27 Dec 2019 00:00:12 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8331211b40f9489961b63904af5f93f96465efa4f5202ee08600fd1fe3caec6c`  
		Last Modified: Fri, 27 Dec 2019 00:00:11 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1feab22a6dc5f30ac5d6a419e21b0ad02df0633e9376cda5af697a214a1677e`  
		Last Modified: Fri, 27 Dec 2019 00:00:12 GMT  
		Size: 10.3 MB (10264412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f291e0ec174ac10d076b738bdd8d7b5a352fd362d9659a6cb4b7c5cf7e219323`  
		Last Modified: Fri, 27 Dec 2019 00:00:10 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeee04bc33533cf870952c9aab9489299215c7b4a6077fc85ded1a38354bfa34`  
		Last Modified: Fri, 27 Dec 2019 00:00:17 GMT  
		Size: 16.6 MB (16572401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4baee82eaeb4bb25b75b28052d7aec12a58e5f0b9cc3abdccdea6d742bda1e`  
		Last Modified: Fri, 27 Dec 2019 00:00:10 GMT  
		Size: 2.2 KB (2215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01721c87d29cd0ad25164e2a64d81439e2201e730353ea8a64a5324af5aaaa6`  
		Last Modified: Fri, 27 Dec 2019 00:00:10 GMT  
		Size: 72.3 KB (72336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3650f92aaf29753dc8d77c5521fe278f1fc1be26d84d5a01b2931c17fba38029`  
		Last Modified: Fri, 27 Dec 2019 01:42:21 GMT  
		Size: 36.3 MB (36327612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cabc1b7971f28befd3ee5c2117694eaaf4e7750fab49a6718b9de78c706ae4b`  
		Last Modified: Fri, 27 Dec 2019 01:42:11 GMT  
		Size: 292.4 KB (292421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a90dea8b1328167473598879d3d8ae5cd35c5b9d38f71e564048508f36f480`  
		Last Modified: Fri, 27 Dec 2019 01:42:11 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f18de3cac22e1e5f06fcdcdc7c32966859717887c9de60785ce0af29c1fd4ca`  
		Last Modified: Fri, 27 Dec 2019 01:42:11 GMT  
		Size: 497.0 KB (497009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392481b4d02274d120941ac388bec69fbb9ac1c1dc3e951b48156c2b1bb5def6`  
		Last Modified: Fri, 27 Dec 2019 01:42:11 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f279761684374c3e2dfc98ed41d387bae19d174837ef1e03e16e2c72696f126b`  
		Last Modified: Fri, 27 Dec 2019 01:42:11 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.9.1` - linux; ppc64le

```console
$ docker pull composer@sha256:d4d9899d9faa184331bc4a29f410d7ad97c617303ddecc1cb7512d79490ec254
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68398531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058a3b17db3adc1e4a850d3509a225280c8618a5496c9cacddb5c48ef1b37da4`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 19:28:37 GMT
ADD file:4d85451a651e236d899cd849617594eb6babf24079f9b2269134ad06d89bdecc in / 
# Tue, 24 Dec 2019 19:28:38 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:21:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:21:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:21:14 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:21:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:21:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:21:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:21:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:21:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:21:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:21:31 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:21:32 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:21:34 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:21:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:21:52 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:26:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:26:57 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:27:14 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:27:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:27:22 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 01:23:47 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 01:24:07 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 01:24:11 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 01:24:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 01:24:15 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 01:24:17 GMT
ENV COMPOSER_VERSION=1.9.1
# Fri, 27 Dec 2019 01:24:22 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 01:24:24 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 01:24:25 GMT
WORKDIR /app
# Fri, 27 Dec 2019 01:24:27 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 01:24:29 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a5dee701e1e87430161d8fce67e77ee5e132bdbafe165c52490a36df654c7660`  
		Last Modified: Tue, 24 Dec 2019 19:29:09 GMT  
		Size: 2.8 MB (2816482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5787caafdab36524ef14f193793a44b3b5f54da82c98e8152770c2868fd93b11`  
		Last Modified: Thu, 26 Dec 2019 23:13:04 GMT  
		Size: 1.4 MB (1397977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691639ddfd73c88dfeda1734ababccfaed311f9d747bf07d41c6e7fed2880baf`  
		Last Modified: Thu, 26 Dec 2019 23:13:03 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2a706347c576336f1e0145755e4fa707710b3f42dc7d18903fcee51bb72842`  
		Last Modified: Thu, 26 Dec 2019 23:13:02 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c9367473ae473e3b4307b84581a68ce338708fd02c58387ea03ebbf3b336c4`  
		Last Modified: Thu, 26 Dec 2019 23:13:00 GMT  
		Size: 10.3 MB (10264430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce400ab5b594b3c37b04d8ff93ef76324ad103b89b864086646553aa374ae3a`  
		Last Modified: Thu, 26 Dec 2019 23:12:59 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df72cd13deac5a2de7a62833b97945cc48eb13a954c074f0c2ef27d321ad172`  
		Last Modified: Thu, 26 Dec 2019 23:13:09 GMT  
		Size: 17.1 MB (17073151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a993ff611f4ce5c9ad8c688b7d218dfaf24788380583d0b8ff19758b953565b`  
		Last Modified: Thu, 26 Dec 2019 23:12:59 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b2a23101f41428ee2ad1948c90b3eaf9cda596853a790ebdb59a2e5f3a4353`  
		Last Modified: Thu, 26 Dec 2019 23:12:59 GMT  
		Size: 73.0 KB (73011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c481dd45fa62f76d142285ca14edc35411b4ea549c65fa328636265afec673`  
		Last Modified: Fri, 27 Dec 2019 01:25:27 GMT  
		Size: 36.0 MB (35979323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5e3a68f6ae205b4e6572bf9337334694abcf7dfe1e953aeda6fe3d3953efaf`  
		Last Modified: Fri, 27 Dec 2019 01:25:16 GMT  
		Size: 291.9 KB (291945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cceb98b5eab7c70364129cb95652d435f2c30fa63e2235def0ca4fbd5c83fb8`  
		Last Modified: Fri, 27 Dec 2019 01:25:16 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3875e4f7132972e39b1f6f2567e1e72a74c20e0ac8200088fd0fc852dc0620a5`  
		Last Modified: Fri, 27 Dec 2019 01:25:16 GMT  
		Size: 497.0 KB (497039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9424e5c97107933298a9e864dab7c85c93b9baae4be24ad2cf5c1d4348829f`  
		Last Modified: Fri, 27 Dec 2019 01:25:16 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ed0b7e2bf3399fa8adf53702486277f2b7e4df20472dfe2d75cc0b4c3523f2`  
		Last Modified: Fri, 27 Dec 2019 01:25:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `composer:latest`

```console
$ docker pull composer@sha256:75a6a13680d0be7074f1c52f78f508751258d002c6e3934a7d5c332739f2b201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `composer:latest` - linux; amd64

```console
$ docker pull composer@sha256:fdbee4b29a1bcca79b12fdced7d9221eb6cc28832b9e00ab2e7c6726f20ca8cc
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66206861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02efded7ec8009b7a35bf247573592efffbe0f382d3c0e3dd07becb80565505`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:47:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 21:47:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 21:47:52 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 21:47:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 21:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 21:47:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:47:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:47:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 21:47:55 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 21:47:55 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 21:47:55 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 21:47:55 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 21:47:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 21:47:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:55:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 21:55:56 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:55:58 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 21:55:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 21:55:58 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 03:48:37 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 03:48:47 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 03:48:47 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 03:48:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 03:48:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 03:48:48 GMT
ENV COMPOSER_VERSION=1.9.1
# Fri, 27 Dec 2019 03:48:49 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 03:48:49 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 03:48:49 GMT
WORKDIR /app
# Fri, 27 Dec 2019 03:48:50 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 03:48:50 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7a574e8632727fe466d1871c39e4fea951243dc9f0a56bdc55cb8720f4aac6`  
		Last Modified: Thu, 26 Dec 2019 23:05:01 GMT  
		Size: 1.4 MB (1354713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6c65f587e94ae6bd946a70d456e75c7543d38cb03271622a815f3b5398ec74`  
		Last Modified: Thu, 26 Dec 2019 23:05:00 GMT  
		Size: 1.2 KB (1227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba33e4b639bb4e1187590b34ea007a27393fbda41d6f3ad10d04c9a0bd1cde4a`  
		Last Modified: Thu, 26 Dec 2019 23:05:00 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94182f10949f8b172016cbddea1d7b4417514c40d0fd664a0895d3b0f93fcbe`  
		Last Modified: Thu, 26 Dec 2019 23:05:00 GMT  
		Size: 10.3 MB (10264403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06b2b4baeabcdc2692442b4f6a6512b1f6b20697c8ec9b984503705cc81039a`  
		Last Modified: Thu, 26 Dec 2019 23:04:59 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6abb9ac3b49074e4561b65dbf3c4beaab0b50ef72743a04656dd6e664bcdecc`  
		Last Modified: Thu, 26 Dec 2019 23:05:03 GMT  
		Size: 16.2 MB (16158246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8028c0b7a7e712cf77e535c0d109ae5bce6ae34cefcd8ebf46b640214b5c91`  
		Last Modified: Thu, 26 Dec 2019 23:04:59 GMT  
		Size: 2.2 KB (2217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cc7bad024a2e7896c445c24345d1b9226c1c7ed0adbc57145db4d8ce9aea2f`  
		Last Modified: Thu, 26 Dec 2019 23:04:59 GMT  
		Size: 73.2 KB (73165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc711a535acb29705350d1595ce40c1748951322b88a6413245a4d2a5b7f645`  
		Last Modified: Fri, 27 Dec 2019 03:49:14 GMT  
		Size: 34.8 MB (34774961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5788687df725e868549f29349dd7e546295b632f970634f2b97660aa15c10c9`  
		Last Modified: Fri, 27 Dec 2019 03:49:06 GMT  
		Size: 277.5 KB (277531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91a01e20dbd8ec111d179be5a7d9f856c2018938a07f94ce1de5f111907de97`  
		Last Modified: Fri, 27 Dec 2019 03:49:06 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c853bffcbc704b657c099fa2a3cc9c10919552af9a3e0a2d8ae4a42e6782eb`  
		Last Modified: Fri, 27 Dec 2019 03:49:06 GMT  
		Size: 497.0 KB (497005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0d79794dfc6b4b090401c350caf4bfcb0c038672d8c0a28d3d822838f9dcd2`  
		Last Modified: Fri, 27 Dec 2019 03:49:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fac451fab2e34ab918bfe33533c77b938fe2bcb55ff4680a6468d524e1c69a6`  
		Last Modified: Fri, 27 Dec 2019 03:49:06 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:dd97b87c2947f5c3a5a55e9e6153cf324920f5747918d25b6ec90cebdc44087e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64113537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fcb94b450243c8357d8679a6da332460fbcf60f735dc84e44f27f87554e02c6`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:20:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:20:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:20:18 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:20:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:20:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:20:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:20:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:20:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:20:24 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:20:25 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:20:26 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:20:27 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:20:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:20:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:24:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:24:26 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:24:30 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:24:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:24:35 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 01:32:05 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 01:32:22 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 01:32:24 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 01:32:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 01:32:26 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 01:32:26 GMT
ENV COMPOSER_VERSION=1.9.1
# Fri, 27 Dec 2019 01:32:29 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 01:32:29 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 01:32:33 GMT
WORKDIR /app
# Fri, 27 Dec 2019 01:32:36 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 01:32:39 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f2222aeb0ea56ad08de7753e2ed3f6c40f7093cda7436e94583ce0f0922072`  
		Last Modified: Thu, 26 Dec 2019 23:02:36 GMT  
		Size: 1.3 MB (1321130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f893e696ec7590309f1a77539ce734af052f1aa42c48aaf6f478453dcd7eafa`  
		Last Modified: Thu, 26 Dec 2019 23:02:35 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ad230ebfba33233fbafdd19ca2939dfd20dffdc83636c23f9285017935fca9`  
		Last Modified: Thu, 26 Dec 2019 23:02:35 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44905e88daf12c640968d3d790a02e11babe5d4f4730e6fcd3eae081f8df2f62`  
		Last Modified: Thu, 26 Dec 2019 23:02:34 GMT  
		Size: 10.3 MB (10264410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e91ff6ebef94b35989b1200b9d2564b71aa5e20f03fbc2c75bf57786cdca79`  
		Last Modified: Thu, 26 Dec 2019 23:02:34 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6b1bfceee6e3798ac6b36213aede482172b522e4c9d17635d9418419bd0672`  
		Last Modified: Thu, 26 Dec 2019 23:02:39 GMT  
		Size: 15.0 MB (14962846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6b063069fde53011cbbab0f1fc6cb9f8b02fb20f6f0e986394d971347f38c0`  
		Last Modified: Thu, 26 Dec 2019 23:02:34 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f29f685cf530bfbe1b0003111bed088314ef583a2585bb11a10d7463dfc5dd8`  
		Last Modified: Thu, 26 Dec 2019 23:02:34 GMT  
		Size: 72.7 KB (72680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa550c82c0fdd2e85ec9b9b51732a4590f1a279d6856aa6bd427e28a5571260`  
		Last Modified: Fri, 27 Dec 2019 01:33:31 GMT  
		Size: 34.1 MB (34107571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9770e9484fb6fd2b55324ba5ef682f2a2b1f08bb3dbcf502ca8ecf32cf0c8f`  
		Last Modified: Fri, 27 Dec 2019 01:33:16 GMT  
		Size: 270.7 KB (270675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1f90781495ee403d3826a9f593fde90d3657e5f87f2bc0d757d74c7b4435ab`  
		Last Modified: Fri, 27 Dec 2019 01:33:16 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5ee0bd8ba874c58e5a766515b76e4d85166155f92d996c24c3a26f0ebc5138`  
		Last Modified: Fri, 27 Dec 2019 01:33:16 GMT  
		Size: 497.0 KB (497035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c38f9121f497e45f2517272c56a59f4a5992b6274fb6d9685b1100f69512c2`  
		Last Modified: Fri, 27 Dec 2019 01:33:16 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36b2e72ff9d80d06d651f66bd8bd8f258ccf15e4c6c144bd710e16fae8aea73`  
		Last Modified: Fri, 27 Dec 2019 01:33:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:f677de2a63ff1ae9145160a6605ea45bc413e58b4bdf8d4cb91263130c945bcf
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61388895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9012e1c5224f7b7e3ec0077971ad126503067b41b3e53da4df6c6012c3aa112`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 18:59:09 GMT
ADD file:caf7ca25875eddd2bfa2d1e56663bb52d278a85f6ee1314f9ccf01dc4da8070a in / 
# Tue, 24 Dec 2019 18:59:10 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:28:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 21:28:59 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 21:29:01 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 21:29:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 21:29:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 21:29:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:29:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 21:29:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 21:29:05 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 21:29:05 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 21:29:06 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 21:29:06 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 21:29:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 21:29:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:31:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 21:31:34 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:31:36 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 21:31:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 21:31:38 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 00:05:43 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 00:06:02 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 00:06:04 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 00:06:04 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 00:06:05 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 00:06:06 GMT
ENV COMPOSER_VERSION=1.9.1
# Fri, 27 Dec 2019 00:06:09 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 00:06:10 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 00:06:11 GMT
WORKDIR /app
# Fri, 27 Dec 2019 00:06:13 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 00:06:15 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:3922e475e500b2739b5e74787fc80622853325822f71f8bd3de7e5b09654d60f`  
		Last Modified: Tue, 24 Dec 2019 18:59:33 GMT  
		Size: 2.4 MB (2416691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d850653ef66a74bc2f65e933df679895db53bc6e01d23076dbc532056eec8a7`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 1.2 MB (1227347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed0b2f0bcd9c23ef1f79be9d752fea5f714457c75308002cf597d596e8b1c1a`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77de73a7de2b81d6828d80578fc934edf55e039effcf2bb8555e6a0b5864080`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69dc1b35828f88798cdf411520e8541662fa44c3e21d0b46b668e5ad1ce38f24`  
		Last Modified: Thu, 26 Dec 2019 22:01:17 GMT  
		Size: 10.3 MB (10264419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1ac53e078b99a6ba0cf4e8600a0ba5aa6bd3b579e0f86d78a3b18bd692976a`  
		Last Modified: Thu, 26 Dec 2019 22:01:16 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a349634f832daa7e54f052c5c5fce54336c7089c5997981c3be8552baf32c10c`  
		Last Modified: Thu, 26 Dec 2019 22:01:21 GMT  
		Size: 14.0 MB (14035302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef07c3ed8c6baead6c71677fb97b0bef1c3762881b234e8ed7aa21c0470854ed`  
		Last Modified: Thu, 26 Dec 2019 22:01:16 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01eab0467fa0094e7e35ef8de9b09468e7ae8b53efc431442a1a9af5a5be310a`  
		Last Modified: Thu, 26 Dec 2019 22:01:16 GMT  
		Size: 72.7 KB (72675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef760acfe9c6c709e6adc3e53bb918efdfbf825221903209bd82018b119c1439`  
		Last Modified: Fri, 27 Dec 2019 00:06:57 GMT  
		Size: 32.6 MB (32605578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51aade9d91ae2843e8ec23f54eea99048fa2d73d2e01cea93889e60c54b4210`  
		Last Modified: Fri, 27 Dec 2019 00:06:44 GMT  
		Size: 264.7 KB (264673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a512d9b12df16845d0df25d19e6307acb404fcf2f3a3862d47f94e2259fb0f23`  
		Last Modified: Fri, 27 Dec 2019 00:06:44 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cde7a20d9972695c743aa2a0e922361370380dbef712fea1617d181bbe4fc`  
		Last Modified: Fri, 27 Dec 2019 00:06:44 GMT  
		Size: 497.0 KB (497037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852bb277a6ed901b13ff9be031f1aa4b6a5e313dfb998b3c6c5f10055a93e3a2`  
		Last Modified: Fri, 27 Dec 2019 00:06:44 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce34df92ca04dd2bdf3e2373fc25a8a172c772c16ad3b38cfa6f9e63eddb7e46`  
		Last Modified: Fri, 27 Dec 2019 00:06:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:baf042a8b58480a86b9a613750042c985cd23d66830d12ef6dbd874cd5ff2b77
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66202831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a184fefdede0cf61596a9690935c94a10a964cdbca862d66a76da536cdbbb4c4`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 20:26:15 GMT
ADD file:d6c3db0313ab0c6201770c7248d1bac964011a1c08f1a9b434442b7c21efef87 in / 
# Tue, 24 Dec 2019 20:26:24 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:08:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:08:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:08:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:08:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:08:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:08:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:08:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:08:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:08:38 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:08:39 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:08:40 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:08:40 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:08:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:08:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:12:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:12:26 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:12:30 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:12:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:12:32 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 01:00:35 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 01:01:10 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 01:01:21 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 01:01:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 01:01:34 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 01:01:38 GMT
ENV COMPOSER_VERSION=1.9.1
# Fri, 27 Dec 2019 01:01:54 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 01:01:56 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 01:02:01 GMT
WORKDIR /app
# Fri, 27 Dec 2019 01:02:03 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 01:02:05 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cde5963f3b93eec667cad527c99d80402a5a91a7a1381f7ffe562f215aec0c50`  
		Last Modified: Tue, 24 Dec 2019 20:26:52 GMT  
		Size: 2.7 MB (2719182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36763f956175b40d2a6ca97c274d362c9a0deb76d9b7eb62e95b8ca953bb1db2`  
		Last Modified: Thu, 26 Dec 2019 22:48:41 GMT  
		Size: 1.4 MB (1359427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01374ab459ad592d2c9b91efb836df933906c6cd8c63606db7f385c084fa04d2`  
		Last Modified: Thu, 26 Dec 2019 22:48:40 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34492236b9882b05dc402fe511c10ac8463554a1223a9bd10460daeab25a98f`  
		Last Modified: Thu, 26 Dec 2019 22:48:40 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b0ab5705e600f30f4341814fc44949ef8a0595246e35d6a72d4146fd467f1e`  
		Last Modified: Thu, 26 Dec 2019 22:48:38 GMT  
		Size: 10.3 MB (10264412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8fe4aab7c71980ba6c9c10d2d41202a098e48ef491850ebc67b17a147487d88`  
		Last Modified: Thu, 26 Dec 2019 22:48:38 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f253d45c879751ce17f7944d232be8fcb0e2bc700a5a6714d97a63867aff06`  
		Last Modified: Thu, 26 Dec 2019 22:48:41 GMT  
		Size: 15.9 MB (15851650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805b37c27a0499cf4df7c736ea7581d72e1cb4a6613bda953833b79a80caac1a`  
		Last Modified: Thu, 26 Dec 2019 22:48:38 GMT  
		Size: 2.2 KB (2215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7400940d887ae822a41abe503ec76c4a6e979621ecf316d123cb0d39eb34db`  
		Last Modified: Thu, 26 Dec 2019 22:48:38 GMT  
		Size: 72.7 KB (72682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1a36a335b2a481db4a07619c7e30bdced72bc39e6b6f1ee3715a6cdc603bd1`  
		Last Modified: Fri, 27 Dec 2019 01:03:09 GMT  
		Size: 35.2 MB (35157603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ea079782c565a70581045175e15f46bb937e07e2200ea63b03bf72af221b07`  
		Last Modified: Fri, 27 Dec 2019 01:02:55 GMT  
		Size: 275.7 KB (275669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae534ca14dbc48106ee3f2e81f33b327cf7eb302898c02bb4ab7345cc44b502`  
		Last Modified: Fri, 27 Dec 2019 01:02:55 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9f707e568acdc4ac64f6df65d1da26a796d239543900581845647ae7cc94df`  
		Last Modified: Fri, 27 Dec 2019 01:02:55 GMT  
		Size: 497.0 KB (497033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38530d4206c9f562e53cadc427a46c8e2adf48db5da189fae8d33fa45f587f3`  
		Last Modified: Fri, 27 Dec 2019 01:02:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d6873676bd3565875ec532df054c50b52dc9d79b2ec8f6e43f5ce27e78b2b1`  
		Last Modified: Fri, 27 Dec 2019 01:02:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; 386

```console
$ docker pull composer@sha256:eb104347bdbea942b571973f68326dce69ae3c92dfe7aa331d88298dc4d5c493
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68289013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb946c124f051f09f714c35fd6e2529d6707c10ec140737cf56e882111bcd82`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 19:38:57 GMT
ADD file:d0127a9692e8445993a88163cb741dbb23fa25436dd65289e76b08484264b397 in / 
# Tue, 24 Dec 2019 19:38:57 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:36:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:36:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:36:14 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:36:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:36:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:36:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:36:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:36:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:36:17 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:36:18 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:36:18 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:36:18 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:36:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:36:23 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:45:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:45:50 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:45:51 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:45:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:45:52 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 01:41:40 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 01:41:52 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 01:41:52 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 01:41:52 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 01:41:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 01:41:53 GMT
ENV COMPOSER_VERSION=1.9.1
# Fri, 27 Dec 2019 01:41:54 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 01:41:54 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 01:41:54 GMT
WORKDIR /app
# Fri, 27 Dec 2019 01:41:55 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 01:41:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:57bbc6f150623b3e4f01930af4ab2efa6ed5df02319341a08b1ce0bbd7e4afdf`  
		Last Modified: Tue, 24 Dec 2019 19:39:19 GMT  
		Size: 2.8 MB (2805146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db25e971d6f24055202f90f96d257a719817ad73623eaf02d98fb13c2dbe9a1b`  
		Last Modified: Fri, 27 Dec 2019 00:00:12 GMT  
		Size: 1.5 MB (1452611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ecdadbdbb91bc66f820e5b3077004286155b3e618cc444f493d7e73b400333`  
		Last Modified: Fri, 27 Dec 2019 00:00:12 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8331211b40f9489961b63904af5f93f96465efa4f5202ee08600fd1fe3caec6c`  
		Last Modified: Fri, 27 Dec 2019 00:00:11 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1feab22a6dc5f30ac5d6a419e21b0ad02df0633e9376cda5af697a214a1677e`  
		Last Modified: Fri, 27 Dec 2019 00:00:12 GMT  
		Size: 10.3 MB (10264412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f291e0ec174ac10d076b738bdd8d7b5a352fd362d9659a6cb4b7c5cf7e219323`  
		Last Modified: Fri, 27 Dec 2019 00:00:10 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeee04bc33533cf870952c9aab9489299215c7b4a6077fc85ded1a38354bfa34`  
		Last Modified: Fri, 27 Dec 2019 00:00:17 GMT  
		Size: 16.6 MB (16572401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4baee82eaeb4bb25b75b28052d7aec12a58e5f0b9cc3abdccdea6d742bda1e`  
		Last Modified: Fri, 27 Dec 2019 00:00:10 GMT  
		Size: 2.2 KB (2215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01721c87d29cd0ad25164e2a64d81439e2201e730353ea8a64a5324af5aaaa6`  
		Last Modified: Fri, 27 Dec 2019 00:00:10 GMT  
		Size: 72.3 KB (72336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3650f92aaf29753dc8d77c5521fe278f1fc1be26d84d5a01b2931c17fba38029`  
		Last Modified: Fri, 27 Dec 2019 01:42:21 GMT  
		Size: 36.3 MB (36327612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cabc1b7971f28befd3ee5c2117694eaaf4e7750fab49a6718b9de78c706ae4b`  
		Last Modified: Fri, 27 Dec 2019 01:42:11 GMT  
		Size: 292.4 KB (292421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a90dea8b1328167473598879d3d8ae5cd35c5b9d38f71e564048508f36f480`  
		Last Modified: Fri, 27 Dec 2019 01:42:11 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f18de3cac22e1e5f06fcdcdc7c32966859717887c9de60785ce0af29c1fd4ca`  
		Last Modified: Fri, 27 Dec 2019 01:42:11 GMT  
		Size: 497.0 KB (497009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392481b4d02274d120941ac388bec69fbb9ac1c1dc3e951b48156c2b1bb5def6`  
		Last Modified: Fri, 27 Dec 2019 01:42:11 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f279761684374c3e2dfc98ed41d387bae19d174837ef1e03e16e2c72696f126b`  
		Last Modified: Fri, 27 Dec 2019 01:42:11 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; ppc64le

```console
$ docker pull composer@sha256:d4d9899d9faa184331bc4a29f410d7ad97c617303ddecc1cb7512d79490ec254
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68398531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058a3b17db3adc1e4a850d3509a225280c8618a5496c9cacddb5c48ef1b37da4`
-	Entrypoint: `["\/bin\/sh","\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 24 Dec 2019 19:28:37 GMT
ADD file:4d85451a651e236d899cd849617594eb6babf24079f9b2269134ad06d89bdecc in / 
# Tue, 24 Dec 2019 19:28:38 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 22:21:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Dec 2019 22:21:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 26 Dec 2019 22:21:14 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 26 Dec 2019 22:21:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Dec 2019 22:21:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 26 Dec 2019 22:21:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:21:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Dec 2019 22:21:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 26 Dec 2019 22:21:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 26 Dec 2019 22:21:31 GMT
ENV PHP_VERSION=7.4.1
# Thu, 26 Dec 2019 22:21:32 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.1.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.1.tar.xz.asc/from/this/mirror
# Thu, 26 Dec 2019 22:21:34 GMT
ENV PHP_SHA256=561bb866bdd509094be00f4ece7c3543ec971c4d878645ee81437e291cffc762 PHP_MD5=
# Thu, 26 Dec 2019 22:21:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Dec 2019 22:21:52 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:26:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 26 Dec 2019 22:26:57 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 26 Dec 2019 22:27:14 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Dec 2019 22:27:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Dec 2019 22:27:22 GMT
CMD ["php" "-a"]
# Fri, 27 Dec 2019 01:23:47 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Dec 2019 01:24:07 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 27 Dec 2019 01:24:11 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Dec 2019 01:24:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Dec 2019 01:24:15 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Dec 2019 01:24:17 GMT
ENV COMPOSER_VERSION=1.9.1
# Fri, 27 Dec 2019 01:24:22 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Dec 2019 01:24:24 GMT
COPY file:098af1c9d6ed00c2f357827391da1b2b0978915db35f033349301c7cbe78010d in /docker-entrypoint.sh 
# Fri, 27 Dec 2019 01:24:25 GMT
WORKDIR /app
# Fri, 27 Dec 2019 01:24:27 GMT
ENTRYPOINT ["/bin/sh" "/docker-entrypoint.sh"]
# Fri, 27 Dec 2019 01:24:29 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a5dee701e1e87430161d8fce67e77ee5e132bdbafe165c52490a36df654c7660`  
		Last Modified: Tue, 24 Dec 2019 19:29:09 GMT  
		Size: 2.8 MB (2816482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5787caafdab36524ef14f193793a44b3b5f54da82c98e8152770c2868fd93b11`  
		Last Modified: Thu, 26 Dec 2019 23:13:04 GMT  
		Size: 1.4 MB (1397977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691639ddfd73c88dfeda1734ababccfaed311f9d747bf07d41c6e7fed2880baf`  
		Last Modified: Thu, 26 Dec 2019 23:13:03 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2a706347c576336f1e0145755e4fa707710b3f42dc7d18903fcee51bb72842`  
		Last Modified: Thu, 26 Dec 2019 23:13:02 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c9367473ae473e3b4307b84581a68ce338708fd02c58387ea03ebbf3b336c4`  
		Last Modified: Thu, 26 Dec 2019 23:13:00 GMT  
		Size: 10.3 MB (10264430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce400ab5b594b3c37b04d8ff93ef76324ad103b89b864086646553aa374ae3a`  
		Last Modified: Thu, 26 Dec 2019 23:12:59 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df72cd13deac5a2de7a62833b97945cc48eb13a954c074f0c2ef27d321ad172`  
		Last Modified: Thu, 26 Dec 2019 23:13:09 GMT  
		Size: 17.1 MB (17073151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a993ff611f4ce5c9ad8c688b7d218dfaf24788380583d0b8ff19758b953565b`  
		Last Modified: Thu, 26 Dec 2019 23:12:59 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b2a23101f41428ee2ad1948c90b3eaf9cda596853a790ebdb59a2e5f3a4353`  
		Last Modified: Thu, 26 Dec 2019 23:12:59 GMT  
		Size: 73.0 KB (73011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c481dd45fa62f76d142285ca14edc35411b4ea549c65fa328636265afec673`  
		Last Modified: Fri, 27 Dec 2019 01:25:27 GMT  
		Size: 36.0 MB (35979323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5e3a68f6ae205b4e6572bf9337334694abcf7dfe1e953aeda6fe3d3953efaf`  
		Last Modified: Fri, 27 Dec 2019 01:25:16 GMT  
		Size: 291.9 KB (291945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cceb98b5eab7c70364129cb95652d435f2c30fa63e2235def0ca4fbd5c83fb8`  
		Last Modified: Fri, 27 Dec 2019 01:25:16 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3875e4f7132972e39b1f6f2567e1e72a74c20e0ac8200088fd0fc852dc0620a5`  
		Last Modified: Fri, 27 Dec 2019 01:25:16 GMT  
		Size: 497.0 KB (497039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9424e5c97107933298a9e864dab7c85c93b9baae4be24ad2cf5c1d4348829f`  
		Last Modified: Fri, 27 Dec 2019 01:25:16 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ed0b7e2bf3399fa8adf53702486277f2b7e4df20472dfe2d75cc0b4c3523f2`  
		Last Modified: Fri, 27 Dec 2019 01:25:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
