<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `composer`

-	[`composer:1`](#composer1)
-	[`composer:1.10`](#composer110)
-	[`composer:1.10.20`](#composer11020)
-	[`composer:2`](#composer2)
-	[`composer:2.0`](#composer20)
-	[`composer:2.0.9`](#composer209)
-	[`composer:latest`](#composerlatest)

## `composer:1`

```console
$ docker pull composer@sha256:69f3e58d91b15f1abe7bf2506597f3909e7b53f33d21d18c1707599904d5b733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `composer:1` - linux; amd64

```console
$ docker pull composer@sha256:15041e5826ffbd609ed496774f5ef19128b1f5c6536a1294365813464f88d814
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62373497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de5740a8abd6c9f77e5008075537110c2545c4b35864292757f2f49ad03b529`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 02:23:51 GMT
ADD file:edbe213ae0c825a5bfbe569928cf20f683f334f93a093ccd0a3a014b7428e760 in / 
# Fri, 15 Jan 2021 02:23:51 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:43:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:43:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:43:26 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:43:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:43:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:43:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:43:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:43:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:43:30 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:43:30 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:43:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:43:31 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:43:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:43:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:51:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 20:17:47 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 20:17:50 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 20:17:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 20:17:51 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:32:03 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:32:24 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:32:24 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:32:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:32:25 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:32:34 GMT
ENV COMPOSER_VERSION=1.10.20
# Thu, 28 Jan 2021 22:32:36 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:32:36 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:32:36 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:32:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:32:37 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:596ba82af5aaa3e2fd9d6f955b8b94f0744a2b60710e3c243ba3e4a467f051d1`  
		Last Modified: Fri, 15 Jan 2021 02:08:10 GMT  
		Size: 2.8 MB (2810825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af74f285bb27c6623f2b5c8c3a2e487603c7dd5c51859fd6e13859542f4310c3`  
		Last Modified: Sat, 16 Jan 2021 01:00:24 GMT  
		Size: 1.7 MB (1694838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab8440e5667ccb2ffd4e62ed905a106742dfdd7dd3167d9d64b4bdeed8a4945`  
		Last Modified: Sat, 16 Jan 2021 01:00:20 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64889fa545ec919e6fe392c368b8cb41a10e7834c1ba4d4d96fd9ee2e3405cc1`  
		Last Modified: Sat, 16 Jan 2021 01:00:20 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94168e6487351b04d28db6aabb22e0c68ad3582533cf8d7e00322078720f8081`  
		Last Modified: Sat, 16 Jan 2021 01:00:19 GMT  
		Size: 10.7 MB (10661716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3898f14298ef25ab2005e9025a88f553003a83a1b6a61765e93d78879441aa36`  
		Last Modified: Sat, 16 Jan 2021 01:00:18 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3747e5f21671eba796a4b76a6abc180c60b0ef9414e9a80b325b31aeaa1f6ca`  
		Last Modified: Sat, 16 Jan 2021 01:00:21 GMT  
		Size: 15.3 MB (15318011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3df0f8088890764041d8dbfe574cd5bdf020400801b0b108cd6b7f965aab3a`  
		Last Modified: Thu, 21 Jan 2021 20:28:34 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f6ddeaf0bdcf495df2e7c8d72852796c1bae3d9f8ef8260058fdb43b995163`  
		Last Modified: Thu, 21 Jan 2021 20:28:34 GMT  
		Size: 17.5 KB (17539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29338fcaf9eb090ba02397a08616210ac758731039ac2d2a5db97288090a1845`  
		Last Modified: Thu, 28 Jan 2021 22:32:55 GMT  
		Size: 31.2 MB (31158400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a0bf379d52ae6a08ffd2313828e5738aa1cfd2a934c2403e6065ae7f94ba05`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 198.3 KB (198274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a346beb5e7dfc07424d1d661858912a89fab48a63bd89492e0c97c3cf1a6c75`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8191633d27c6e6161ac5ccc3f5112e823af18e5cc62bdfe4146589d7c44aebf1`  
		Last Modified: Thu, 28 Jan 2021 22:33:02 GMT  
		Size: 508.9 KB (508927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eac7632c4a851dce2efef3f2aa6da2e0d0571a278890a683388059992f89483`  
		Last Modified: Thu, 28 Jan 2021 22:33:02 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256c9cc11c9c202b76652699f47cb4c1ae4bfb8c76b50287be53de24ec90b653`  
		Last Modified: Thu, 28 Jan 2021 22:33:02 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1` - linux; arm variant v6

```console
$ docker pull composer@sha256:681a45213e37b7024fd1986c8f4cac581a37f1bd3b5afac7146b96450347a7a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58221747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a4cabcfab9fbba95857b0c4844c30aed503a82b49272d278d8f0231b2ce2a4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 28 Jan 2021 23:49:59 GMT
ADD file:c197324e4979e2a7b257ad683d20dd9cbdae525a076bd68fe6aa0e0b126875df in / 
# Thu, 28 Jan 2021 23:49:59 GMT
CMD ["/bin/sh"]
# Fri, 29 Jan 2021 00:33:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 29 Jan 2021 00:33:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 29 Jan 2021 00:33:59 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 29 Jan 2021 00:34:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 29 Jan 2021 00:34:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 29 Jan 2021 00:34:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 29 Jan 2021 00:34:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 29 Jan 2021 00:34:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 29 Jan 2021 00:34:08 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 29 Jan 2021 00:34:11 GMT
ENV PHP_VERSION=8.0.1
# Fri, 29 Jan 2021 00:34:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 29 Jan 2021 00:34:13 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 29 Jan 2021 00:34:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 29 Jan 2021 00:34:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 29 Jan 2021 00:37:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 29 Jan 2021 00:37:35 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 29 Jan 2021 00:37:38 GMT
RUN docker-php-ext-enable sodium
# Fri, 29 Jan 2021 00:37:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 29 Jan 2021 00:37:40 GMT
CMD ["php" "-a"]
# Fri, 29 Jan 2021 02:11:29 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 29 Jan 2021 02:11:49 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 29 Jan 2021 02:11:51 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 29 Jan 2021 02:11:51 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 29 Jan 2021 02:11:52 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 29 Jan 2021 02:12:09 GMT
ENV COMPOSER_VERSION=1.10.20
# Fri, 29 Jan 2021 02:12:12 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 29 Jan 2021 02:12:12 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 29 Jan 2021 02:12:13 GMT
WORKDIR /app
# Fri, 29 Jan 2021 02:12:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 29 Jan 2021 02:12:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a66f440da051140fefcb0a520bdeb69d763b1eb4fd1b2ed46b4c0a168e335108`  
		Last Modified: Thu, 28 Jan 2021 23:50:33 GMT  
		Size: 2.6 MB (2621759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa34846effbef1e901021c65a67535efc29a1aa39b259a4c29559d1439f4131`  
		Last Modified: Fri, 29 Jan 2021 01:05:52 GMT  
		Size: 1.7 MB (1684855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba088c5e0e1fb4c64a8b59354bedcae82636c10a93fe3790125bec5c1e841299`  
		Last Modified: Fri, 29 Jan 2021 01:05:51 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b10584422ada7d37ac091eae04bcee5df4cee5b93cd86068ce55c7ab085ae62`  
		Last Modified: Fri, 29 Jan 2021 01:05:51 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd2125b643842a0b1fb7799c57d504cb3ea72f1cdaac6d48b6d3ee2fa033d39`  
		Last Modified: Fri, 29 Jan 2021 01:05:50 GMT  
		Size: 10.7 MB (10661723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370c8d7d436fffa9dd306db82b4a90f7b25ae1d68c658dac4c195ec6a921976e`  
		Last Modified: Fri, 29 Jan 2021 01:05:49 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c1bd9522799773adb723d78cef494168d851dd759ef42bdf230e3518c9888d`  
		Last Modified: Fri, 29 Jan 2021 01:05:54 GMT  
		Size: 13.6 MB (13571709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60b70fa5215a21be024094dd917f70d206590186d21137fcb75d1fb68a887a2`  
		Last Modified: Fri, 29 Jan 2021 01:05:49 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733b25bcaba65cbff9b151c9ab65d005350d890d7728bfe14024f5f4bd9ca890`  
		Last Modified: Fri, 29 Jan 2021 01:05:49 GMT  
		Size: 17.5 KB (17531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dda7886eea28b54dfe2eea50537d02027bbbcda31bb0d081dff700b99290584`  
		Last Modified: Fri, 29 Jan 2021 02:12:41 GMT  
		Size: 29.0 MB (28956651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90907b51293338df699b9f07cbb70441610fa8f2924e32d21967026449fe4064`  
		Last Modified: Fri, 29 Jan 2021 02:12:28 GMT  
		Size: 193.5 KB (193490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85552216f6bbc21bc776e9622f10a51b96b9a92310894072d91339b4fe625b1e`  
		Last Modified: Fri, 29 Jan 2021 02:12:28 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826269360f1b18acb29abbbca07ffda1fb53dc87ea68b0b9044157f2aea8dcd7`  
		Last Modified: Fri, 29 Jan 2021 02:12:51 GMT  
		Size: 508.9 KB (508950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1040cda38a25cfabe23a4f3025d4fd9430498b5da7860c6fc370d0e8a675288b`  
		Last Modified: Fri, 29 Jan 2021 02:12:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b870d06eca9355beb7c18b2bc89e44760735adfe9c4dbb3b36b6edeee5f761cd`  
		Last Modified: Fri, 29 Jan 2021 02:12:51 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1` - linux; arm variant v7

```console
$ docker pull composer@sha256:8c924eed02fb1a3b071e3741eac381bcd2f6e461e6c16dea19d46a35336df585
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56063307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37defddda0760cf3372f74c959e1335a4fc24f5f353a9b3b920abfe647d2c36`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:58:27 GMT
ADD file:718d7c24a8d6ff0feb2843cf8c3ca4b7ef1fb523a45dea568404259a7b4e6f10 in / 
# Fri, 15 Jan 2021 01:58:29 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:04:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:04:05 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:04:07 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:04:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:04:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:04:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:04:13 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:04:14 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:04:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:04:15 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:04:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:04:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:07:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:10:13 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:10:16 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:10:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:10:18 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 21:57:49 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 21:58:13 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 21:58:15 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 21:58:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 21:58:17 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 21:58:36 GMT
ENV COMPOSER_VERSION=1.10.20
# Thu, 28 Jan 2021 21:58:39 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 21:58:40 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 21:58:40 GMT
WORKDIR /app
# Thu, 28 Jan 2021 21:58:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 21:58:42 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:0f34ce5da94097b8c334f6b2065a010aced9855c3532e4462e9bd1b0a4c4b3f6`  
		Last Modified: Fri, 15 Jan 2021 01:59:13 GMT  
		Size: 2.4 MB (2422744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cecec77a7b5b50913bcb9f7bfe0c5fdcebb948b947747285290197c13902be91`  
		Last Modified: Fri, 15 Jan 2021 23:42:36 GMT  
		Size: 1.6 MB (1555130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0496082b3c55009a50b47ce80bf27dd7451aaa7e13b5b4ccbe886a780c614dd1`  
		Last Modified: Fri, 15 Jan 2021 23:42:33 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af351861d88fff830659b71d51e45b8e623d31cb86c764fab107e6c39ca5a717`  
		Last Modified: Fri, 15 Jan 2021 23:42:33 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11aa9107e62f7893b45936388317768641833b4f6b1937989fcbfc5845e1c698`  
		Last Modified: Fri, 15 Jan 2021 23:42:32 GMT  
		Size: 10.7 MB (10661711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739d880e478996d44b501dcc056bf9f5f25909c929d579ba0c02f123be170522`  
		Last Modified: Fri, 15 Jan 2021 23:42:30 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed2a0f0dbdad0b49284a158baa86126c2b2a794ee53b82c4181378520555f1d`  
		Last Modified: Fri, 15 Jan 2021 23:42:36 GMT  
		Size: 13.1 MB (13070133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b9ed4df09ec14031c338ad506ba7fcc76ab6a07fc32432ad75d94867ae04d9`  
		Last Modified: Thu, 21 Jan 2021 19:23:58 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500dd1602efbacb91e481ac3e868dadb7bca74fb6b4f73d41fb2ec82cab72f22`  
		Last Modified: Thu, 21 Jan 2021 19:23:59 GMT  
		Size: 17.5 KB (17536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b52f140a609f714bafc66c167ec2b6c04c8962153f406e1ac18bac7b669c61`  
		Last Modified: Thu, 28 Jan 2021 21:59:15 GMT  
		Size: 27.6 MB (27635729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cb9e5e751c90392752772de98a302d52a12f4ea2dcf08223098a5cb41c1fd4`  
		Last Modified: Thu, 28 Jan 2021 21:58:57 GMT  
		Size: 186.3 KB (186294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964a5881822f5f5e182f7b8d8fef32582177380aff1c392f68c3c5f908be31d4`  
		Last Modified: Thu, 28 Jan 2021 21:58:57 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f372f4a1d57fcda1ba2142f3ead85e6bbf97c49e1aeb89bb65e355ab41bfea6e`  
		Last Modified: Thu, 28 Jan 2021 21:59:27 GMT  
		Size: 509.0 KB (508954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52252a296f2b0f0d04e335396310b8ce47f5313114ac535d44c3233623e2e112`  
		Last Modified: Thu, 28 Jan 2021 21:59:27 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ca700269cc2d3c3588c2afe11cec218a2afc3fd62460983326434a940d8394`  
		Last Modified: Thu, 28 Jan 2021 21:59:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:f0c754ec0e20b19ed5482233110351043b98ca186e677e46c0784e6390973eb3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61935669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd59253a35bffa6894e23823e2d163cc891258a2175959f10445847410c63aa5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:47:51 GMT
ADD file:95be2cec37537b3fd70aeb1d4eb3479fc4a56b00ad7180788ddd7fa772ca65e7 in / 
# Fri, 15 Jan 2021 01:47:52 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:04:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:04:28 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:04:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:04:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:04:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:04:39 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:04:40 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:04:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:04:41 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:04:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:04:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:09:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:51:20 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:51:27 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:51:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:51:31 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:39:49 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:40:10 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:40:12 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:40:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:40:14 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:40:35 GMT
ENV COMPOSER_VERSION=1.10.20
# Thu, 28 Jan 2021 22:40:38 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:40:39 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:40:40 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:40:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:40:41 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:30d5333d20a68dd6ea3689e2c5692d7071f2d68e72c06f0b3b4c7e213df454e2`  
		Last Modified: Fri, 15 Jan 2021 01:48:29 GMT  
		Size: 2.7 MB (2710904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72077bc47778707d4c51904bf6932e44a09d9a5a37f1bac45ef59fe94bc54e1`  
		Last Modified: Fri, 15 Jan 2021 23:49:43 GMT  
		Size: 1.7 MB (1694577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bfc628cf72db6285835ff062834a15ee7c9067f6b7ccb55fad0a8bb0f292be`  
		Last Modified: Fri, 15 Jan 2021 23:49:41 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ab015e378a2ad2e4c345884006fc6b1678a0ebba44214fbc5e9dcb48ef7bb2`  
		Last Modified: Fri, 15 Jan 2021 23:49:41 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d24a448de09dec3ceb6bc305d0c17be120e79f5611f1e4054850e11526133cc8`  
		Last Modified: Fri, 15 Jan 2021 23:49:39 GMT  
		Size: 10.7 MB (10661733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8079f19e688581d52496f1937db9dc33ef25e597b149eb517633043678bd61d2`  
		Last Modified: Fri, 15 Jan 2021 23:49:39 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978c3da5ab542fa26ea4333b9b5c608d2ee68fa98cbf1e0d05df83ece9439e24`  
		Last Modified: Fri, 15 Jan 2021 23:49:45 GMT  
		Size: 14.8 MB (14764647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1043bb484cdf4818387523cb0c703d862e1c50b54ebe62f605c0d3b74837f39`  
		Last Modified: Thu, 21 Jan 2021 20:05:13 GMT  
		Size: 2.3 KB (2269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c953f678545439a3b425e1dd037e3e5d5b8092e37adb1a63cb110a0a888b5300`  
		Last Modified: Thu, 21 Jan 2021 20:05:12 GMT  
		Size: 17.6 KB (17550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f77742777349432a5c810bb823719115d594ef2d7e0d79d11fdccf49b1c298`  
		Last Modified: Thu, 28 Jan 2021 22:41:08 GMT  
		Size: 31.4 MB (31376168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20f98fa3077571418cb9ac1f3ceb60436f9c6bcda79d861d68e9c48787403d1`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 196.1 KB (196059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899d29da6e7af774384acf87f4eea2a9876f6bff3365b1486ecb6738a8e95143`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c98b0e6011753de7f48370ec14b7d6df3edd44bea6c654333efab43d29ecf1`  
		Last Modified: Thu, 28 Jan 2021 22:41:25 GMT  
		Size: 509.0 KB (508952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58045ba48e2988e029a9204473be18429006cfff4e1415ee55c04fad8e97cc2`  
		Last Modified: Thu, 28 Jan 2021 22:41:24 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5366c00175f04b24edf1440c7b0ac425e885f97839ee2b42533db92c19f0df`  
		Last Modified: Thu, 28 Jan 2021 22:41:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1` - linux; 386

```console
$ docker pull composer@sha256:522d1c17cfd4585f4db74672c4594ba0c2e10eaa887194fb74aafcc5639d55e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63658787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd03c16d8b1151c76d26e7c44166aae340dcc1257ba9cee77733961c3484b8f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:38:28 GMT
ADD file:d8723c02f1eb0efa4dadc6480a753d18d7e28d9815bff96a92ff09ff55a92b11 in / 
# Fri, 15 Jan 2021 01:38:29 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 22:42:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 22:42:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 22:42:23 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 22:42:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 22:42:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 22:42:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:42:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:42:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 22:42:24 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 22:42:25 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 22:42:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 22:42:25 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 22:42:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 22:42:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 22:49:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:44:48 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:44:51 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:44:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:44:51 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:38:41 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:38:56 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:38:57 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:38:57 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:38:57 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:39:09 GMT
ENV COMPOSER_VERSION=1.10.20
# Thu, 28 Jan 2021 22:39:10 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:39:11 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:39:12 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:39:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9e6a151110e36daa7a487250f98425289313f856e3a586d89d82bafc1bf322c3`  
		Last Modified: Fri, 15 Jan 2021 01:39:01 GMT  
		Size: 2.8 MB (2817152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b194694eae0c8525a66d3c56796eb37a9e263d63f03eaecf6bc83d2ab3f7c9`  
		Last Modified: Fri, 15 Jan 2021 23:50:55 GMT  
		Size: 1.8 MB (1793505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a9a95dec7f2cd3bcf6903d006a870fa7113f6a974d30ec6634ab82b0a0a792`  
		Last Modified: Fri, 15 Jan 2021 23:50:52 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ad687f5cfc54121cc70af5ff69cb844177c4325a2c14efcd144cb096ecfba2`  
		Last Modified: Fri, 15 Jan 2021 23:50:54 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ae4debbbbc31db383a639e6a7df85ebf9c2f15905a9ec2df4fb8a3998dec90`  
		Last Modified: Fri, 15 Jan 2021 23:50:56 GMT  
		Size: 10.7 MB (10661677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900efcbd73b95b91ec42e946efd16fa2e312e57beba40e9aac2b0699baa90d1d`  
		Last Modified: Fri, 15 Jan 2021 23:50:51 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c042850cc5dcebe86c931da9e6014fe607a6c507fe5a61059ba47003a80cac2`  
		Last Modified: Fri, 15 Jan 2021 23:51:00 GMT  
		Size: 15.3 MB (15348857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a592432a0a1e356653687e23dd3c8f953d0fc904db0377fa898de0c851be229d`  
		Last Modified: Thu, 21 Jan 2021 19:55:39 GMT  
		Size: 2.3 KB (2270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3b6898b8d491988e64358ef661f654c98cbec8cc3e36edeedea25334aae60e`  
		Last Modified: Thu, 21 Jan 2021 19:55:40 GMT  
		Size: 17.5 KB (17525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fcd335e71480482247bfd7863baa60db887184f8227377b99d22f61dc2a4d6`  
		Last Modified: Thu, 28 Jan 2021 22:39:38 GMT  
		Size: 32.3 MB (32292342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f574926dca5384453b345a61350707cbf2753926b84e8c685a1899bbe6ff5b`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 213.8 KB (213825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25022b6f8e9b3bd588f8db12caab7e929709dcb604f7f84786e3a7d54f6bd2f4`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a994c0ddb1f52a20e600cc2a3f65e7cc10c05053931d749c3003447c373c174e`  
		Last Modified: Thu, 28 Jan 2021 22:39:45 GMT  
		Size: 508.9 KB (508932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a8e706fc35dce4c888ff6a5600c1c4ca890bd470226f86c55f5b870f5716ba`  
		Last Modified: Thu, 28 Jan 2021 22:39:44 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33b7e4e5c37989586a88b9a4437f5db1926f1291aa88ea8692239638804cd9b`  
		Last Modified: Thu, 28 Jan 2021 22:39:44 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1` - linux; ppc64le

```console
$ docker pull composer@sha256:64ec310b74e056c1a829af51d012910446deda6483099ab4fd21431b7c649ebe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (64004945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe32bddbb4094f3cd642c80e9f8dfe9e9fef99cd6cdcfeae23438ad7f483659`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 02:41:43 GMT
ADD file:137e8f98476d5dceaeb2e8359f50eb818dee4c327e4492d16e87fb27d40aa891 in / 
# Fri, 15 Jan 2021 02:41:46 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:17:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:17:44 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:17:56 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:18:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:18:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:18:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:18:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:18:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:18:39 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:18:43 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:18:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:19:07 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:19:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:19:38 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:24:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:33:15 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:33:36 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:33:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:33:47 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:26:03 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:27:01 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:27:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:27:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:27:24 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:28:39 GMT
ENV COMPOSER_VERSION=1.10.20
# Thu, 28 Jan 2021 22:29:02 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:29:09 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:29:17 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:29:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:29:44 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cb0f06c26ffdc2117b9a3467f79e69cdf8d9c677a3c0bacabc8a694a9fe303a8`  
		Last Modified: Fri, 15 Jan 2021 02:42:19 GMT  
		Size: 2.8 MB (2812389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9a7aad5bd113c5dca33b681663b0c58f66e510017e693801a6688a9c4bab60`  
		Last Modified: Sat, 16 Jan 2021 00:14:01 GMT  
		Size: 1.7 MB (1741834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ce1d80ff72759b98cf2f5ad1efa6dd181e5f4343bb0e25cbb4ec9d5d3847f4`  
		Last Modified: Sat, 16 Jan 2021 00:14:01 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48055526d8202af50f6248db9b3cb8938cab9cfec15a1312b4c1e3782f3307c4`  
		Last Modified: Sat, 16 Jan 2021 00:14:02 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7cb5ec22b0cc763855f0481247394a6e312f8f906d232f738fc88a4219bfb1e`  
		Last Modified: Sat, 16 Jan 2021 00:13:58 GMT  
		Size: 10.7 MB (10661716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea93ae862f86d372e01dcb82dbf509e78b3f4e6533f9660f4b63c49471cb4852`  
		Last Modified: Sat, 16 Jan 2021 00:13:57 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7518496c61b651e86a2bdd79ee76e400addfddbafa26db36f7e692520aeebc1e`  
		Last Modified: Sat, 16 Jan 2021 00:14:01 GMT  
		Size: 16.1 MB (16059509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dce1a5a13b51550c7b84a60d64d364686f108d412e4776aae7d7a4922ac1ebd`  
		Last Modified: Thu, 21 Jan 2021 20:03:07 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98df2e2e9c3e105f7ddf5634cc2558ef8a2e569cd7e61121bd1f18c83a96152d`  
		Last Modified: Thu, 21 Jan 2021 20:03:07 GMT  
		Size: 17.5 KB (17538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c3ac64e0e6d2c9f92c30e69ce18c62c2ff9ba34f99a48d00be9b92ccfcf393`  
		Last Modified: Thu, 28 Jan 2021 22:30:18 GMT  
		Size: 32.0 MB (31993881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fb84ebef4906eea3269f759da0902a8097011fb84006aabbd679b5950e0970`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 204.0 KB (204039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8dba6ae992e0605a8d35408b1a00afba44b82e2b40e0fde68e8181c954ff546`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07b7d2523e9bfca30dadee73bb72e48be92fa7ed7446ca26c4c5b6d88513f05`  
		Last Modified: Thu, 28 Jan 2021 22:30:35 GMT  
		Size: 509.0 KB (508958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496694a46b536e391969cc3377192c2d8b5199bb9abb26353c1480f80974425e`  
		Last Modified: Thu, 28 Jan 2021 22:30:35 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c1b4574bc541314a3ac8a8820e41e03672eeb834c9adb4a173c6ffaa7f15c5`  
		Last Modified: Thu, 28 Jan 2021 22:30:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1` - linux; s390x

```console
$ docker pull composer@sha256:efb0271bdbdb3b0ed80df63d0ce30144363aff051fc6b1c6b4906535e3ec114b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61503008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3b4d800099b7a2589dff69a16ce36042ebdbb9f8aa76310d0167fcd872e1b7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:51:34 GMT
ADD file:3ba807ca8ed73ca14224dd26a883f2399031fa32430f035cc5ae97b5e6db0ca7 in / 
# Fri, 15 Jan 2021 01:51:35 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 22:57:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 22:57:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 22:57:13 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 22:57:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 22:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 22:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:57:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:57:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 22:57:17 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 22:57:17 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 22:57:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 22:57:18 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 22:57:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 22:57:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:02:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:54:10 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:54:13 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:54:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:54:14 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:42:35 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:42:53 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:42:54 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:42:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:42:54 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:43:05 GMT
ENV COMPOSER_VERSION=1.10.20
# Thu, 28 Jan 2021 22:43:07 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:43:07 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:43:07 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:43:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:43:08 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:3997176601fb5d5ac06922718668ede4acac00a5c0daef8a9099fd76ce93047f`  
		Last Modified: Fri, 15 Jan 2021 01:52:40 GMT  
		Size: 2.6 MB (2601720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497e79d9095f9ba4812f1150c33ad07d399f559fea8e3c4fe8553e02f2cf8b6a`  
		Last Modified: Fri, 15 Jan 2021 23:39:10 GMT  
		Size: 1.8 MB (1756352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99527660904ffc5aed1d27bb86166f189e04b5df76d7becf74efffb1836eaf5e`  
		Last Modified: Fri, 15 Jan 2021 23:39:10 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9b51111e1ef5a5156e505d6369bb2d4e21354a1203636fca6f26de34df9c15`  
		Last Modified: Fri, 15 Jan 2021 23:39:10 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3c721a3fef9acf0bac166c45ff18e2485752ef7b86447284b7b710646d40df`  
		Last Modified: Fri, 15 Jan 2021 23:38:47 GMT  
		Size: 10.7 MB (10661723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e676c2ca01980f72daf35a53dae36e4fe10945de76af81d54618066f5204c598`  
		Last Modified: Fri, 15 Jan 2021 23:38:48 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90c350aff0df72bb91eaa20306afe2218ac1d50242eb213d4e481f65b2a9f60`  
		Last Modified: Fri, 15 Jan 2021 23:38:48 GMT  
		Size: 14.4 MB (14364644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c91dec7c10d367e01e4907cb6c2d00b3e5b7390545c8c9499eaac3c35986507`  
		Last Modified: Thu, 21 Jan 2021 20:05:24 GMT  
		Size: 2.3 KB (2269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63e510378e653ab6ff71c58fc15e869877848171131d614af01c250d7a36e31`  
		Last Modified: Thu, 21 Jan 2021 20:05:20 GMT  
		Size: 17.5 KB (17541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4079b673c2155f6fc765bd4b8d683a2326dd552affe882edccb45c657534ed18`  
		Last Modified: Thu, 28 Jan 2021 22:43:28 GMT  
		Size: 31.4 MB (31389182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdeafc632059b12ff488232684da09d9c34de98941c5f6ff69c471274af7602`  
		Last Modified: Thu, 28 Jan 2021 22:43:22 GMT  
		Size: 197.8 KB (197815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f475e4a4966b8ce4d7561e4c7a2e4961201d5b118193c3525421174abaaa14e5`  
		Last Modified: Thu, 28 Jan 2021 22:43:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01db2c98c35df2890d6f5c065108d858de37de4b58a8af30d6830c024634d31`  
		Last Modified: Thu, 28 Jan 2021 22:43:38 GMT  
		Size: 509.0 KB (508952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807d3d6110e2b559a85eaf8fe97082ffeabdb11b432aafad723ba63a79f58746`  
		Last Modified: Thu, 28 Jan 2021 22:43:37 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd86330f0fa7ed84623e7652846606dff7efb38d5a5079076613ec22a547429f`  
		Last Modified: Thu, 28 Jan 2021 22:43:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `composer:1.10`

```console
$ docker pull composer@sha256:69f3e58d91b15f1abe7bf2506597f3909e7b53f33d21d18c1707599904d5b733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `composer:1.10` - linux; amd64

```console
$ docker pull composer@sha256:15041e5826ffbd609ed496774f5ef19128b1f5c6536a1294365813464f88d814
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62373497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de5740a8abd6c9f77e5008075537110c2545c4b35864292757f2f49ad03b529`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 02:23:51 GMT
ADD file:edbe213ae0c825a5bfbe569928cf20f683f334f93a093ccd0a3a014b7428e760 in / 
# Fri, 15 Jan 2021 02:23:51 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:43:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:43:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:43:26 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:43:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:43:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:43:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:43:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:43:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:43:30 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:43:30 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:43:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:43:31 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:43:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:43:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:51:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 20:17:47 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 20:17:50 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 20:17:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 20:17:51 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:32:03 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:32:24 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:32:24 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:32:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:32:25 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:32:34 GMT
ENV COMPOSER_VERSION=1.10.20
# Thu, 28 Jan 2021 22:32:36 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:32:36 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:32:36 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:32:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:32:37 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:596ba82af5aaa3e2fd9d6f955b8b94f0744a2b60710e3c243ba3e4a467f051d1`  
		Last Modified: Fri, 15 Jan 2021 02:08:10 GMT  
		Size: 2.8 MB (2810825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af74f285bb27c6623f2b5c8c3a2e487603c7dd5c51859fd6e13859542f4310c3`  
		Last Modified: Sat, 16 Jan 2021 01:00:24 GMT  
		Size: 1.7 MB (1694838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab8440e5667ccb2ffd4e62ed905a106742dfdd7dd3167d9d64b4bdeed8a4945`  
		Last Modified: Sat, 16 Jan 2021 01:00:20 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64889fa545ec919e6fe392c368b8cb41a10e7834c1ba4d4d96fd9ee2e3405cc1`  
		Last Modified: Sat, 16 Jan 2021 01:00:20 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94168e6487351b04d28db6aabb22e0c68ad3582533cf8d7e00322078720f8081`  
		Last Modified: Sat, 16 Jan 2021 01:00:19 GMT  
		Size: 10.7 MB (10661716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3898f14298ef25ab2005e9025a88f553003a83a1b6a61765e93d78879441aa36`  
		Last Modified: Sat, 16 Jan 2021 01:00:18 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3747e5f21671eba796a4b76a6abc180c60b0ef9414e9a80b325b31aeaa1f6ca`  
		Last Modified: Sat, 16 Jan 2021 01:00:21 GMT  
		Size: 15.3 MB (15318011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3df0f8088890764041d8dbfe574cd5bdf020400801b0b108cd6b7f965aab3a`  
		Last Modified: Thu, 21 Jan 2021 20:28:34 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f6ddeaf0bdcf495df2e7c8d72852796c1bae3d9f8ef8260058fdb43b995163`  
		Last Modified: Thu, 21 Jan 2021 20:28:34 GMT  
		Size: 17.5 KB (17539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29338fcaf9eb090ba02397a08616210ac758731039ac2d2a5db97288090a1845`  
		Last Modified: Thu, 28 Jan 2021 22:32:55 GMT  
		Size: 31.2 MB (31158400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a0bf379d52ae6a08ffd2313828e5738aa1cfd2a934c2403e6065ae7f94ba05`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 198.3 KB (198274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a346beb5e7dfc07424d1d661858912a89fab48a63bd89492e0c97c3cf1a6c75`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8191633d27c6e6161ac5ccc3f5112e823af18e5cc62bdfe4146589d7c44aebf1`  
		Last Modified: Thu, 28 Jan 2021 22:33:02 GMT  
		Size: 508.9 KB (508927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eac7632c4a851dce2efef3f2aa6da2e0d0571a278890a683388059992f89483`  
		Last Modified: Thu, 28 Jan 2021 22:33:02 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256c9cc11c9c202b76652699f47cb4c1ae4bfb8c76b50287be53de24ec90b653`  
		Last Modified: Thu, 28 Jan 2021 22:33:02 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.10` - linux; arm variant v6

```console
$ docker pull composer@sha256:681a45213e37b7024fd1986c8f4cac581a37f1bd3b5afac7146b96450347a7a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58221747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a4cabcfab9fbba95857b0c4844c30aed503a82b49272d278d8f0231b2ce2a4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 28 Jan 2021 23:49:59 GMT
ADD file:c197324e4979e2a7b257ad683d20dd9cbdae525a076bd68fe6aa0e0b126875df in / 
# Thu, 28 Jan 2021 23:49:59 GMT
CMD ["/bin/sh"]
# Fri, 29 Jan 2021 00:33:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 29 Jan 2021 00:33:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 29 Jan 2021 00:33:59 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 29 Jan 2021 00:34:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 29 Jan 2021 00:34:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 29 Jan 2021 00:34:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 29 Jan 2021 00:34:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 29 Jan 2021 00:34:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 29 Jan 2021 00:34:08 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 29 Jan 2021 00:34:11 GMT
ENV PHP_VERSION=8.0.1
# Fri, 29 Jan 2021 00:34:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 29 Jan 2021 00:34:13 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 29 Jan 2021 00:34:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 29 Jan 2021 00:34:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 29 Jan 2021 00:37:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 29 Jan 2021 00:37:35 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 29 Jan 2021 00:37:38 GMT
RUN docker-php-ext-enable sodium
# Fri, 29 Jan 2021 00:37:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 29 Jan 2021 00:37:40 GMT
CMD ["php" "-a"]
# Fri, 29 Jan 2021 02:11:29 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 29 Jan 2021 02:11:49 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 29 Jan 2021 02:11:51 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 29 Jan 2021 02:11:51 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 29 Jan 2021 02:11:52 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 29 Jan 2021 02:12:09 GMT
ENV COMPOSER_VERSION=1.10.20
# Fri, 29 Jan 2021 02:12:12 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 29 Jan 2021 02:12:12 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 29 Jan 2021 02:12:13 GMT
WORKDIR /app
# Fri, 29 Jan 2021 02:12:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 29 Jan 2021 02:12:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a66f440da051140fefcb0a520bdeb69d763b1eb4fd1b2ed46b4c0a168e335108`  
		Last Modified: Thu, 28 Jan 2021 23:50:33 GMT  
		Size: 2.6 MB (2621759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa34846effbef1e901021c65a67535efc29a1aa39b259a4c29559d1439f4131`  
		Last Modified: Fri, 29 Jan 2021 01:05:52 GMT  
		Size: 1.7 MB (1684855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba088c5e0e1fb4c64a8b59354bedcae82636c10a93fe3790125bec5c1e841299`  
		Last Modified: Fri, 29 Jan 2021 01:05:51 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b10584422ada7d37ac091eae04bcee5df4cee5b93cd86068ce55c7ab085ae62`  
		Last Modified: Fri, 29 Jan 2021 01:05:51 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd2125b643842a0b1fb7799c57d504cb3ea72f1cdaac6d48b6d3ee2fa033d39`  
		Last Modified: Fri, 29 Jan 2021 01:05:50 GMT  
		Size: 10.7 MB (10661723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370c8d7d436fffa9dd306db82b4a90f7b25ae1d68c658dac4c195ec6a921976e`  
		Last Modified: Fri, 29 Jan 2021 01:05:49 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c1bd9522799773adb723d78cef494168d851dd759ef42bdf230e3518c9888d`  
		Last Modified: Fri, 29 Jan 2021 01:05:54 GMT  
		Size: 13.6 MB (13571709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60b70fa5215a21be024094dd917f70d206590186d21137fcb75d1fb68a887a2`  
		Last Modified: Fri, 29 Jan 2021 01:05:49 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733b25bcaba65cbff9b151c9ab65d005350d890d7728bfe14024f5f4bd9ca890`  
		Last Modified: Fri, 29 Jan 2021 01:05:49 GMT  
		Size: 17.5 KB (17531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dda7886eea28b54dfe2eea50537d02027bbbcda31bb0d081dff700b99290584`  
		Last Modified: Fri, 29 Jan 2021 02:12:41 GMT  
		Size: 29.0 MB (28956651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90907b51293338df699b9f07cbb70441610fa8f2924e32d21967026449fe4064`  
		Last Modified: Fri, 29 Jan 2021 02:12:28 GMT  
		Size: 193.5 KB (193490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85552216f6bbc21bc776e9622f10a51b96b9a92310894072d91339b4fe625b1e`  
		Last Modified: Fri, 29 Jan 2021 02:12:28 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826269360f1b18acb29abbbca07ffda1fb53dc87ea68b0b9044157f2aea8dcd7`  
		Last Modified: Fri, 29 Jan 2021 02:12:51 GMT  
		Size: 508.9 KB (508950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1040cda38a25cfabe23a4f3025d4fd9430498b5da7860c6fc370d0e8a675288b`  
		Last Modified: Fri, 29 Jan 2021 02:12:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b870d06eca9355beb7c18b2bc89e44760735adfe9c4dbb3b36b6edeee5f761cd`  
		Last Modified: Fri, 29 Jan 2021 02:12:51 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.10` - linux; arm variant v7

```console
$ docker pull composer@sha256:8c924eed02fb1a3b071e3741eac381bcd2f6e461e6c16dea19d46a35336df585
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56063307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37defddda0760cf3372f74c959e1335a4fc24f5f353a9b3b920abfe647d2c36`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:58:27 GMT
ADD file:718d7c24a8d6ff0feb2843cf8c3ca4b7ef1fb523a45dea568404259a7b4e6f10 in / 
# Fri, 15 Jan 2021 01:58:29 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:04:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:04:05 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:04:07 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:04:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:04:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:04:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:04:13 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:04:14 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:04:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:04:15 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:04:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:04:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:07:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:10:13 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:10:16 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:10:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:10:18 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 21:57:49 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 21:58:13 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 21:58:15 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 21:58:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 21:58:17 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 21:58:36 GMT
ENV COMPOSER_VERSION=1.10.20
# Thu, 28 Jan 2021 21:58:39 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 21:58:40 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 21:58:40 GMT
WORKDIR /app
# Thu, 28 Jan 2021 21:58:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 21:58:42 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:0f34ce5da94097b8c334f6b2065a010aced9855c3532e4462e9bd1b0a4c4b3f6`  
		Last Modified: Fri, 15 Jan 2021 01:59:13 GMT  
		Size: 2.4 MB (2422744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cecec77a7b5b50913bcb9f7bfe0c5fdcebb948b947747285290197c13902be91`  
		Last Modified: Fri, 15 Jan 2021 23:42:36 GMT  
		Size: 1.6 MB (1555130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0496082b3c55009a50b47ce80bf27dd7451aaa7e13b5b4ccbe886a780c614dd1`  
		Last Modified: Fri, 15 Jan 2021 23:42:33 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af351861d88fff830659b71d51e45b8e623d31cb86c764fab107e6c39ca5a717`  
		Last Modified: Fri, 15 Jan 2021 23:42:33 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11aa9107e62f7893b45936388317768641833b4f6b1937989fcbfc5845e1c698`  
		Last Modified: Fri, 15 Jan 2021 23:42:32 GMT  
		Size: 10.7 MB (10661711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739d880e478996d44b501dcc056bf9f5f25909c929d579ba0c02f123be170522`  
		Last Modified: Fri, 15 Jan 2021 23:42:30 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed2a0f0dbdad0b49284a158baa86126c2b2a794ee53b82c4181378520555f1d`  
		Last Modified: Fri, 15 Jan 2021 23:42:36 GMT  
		Size: 13.1 MB (13070133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b9ed4df09ec14031c338ad506ba7fcc76ab6a07fc32432ad75d94867ae04d9`  
		Last Modified: Thu, 21 Jan 2021 19:23:58 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500dd1602efbacb91e481ac3e868dadb7bca74fb6b4f73d41fb2ec82cab72f22`  
		Last Modified: Thu, 21 Jan 2021 19:23:59 GMT  
		Size: 17.5 KB (17536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b52f140a609f714bafc66c167ec2b6c04c8962153f406e1ac18bac7b669c61`  
		Last Modified: Thu, 28 Jan 2021 21:59:15 GMT  
		Size: 27.6 MB (27635729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cb9e5e751c90392752772de98a302d52a12f4ea2dcf08223098a5cb41c1fd4`  
		Last Modified: Thu, 28 Jan 2021 21:58:57 GMT  
		Size: 186.3 KB (186294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964a5881822f5f5e182f7b8d8fef32582177380aff1c392f68c3c5f908be31d4`  
		Last Modified: Thu, 28 Jan 2021 21:58:57 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f372f4a1d57fcda1ba2142f3ead85e6bbf97c49e1aeb89bb65e355ab41bfea6e`  
		Last Modified: Thu, 28 Jan 2021 21:59:27 GMT  
		Size: 509.0 KB (508954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52252a296f2b0f0d04e335396310b8ce47f5313114ac535d44c3233623e2e112`  
		Last Modified: Thu, 28 Jan 2021 21:59:27 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ca700269cc2d3c3588c2afe11cec218a2afc3fd62460983326434a940d8394`  
		Last Modified: Thu, 28 Jan 2021 21:59:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.10` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:f0c754ec0e20b19ed5482233110351043b98ca186e677e46c0784e6390973eb3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61935669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd59253a35bffa6894e23823e2d163cc891258a2175959f10445847410c63aa5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:47:51 GMT
ADD file:95be2cec37537b3fd70aeb1d4eb3479fc4a56b00ad7180788ddd7fa772ca65e7 in / 
# Fri, 15 Jan 2021 01:47:52 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:04:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:04:28 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:04:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:04:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:04:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:04:39 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:04:40 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:04:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:04:41 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:04:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:04:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:09:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:51:20 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:51:27 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:51:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:51:31 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:39:49 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:40:10 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:40:12 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:40:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:40:14 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:40:35 GMT
ENV COMPOSER_VERSION=1.10.20
# Thu, 28 Jan 2021 22:40:38 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:40:39 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:40:40 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:40:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:40:41 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:30d5333d20a68dd6ea3689e2c5692d7071f2d68e72c06f0b3b4c7e213df454e2`  
		Last Modified: Fri, 15 Jan 2021 01:48:29 GMT  
		Size: 2.7 MB (2710904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72077bc47778707d4c51904bf6932e44a09d9a5a37f1bac45ef59fe94bc54e1`  
		Last Modified: Fri, 15 Jan 2021 23:49:43 GMT  
		Size: 1.7 MB (1694577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bfc628cf72db6285835ff062834a15ee7c9067f6b7ccb55fad0a8bb0f292be`  
		Last Modified: Fri, 15 Jan 2021 23:49:41 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ab015e378a2ad2e4c345884006fc6b1678a0ebba44214fbc5e9dcb48ef7bb2`  
		Last Modified: Fri, 15 Jan 2021 23:49:41 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d24a448de09dec3ceb6bc305d0c17be120e79f5611f1e4054850e11526133cc8`  
		Last Modified: Fri, 15 Jan 2021 23:49:39 GMT  
		Size: 10.7 MB (10661733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8079f19e688581d52496f1937db9dc33ef25e597b149eb517633043678bd61d2`  
		Last Modified: Fri, 15 Jan 2021 23:49:39 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978c3da5ab542fa26ea4333b9b5c608d2ee68fa98cbf1e0d05df83ece9439e24`  
		Last Modified: Fri, 15 Jan 2021 23:49:45 GMT  
		Size: 14.8 MB (14764647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1043bb484cdf4818387523cb0c703d862e1c50b54ebe62f605c0d3b74837f39`  
		Last Modified: Thu, 21 Jan 2021 20:05:13 GMT  
		Size: 2.3 KB (2269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c953f678545439a3b425e1dd037e3e5d5b8092e37adb1a63cb110a0a888b5300`  
		Last Modified: Thu, 21 Jan 2021 20:05:12 GMT  
		Size: 17.6 KB (17550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f77742777349432a5c810bb823719115d594ef2d7e0d79d11fdccf49b1c298`  
		Last Modified: Thu, 28 Jan 2021 22:41:08 GMT  
		Size: 31.4 MB (31376168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20f98fa3077571418cb9ac1f3ceb60436f9c6bcda79d861d68e9c48787403d1`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 196.1 KB (196059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899d29da6e7af774384acf87f4eea2a9876f6bff3365b1486ecb6738a8e95143`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c98b0e6011753de7f48370ec14b7d6df3edd44bea6c654333efab43d29ecf1`  
		Last Modified: Thu, 28 Jan 2021 22:41:25 GMT  
		Size: 509.0 KB (508952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58045ba48e2988e029a9204473be18429006cfff4e1415ee55c04fad8e97cc2`  
		Last Modified: Thu, 28 Jan 2021 22:41:24 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5366c00175f04b24edf1440c7b0ac425e885f97839ee2b42533db92c19f0df`  
		Last Modified: Thu, 28 Jan 2021 22:41:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.10` - linux; 386

```console
$ docker pull composer@sha256:522d1c17cfd4585f4db74672c4594ba0c2e10eaa887194fb74aafcc5639d55e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63658787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd03c16d8b1151c76d26e7c44166aae340dcc1257ba9cee77733961c3484b8f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:38:28 GMT
ADD file:d8723c02f1eb0efa4dadc6480a753d18d7e28d9815bff96a92ff09ff55a92b11 in / 
# Fri, 15 Jan 2021 01:38:29 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 22:42:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 22:42:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 22:42:23 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 22:42:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 22:42:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 22:42:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:42:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:42:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 22:42:24 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 22:42:25 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 22:42:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 22:42:25 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 22:42:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 22:42:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 22:49:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:44:48 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:44:51 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:44:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:44:51 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:38:41 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:38:56 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:38:57 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:38:57 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:38:57 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:39:09 GMT
ENV COMPOSER_VERSION=1.10.20
# Thu, 28 Jan 2021 22:39:10 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:39:11 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:39:12 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:39:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9e6a151110e36daa7a487250f98425289313f856e3a586d89d82bafc1bf322c3`  
		Last Modified: Fri, 15 Jan 2021 01:39:01 GMT  
		Size: 2.8 MB (2817152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b194694eae0c8525a66d3c56796eb37a9e263d63f03eaecf6bc83d2ab3f7c9`  
		Last Modified: Fri, 15 Jan 2021 23:50:55 GMT  
		Size: 1.8 MB (1793505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a9a95dec7f2cd3bcf6903d006a870fa7113f6a974d30ec6634ab82b0a0a792`  
		Last Modified: Fri, 15 Jan 2021 23:50:52 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ad687f5cfc54121cc70af5ff69cb844177c4325a2c14efcd144cb096ecfba2`  
		Last Modified: Fri, 15 Jan 2021 23:50:54 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ae4debbbbc31db383a639e6a7df85ebf9c2f15905a9ec2df4fb8a3998dec90`  
		Last Modified: Fri, 15 Jan 2021 23:50:56 GMT  
		Size: 10.7 MB (10661677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900efcbd73b95b91ec42e946efd16fa2e312e57beba40e9aac2b0699baa90d1d`  
		Last Modified: Fri, 15 Jan 2021 23:50:51 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c042850cc5dcebe86c931da9e6014fe607a6c507fe5a61059ba47003a80cac2`  
		Last Modified: Fri, 15 Jan 2021 23:51:00 GMT  
		Size: 15.3 MB (15348857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a592432a0a1e356653687e23dd3c8f953d0fc904db0377fa898de0c851be229d`  
		Last Modified: Thu, 21 Jan 2021 19:55:39 GMT  
		Size: 2.3 KB (2270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3b6898b8d491988e64358ef661f654c98cbec8cc3e36edeedea25334aae60e`  
		Last Modified: Thu, 21 Jan 2021 19:55:40 GMT  
		Size: 17.5 KB (17525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fcd335e71480482247bfd7863baa60db887184f8227377b99d22f61dc2a4d6`  
		Last Modified: Thu, 28 Jan 2021 22:39:38 GMT  
		Size: 32.3 MB (32292342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f574926dca5384453b345a61350707cbf2753926b84e8c685a1899bbe6ff5b`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 213.8 KB (213825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25022b6f8e9b3bd588f8db12caab7e929709dcb604f7f84786e3a7d54f6bd2f4`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a994c0ddb1f52a20e600cc2a3f65e7cc10c05053931d749c3003447c373c174e`  
		Last Modified: Thu, 28 Jan 2021 22:39:45 GMT  
		Size: 508.9 KB (508932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a8e706fc35dce4c888ff6a5600c1c4ca890bd470226f86c55f5b870f5716ba`  
		Last Modified: Thu, 28 Jan 2021 22:39:44 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33b7e4e5c37989586a88b9a4437f5db1926f1291aa88ea8692239638804cd9b`  
		Last Modified: Thu, 28 Jan 2021 22:39:44 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.10` - linux; ppc64le

```console
$ docker pull composer@sha256:64ec310b74e056c1a829af51d012910446deda6483099ab4fd21431b7c649ebe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (64004945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe32bddbb4094f3cd642c80e9f8dfe9e9fef99cd6cdcfeae23438ad7f483659`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 02:41:43 GMT
ADD file:137e8f98476d5dceaeb2e8359f50eb818dee4c327e4492d16e87fb27d40aa891 in / 
# Fri, 15 Jan 2021 02:41:46 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:17:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:17:44 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:17:56 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:18:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:18:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:18:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:18:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:18:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:18:39 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:18:43 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:18:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:19:07 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:19:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:19:38 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:24:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:33:15 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:33:36 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:33:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:33:47 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:26:03 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:27:01 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:27:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:27:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:27:24 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:28:39 GMT
ENV COMPOSER_VERSION=1.10.20
# Thu, 28 Jan 2021 22:29:02 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:29:09 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:29:17 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:29:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:29:44 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cb0f06c26ffdc2117b9a3467f79e69cdf8d9c677a3c0bacabc8a694a9fe303a8`  
		Last Modified: Fri, 15 Jan 2021 02:42:19 GMT  
		Size: 2.8 MB (2812389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9a7aad5bd113c5dca33b681663b0c58f66e510017e693801a6688a9c4bab60`  
		Last Modified: Sat, 16 Jan 2021 00:14:01 GMT  
		Size: 1.7 MB (1741834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ce1d80ff72759b98cf2f5ad1efa6dd181e5f4343bb0e25cbb4ec9d5d3847f4`  
		Last Modified: Sat, 16 Jan 2021 00:14:01 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48055526d8202af50f6248db9b3cb8938cab9cfec15a1312b4c1e3782f3307c4`  
		Last Modified: Sat, 16 Jan 2021 00:14:02 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7cb5ec22b0cc763855f0481247394a6e312f8f906d232f738fc88a4219bfb1e`  
		Last Modified: Sat, 16 Jan 2021 00:13:58 GMT  
		Size: 10.7 MB (10661716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea93ae862f86d372e01dcb82dbf509e78b3f4e6533f9660f4b63c49471cb4852`  
		Last Modified: Sat, 16 Jan 2021 00:13:57 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7518496c61b651e86a2bdd79ee76e400addfddbafa26db36f7e692520aeebc1e`  
		Last Modified: Sat, 16 Jan 2021 00:14:01 GMT  
		Size: 16.1 MB (16059509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dce1a5a13b51550c7b84a60d64d364686f108d412e4776aae7d7a4922ac1ebd`  
		Last Modified: Thu, 21 Jan 2021 20:03:07 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98df2e2e9c3e105f7ddf5634cc2558ef8a2e569cd7e61121bd1f18c83a96152d`  
		Last Modified: Thu, 21 Jan 2021 20:03:07 GMT  
		Size: 17.5 KB (17538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c3ac64e0e6d2c9f92c30e69ce18c62c2ff9ba34f99a48d00be9b92ccfcf393`  
		Last Modified: Thu, 28 Jan 2021 22:30:18 GMT  
		Size: 32.0 MB (31993881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fb84ebef4906eea3269f759da0902a8097011fb84006aabbd679b5950e0970`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 204.0 KB (204039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8dba6ae992e0605a8d35408b1a00afba44b82e2b40e0fde68e8181c954ff546`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07b7d2523e9bfca30dadee73bb72e48be92fa7ed7446ca26c4c5b6d88513f05`  
		Last Modified: Thu, 28 Jan 2021 22:30:35 GMT  
		Size: 509.0 KB (508958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496694a46b536e391969cc3377192c2d8b5199bb9abb26353c1480f80974425e`  
		Last Modified: Thu, 28 Jan 2021 22:30:35 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c1b4574bc541314a3ac8a8820e41e03672eeb834c9adb4a173c6ffaa7f15c5`  
		Last Modified: Thu, 28 Jan 2021 22:30:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.10` - linux; s390x

```console
$ docker pull composer@sha256:efb0271bdbdb3b0ed80df63d0ce30144363aff051fc6b1c6b4906535e3ec114b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61503008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3b4d800099b7a2589dff69a16ce36042ebdbb9f8aa76310d0167fcd872e1b7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:51:34 GMT
ADD file:3ba807ca8ed73ca14224dd26a883f2399031fa32430f035cc5ae97b5e6db0ca7 in / 
# Fri, 15 Jan 2021 01:51:35 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 22:57:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 22:57:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 22:57:13 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 22:57:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 22:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 22:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:57:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:57:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 22:57:17 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 22:57:17 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 22:57:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 22:57:18 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 22:57:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 22:57:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:02:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:54:10 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:54:13 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:54:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:54:14 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:42:35 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:42:53 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:42:54 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:42:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:42:54 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:43:05 GMT
ENV COMPOSER_VERSION=1.10.20
# Thu, 28 Jan 2021 22:43:07 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:43:07 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:43:07 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:43:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:43:08 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:3997176601fb5d5ac06922718668ede4acac00a5c0daef8a9099fd76ce93047f`  
		Last Modified: Fri, 15 Jan 2021 01:52:40 GMT  
		Size: 2.6 MB (2601720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497e79d9095f9ba4812f1150c33ad07d399f559fea8e3c4fe8553e02f2cf8b6a`  
		Last Modified: Fri, 15 Jan 2021 23:39:10 GMT  
		Size: 1.8 MB (1756352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99527660904ffc5aed1d27bb86166f189e04b5df76d7becf74efffb1836eaf5e`  
		Last Modified: Fri, 15 Jan 2021 23:39:10 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9b51111e1ef5a5156e505d6369bb2d4e21354a1203636fca6f26de34df9c15`  
		Last Modified: Fri, 15 Jan 2021 23:39:10 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3c721a3fef9acf0bac166c45ff18e2485752ef7b86447284b7b710646d40df`  
		Last Modified: Fri, 15 Jan 2021 23:38:47 GMT  
		Size: 10.7 MB (10661723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e676c2ca01980f72daf35a53dae36e4fe10945de76af81d54618066f5204c598`  
		Last Modified: Fri, 15 Jan 2021 23:38:48 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90c350aff0df72bb91eaa20306afe2218ac1d50242eb213d4e481f65b2a9f60`  
		Last Modified: Fri, 15 Jan 2021 23:38:48 GMT  
		Size: 14.4 MB (14364644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c91dec7c10d367e01e4907cb6c2d00b3e5b7390545c8c9499eaac3c35986507`  
		Last Modified: Thu, 21 Jan 2021 20:05:24 GMT  
		Size: 2.3 KB (2269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63e510378e653ab6ff71c58fc15e869877848171131d614af01c250d7a36e31`  
		Last Modified: Thu, 21 Jan 2021 20:05:20 GMT  
		Size: 17.5 KB (17541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4079b673c2155f6fc765bd4b8d683a2326dd552affe882edccb45c657534ed18`  
		Last Modified: Thu, 28 Jan 2021 22:43:28 GMT  
		Size: 31.4 MB (31389182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdeafc632059b12ff488232684da09d9c34de98941c5f6ff69c471274af7602`  
		Last Modified: Thu, 28 Jan 2021 22:43:22 GMT  
		Size: 197.8 KB (197815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f475e4a4966b8ce4d7561e4c7a2e4961201d5b118193c3525421174abaaa14e5`  
		Last Modified: Thu, 28 Jan 2021 22:43:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01db2c98c35df2890d6f5c065108d858de37de4b58a8af30d6830c024634d31`  
		Last Modified: Thu, 28 Jan 2021 22:43:38 GMT  
		Size: 509.0 KB (508952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807d3d6110e2b559a85eaf8fe97082ffeabdb11b432aafad723ba63a79f58746`  
		Last Modified: Thu, 28 Jan 2021 22:43:37 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd86330f0fa7ed84623e7652846606dff7efb38d5a5079076613ec22a547429f`  
		Last Modified: Thu, 28 Jan 2021 22:43:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `composer:1.10.20`

```console
$ docker pull composer@sha256:69f3e58d91b15f1abe7bf2506597f3909e7b53f33d21d18c1707599904d5b733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `composer:1.10.20` - linux; amd64

```console
$ docker pull composer@sha256:15041e5826ffbd609ed496774f5ef19128b1f5c6536a1294365813464f88d814
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62373497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de5740a8abd6c9f77e5008075537110c2545c4b35864292757f2f49ad03b529`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 02:23:51 GMT
ADD file:edbe213ae0c825a5bfbe569928cf20f683f334f93a093ccd0a3a014b7428e760 in / 
# Fri, 15 Jan 2021 02:23:51 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:43:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:43:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:43:26 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:43:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:43:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:43:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:43:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:43:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:43:30 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:43:30 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:43:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:43:31 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:43:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:43:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:51:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 20:17:47 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 20:17:50 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 20:17:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 20:17:51 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:32:03 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:32:24 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:32:24 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:32:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:32:25 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:32:34 GMT
ENV COMPOSER_VERSION=1.10.20
# Thu, 28 Jan 2021 22:32:36 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:32:36 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:32:36 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:32:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:32:37 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:596ba82af5aaa3e2fd9d6f955b8b94f0744a2b60710e3c243ba3e4a467f051d1`  
		Last Modified: Fri, 15 Jan 2021 02:08:10 GMT  
		Size: 2.8 MB (2810825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af74f285bb27c6623f2b5c8c3a2e487603c7dd5c51859fd6e13859542f4310c3`  
		Last Modified: Sat, 16 Jan 2021 01:00:24 GMT  
		Size: 1.7 MB (1694838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab8440e5667ccb2ffd4e62ed905a106742dfdd7dd3167d9d64b4bdeed8a4945`  
		Last Modified: Sat, 16 Jan 2021 01:00:20 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64889fa545ec919e6fe392c368b8cb41a10e7834c1ba4d4d96fd9ee2e3405cc1`  
		Last Modified: Sat, 16 Jan 2021 01:00:20 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94168e6487351b04d28db6aabb22e0c68ad3582533cf8d7e00322078720f8081`  
		Last Modified: Sat, 16 Jan 2021 01:00:19 GMT  
		Size: 10.7 MB (10661716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3898f14298ef25ab2005e9025a88f553003a83a1b6a61765e93d78879441aa36`  
		Last Modified: Sat, 16 Jan 2021 01:00:18 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3747e5f21671eba796a4b76a6abc180c60b0ef9414e9a80b325b31aeaa1f6ca`  
		Last Modified: Sat, 16 Jan 2021 01:00:21 GMT  
		Size: 15.3 MB (15318011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3df0f8088890764041d8dbfe574cd5bdf020400801b0b108cd6b7f965aab3a`  
		Last Modified: Thu, 21 Jan 2021 20:28:34 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f6ddeaf0bdcf495df2e7c8d72852796c1bae3d9f8ef8260058fdb43b995163`  
		Last Modified: Thu, 21 Jan 2021 20:28:34 GMT  
		Size: 17.5 KB (17539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29338fcaf9eb090ba02397a08616210ac758731039ac2d2a5db97288090a1845`  
		Last Modified: Thu, 28 Jan 2021 22:32:55 GMT  
		Size: 31.2 MB (31158400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a0bf379d52ae6a08ffd2313828e5738aa1cfd2a934c2403e6065ae7f94ba05`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 198.3 KB (198274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a346beb5e7dfc07424d1d661858912a89fab48a63bd89492e0c97c3cf1a6c75`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8191633d27c6e6161ac5ccc3f5112e823af18e5cc62bdfe4146589d7c44aebf1`  
		Last Modified: Thu, 28 Jan 2021 22:33:02 GMT  
		Size: 508.9 KB (508927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eac7632c4a851dce2efef3f2aa6da2e0d0571a278890a683388059992f89483`  
		Last Modified: Thu, 28 Jan 2021 22:33:02 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256c9cc11c9c202b76652699f47cb4c1ae4bfb8c76b50287be53de24ec90b653`  
		Last Modified: Thu, 28 Jan 2021 22:33:02 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.10.20` - linux; arm variant v6

```console
$ docker pull composer@sha256:681a45213e37b7024fd1986c8f4cac581a37f1bd3b5afac7146b96450347a7a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58221747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a4cabcfab9fbba95857b0c4844c30aed503a82b49272d278d8f0231b2ce2a4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 28 Jan 2021 23:49:59 GMT
ADD file:c197324e4979e2a7b257ad683d20dd9cbdae525a076bd68fe6aa0e0b126875df in / 
# Thu, 28 Jan 2021 23:49:59 GMT
CMD ["/bin/sh"]
# Fri, 29 Jan 2021 00:33:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 29 Jan 2021 00:33:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 29 Jan 2021 00:33:59 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 29 Jan 2021 00:34:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 29 Jan 2021 00:34:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 29 Jan 2021 00:34:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 29 Jan 2021 00:34:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 29 Jan 2021 00:34:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 29 Jan 2021 00:34:08 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 29 Jan 2021 00:34:11 GMT
ENV PHP_VERSION=8.0.1
# Fri, 29 Jan 2021 00:34:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 29 Jan 2021 00:34:13 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 29 Jan 2021 00:34:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 29 Jan 2021 00:34:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 29 Jan 2021 00:37:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 29 Jan 2021 00:37:35 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 29 Jan 2021 00:37:38 GMT
RUN docker-php-ext-enable sodium
# Fri, 29 Jan 2021 00:37:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 29 Jan 2021 00:37:40 GMT
CMD ["php" "-a"]
# Fri, 29 Jan 2021 02:11:29 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 29 Jan 2021 02:11:49 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 29 Jan 2021 02:11:51 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 29 Jan 2021 02:11:51 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 29 Jan 2021 02:11:52 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 29 Jan 2021 02:12:09 GMT
ENV COMPOSER_VERSION=1.10.20
# Fri, 29 Jan 2021 02:12:12 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 29 Jan 2021 02:12:12 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 29 Jan 2021 02:12:13 GMT
WORKDIR /app
# Fri, 29 Jan 2021 02:12:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 29 Jan 2021 02:12:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a66f440da051140fefcb0a520bdeb69d763b1eb4fd1b2ed46b4c0a168e335108`  
		Last Modified: Thu, 28 Jan 2021 23:50:33 GMT  
		Size: 2.6 MB (2621759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa34846effbef1e901021c65a67535efc29a1aa39b259a4c29559d1439f4131`  
		Last Modified: Fri, 29 Jan 2021 01:05:52 GMT  
		Size: 1.7 MB (1684855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba088c5e0e1fb4c64a8b59354bedcae82636c10a93fe3790125bec5c1e841299`  
		Last Modified: Fri, 29 Jan 2021 01:05:51 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b10584422ada7d37ac091eae04bcee5df4cee5b93cd86068ce55c7ab085ae62`  
		Last Modified: Fri, 29 Jan 2021 01:05:51 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd2125b643842a0b1fb7799c57d504cb3ea72f1cdaac6d48b6d3ee2fa033d39`  
		Last Modified: Fri, 29 Jan 2021 01:05:50 GMT  
		Size: 10.7 MB (10661723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370c8d7d436fffa9dd306db82b4a90f7b25ae1d68c658dac4c195ec6a921976e`  
		Last Modified: Fri, 29 Jan 2021 01:05:49 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c1bd9522799773adb723d78cef494168d851dd759ef42bdf230e3518c9888d`  
		Last Modified: Fri, 29 Jan 2021 01:05:54 GMT  
		Size: 13.6 MB (13571709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60b70fa5215a21be024094dd917f70d206590186d21137fcb75d1fb68a887a2`  
		Last Modified: Fri, 29 Jan 2021 01:05:49 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733b25bcaba65cbff9b151c9ab65d005350d890d7728bfe14024f5f4bd9ca890`  
		Last Modified: Fri, 29 Jan 2021 01:05:49 GMT  
		Size: 17.5 KB (17531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dda7886eea28b54dfe2eea50537d02027bbbcda31bb0d081dff700b99290584`  
		Last Modified: Fri, 29 Jan 2021 02:12:41 GMT  
		Size: 29.0 MB (28956651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90907b51293338df699b9f07cbb70441610fa8f2924e32d21967026449fe4064`  
		Last Modified: Fri, 29 Jan 2021 02:12:28 GMT  
		Size: 193.5 KB (193490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85552216f6bbc21bc776e9622f10a51b96b9a92310894072d91339b4fe625b1e`  
		Last Modified: Fri, 29 Jan 2021 02:12:28 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826269360f1b18acb29abbbca07ffda1fb53dc87ea68b0b9044157f2aea8dcd7`  
		Last Modified: Fri, 29 Jan 2021 02:12:51 GMT  
		Size: 508.9 KB (508950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1040cda38a25cfabe23a4f3025d4fd9430498b5da7860c6fc370d0e8a675288b`  
		Last Modified: Fri, 29 Jan 2021 02:12:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b870d06eca9355beb7c18b2bc89e44760735adfe9c4dbb3b36b6edeee5f761cd`  
		Last Modified: Fri, 29 Jan 2021 02:12:51 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.10.20` - linux; arm variant v7

```console
$ docker pull composer@sha256:8c924eed02fb1a3b071e3741eac381bcd2f6e461e6c16dea19d46a35336df585
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56063307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37defddda0760cf3372f74c959e1335a4fc24f5f353a9b3b920abfe647d2c36`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:58:27 GMT
ADD file:718d7c24a8d6ff0feb2843cf8c3ca4b7ef1fb523a45dea568404259a7b4e6f10 in / 
# Fri, 15 Jan 2021 01:58:29 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:04:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:04:05 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:04:07 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:04:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:04:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:04:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:04:13 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:04:14 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:04:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:04:15 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:04:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:04:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:07:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:10:13 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:10:16 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:10:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:10:18 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 21:57:49 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 21:58:13 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 21:58:15 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 21:58:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 21:58:17 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 21:58:36 GMT
ENV COMPOSER_VERSION=1.10.20
# Thu, 28 Jan 2021 21:58:39 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 21:58:40 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 21:58:40 GMT
WORKDIR /app
# Thu, 28 Jan 2021 21:58:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 21:58:42 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:0f34ce5da94097b8c334f6b2065a010aced9855c3532e4462e9bd1b0a4c4b3f6`  
		Last Modified: Fri, 15 Jan 2021 01:59:13 GMT  
		Size: 2.4 MB (2422744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cecec77a7b5b50913bcb9f7bfe0c5fdcebb948b947747285290197c13902be91`  
		Last Modified: Fri, 15 Jan 2021 23:42:36 GMT  
		Size: 1.6 MB (1555130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0496082b3c55009a50b47ce80bf27dd7451aaa7e13b5b4ccbe886a780c614dd1`  
		Last Modified: Fri, 15 Jan 2021 23:42:33 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af351861d88fff830659b71d51e45b8e623d31cb86c764fab107e6c39ca5a717`  
		Last Modified: Fri, 15 Jan 2021 23:42:33 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11aa9107e62f7893b45936388317768641833b4f6b1937989fcbfc5845e1c698`  
		Last Modified: Fri, 15 Jan 2021 23:42:32 GMT  
		Size: 10.7 MB (10661711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739d880e478996d44b501dcc056bf9f5f25909c929d579ba0c02f123be170522`  
		Last Modified: Fri, 15 Jan 2021 23:42:30 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed2a0f0dbdad0b49284a158baa86126c2b2a794ee53b82c4181378520555f1d`  
		Last Modified: Fri, 15 Jan 2021 23:42:36 GMT  
		Size: 13.1 MB (13070133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b9ed4df09ec14031c338ad506ba7fcc76ab6a07fc32432ad75d94867ae04d9`  
		Last Modified: Thu, 21 Jan 2021 19:23:58 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500dd1602efbacb91e481ac3e868dadb7bca74fb6b4f73d41fb2ec82cab72f22`  
		Last Modified: Thu, 21 Jan 2021 19:23:59 GMT  
		Size: 17.5 KB (17536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b52f140a609f714bafc66c167ec2b6c04c8962153f406e1ac18bac7b669c61`  
		Last Modified: Thu, 28 Jan 2021 21:59:15 GMT  
		Size: 27.6 MB (27635729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cb9e5e751c90392752772de98a302d52a12f4ea2dcf08223098a5cb41c1fd4`  
		Last Modified: Thu, 28 Jan 2021 21:58:57 GMT  
		Size: 186.3 KB (186294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964a5881822f5f5e182f7b8d8fef32582177380aff1c392f68c3c5f908be31d4`  
		Last Modified: Thu, 28 Jan 2021 21:58:57 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f372f4a1d57fcda1ba2142f3ead85e6bbf97c49e1aeb89bb65e355ab41bfea6e`  
		Last Modified: Thu, 28 Jan 2021 21:59:27 GMT  
		Size: 509.0 KB (508954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52252a296f2b0f0d04e335396310b8ce47f5313114ac535d44c3233623e2e112`  
		Last Modified: Thu, 28 Jan 2021 21:59:27 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ca700269cc2d3c3588c2afe11cec218a2afc3fd62460983326434a940d8394`  
		Last Modified: Thu, 28 Jan 2021 21:59:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.10.20` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:f0c754ec0e20b19ed5482233110351043b98ca186e677e46c0784e6390973eb3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61935669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd59253a35bffa6894e23823e2d163cc891258a2175959f10445847410c63aa5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:47:51 GMT
ADD file:95be2cec37537b3fd70aeb1d4eb3479fc4a56b00ad7180788ddd7fa772ca65e7 in / 
# Fri, 15 Jan 2021 01:47:52 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:04:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:04:28 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:04:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:04:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:04:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:04:39 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:04:40 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:04:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:04:41 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:04:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:04:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:09:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:51:20 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:51:27 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:51:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:51:31 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:39:49 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:40:10 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:40:12 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:40:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:40:14 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:40:35 GMT
ENV COMPOSER_VERSION=1.10.20
# Thu, 28 Jan 2021 22:40:38 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:40:39 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:40:40 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:40:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:40:41 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:30d5333d20a68dd6ea3689e2c5692d7071f2d68e72c06f0b3b4c7e213df454e2`  
		Last Modified: Fri, 15 Jan 2021 01:48:29 GMT  
		Size: 2.7 MB (2710904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72077bc47778707d4c51904bf6932e44a09d9a5a37f1bac45ef59fe94bc54e1`  
		Last Modified: Fri, 15 Jan 2021 23:49:43 GMT  
		Size: 1.7 MB (1694577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bfc628cf72db6285835ff062834a15ee7c9067f6b7ccb55fad0a8bb0f292be`  
		Last Modified: Fri, 15 Jan 2021 23:49:41 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ab015e378a2ad2e4c345884006fc6b1678a0ebba44214fbc5e9dcb48ef7bb2`  
		Last Modified: Fri, 15 Jan 2021 23:49:41 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d24a448de09dec3ceb6bc305d0c17be120e79f5611f1e4054850e11526133cc8`  
		Last Modified: Fri, 15 Jan 2021 23:49:39 GMT  
		Size: 10.7 MB (10661733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8079f19e688581d52496f1937db9dc33ef25e597b149eb517633043678bd61d2`  
		Last Modified: Fri, 15 Jan 2021 23:49:39 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978c3da5ab542fa26ea4333b9b5c608d2ee68fa98cbf1e0d05df83ece9439e24`  
		Last Modified: Fri, 15 Jan 2021 23:49:45 GMT  
		Size: 14.8 MB (14764647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1043bb484cdf4818387523cb0c703d862e1c50b54ebe62f605c0d3b74837f39`  
		Last Modified: Thu, 21 Jan 2021 20:05:13 GMT  
		Size: 2.3 KB (2269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c953f678545439a3b425e1dd037e3e5d5b8092e37adb1a63cb110a0a888b5300`  
		Last Modified: Thu, 21 Jan 2021 20:05:12 GMT  
		Size: 17.6 KB (17550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f77742777349432a5c810bb823719115d594ef2d7e0d79d11fdccf49b1c298`  
		Last Modified: Thu, 28 Jan 2021 22:41:08 GMT  
		Size: 31.4 MB (31376168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20f98fa3077571418cb9ac1f3ceb60436f9c6bcda79d861d68e9c48787403d1`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 196.1 KB (196059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899d29da6e7af774384acf87f4eea2a9876f6bff3365b1486ecb6738a8e95143`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c98b0e6011753de7f48370ec14b7d6df3edd44bea6c654333efab43d29ecf1`  
		Last Modified: Thu, 28 Jan 2021 22:41:25 GMT  
		Size: 509.0 KB (508952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58045ba48e2988e029a9204473be18429006cfff4e1415ee55c04fad8e97cc2`  
		Last Modified: Thu, 28 Jan 2021 22:41:24 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5366c00175f04b24edf1440c7b0ac425e885f97839ee2b42533db92c19f0df`  
		Last Modified: Thu, 28 Jan 2021 22:41:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.10.20` - linux; 386

```console
$ docker pull composer@sha256:522d1c17cfd4585f4db74672c4594ba0c2e10eaa887194fb74aafcc5639d55e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63658787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd03c16d8b1151c76d26e7c44166aae340dcc1257ba9cee77733961c3484b8f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:38:28 GMT
ADD file:d8723c02f1eb0efa4dadc6480a753d18d7e28d9815bff96a92ff09ff55a92b11 in / 
# Fri, 15 Jan 2021 01:38:29 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 22:42:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 22:42:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 22:42:23 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 22:42:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 22:42:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 22:42:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:42:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:42:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 22:42:24 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 22:42:25 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 22:42:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 22:42:25 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 22:42:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 22:42:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 22:49:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:44:48 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:44:51 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:44:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:44:51 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:38:41 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:38:56 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:38:57 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:38:57 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:38:57 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:39:09 GMT
ENV COMPOSER_VERSION=1.10.20
# Thu, 28 Jan 2021 22:39:10 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:39:11 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:39:12 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:39:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9e6a151110e36daa7a487250f98425289313f856e3a586d89d82bafc1bf322c3`  
		Last Modified: Fri, 15 Jan 2021 01:39:01 GMT  
		Size: 2.8 MB (2817152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b194694eae0c8525a66d3c56796eb37a9e263d63f03eaecf6bc83d2ab3f7c9`  
		Last Modified: Fri, 15 Jan 2021 23:50:55 GMT  
		Size: 1.8 MB (1793505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a9a95dec7f2cd3bcf6903d006a870fa7113f6a974d30ec6634ab82b0a0a792`  
		Last Modified: Fri, 15 Jan 2021 23:50:52 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ad687f5cfc54121cc70af5ff69cb844177c4325a2c14efcd144cb096ecfba2`  
		Last Modified: Fri, 15 Jan 2021 23:50:54 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ae4debbbbc31db383a639e6a7df85ebf9c2f15905a9ec2df4fb8a3998dec90`  
		Last Modified: Fri, 15 Jan 2021 23:50:56 GMT  
		Size: 10.7 MB (10661677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900efcbd73b95b91ec42e946efd16fa2e312e57beba40e9aac2b0699baa90d1d`  
		Last Modified: Fri, 15 Jan 2021 23:50:51 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c042850cc5dcebe86c931da9e6014fe607a6c507fe5a61059ba47003a80cac2`  
		Last Modified: Fri, 15 Jan 2021 23:51:00 GMT  
		Size: 15.3 MB (15348857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a592432a0a1e356653687e23dd3c8f953d0fc904db0377fa898de0c851be229d`  
		Last Modified: Thu, 21 Jan 2021 19:55:39 GMT  
		Size: 2.3 KB (2270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3b6898b8d491988e64358ef661f654c98cbec8cc3e36edeedea25334aae60e`  
		Last Modified: Thu, 21 Jan 2021 19:55:40 GMT  
		Size: 17.5 KB (17525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fcd335e71480482247bfd7863baa60db887184f8227377b99d22f61dc2a4d6`  
		Last Modified: Thu, 28 Jan 2021 22:39:38 GMT  
		Size: 32.3 MB (32292342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f574926dca5384453b345a61350707cbf2753926b84e8c685a1899bbe6ff5b`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 213.8 KB (213825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25022b6f8e9b3bd588f8db12caab7e929709dcb604f7f84786e3a7d54f6bd2f4`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a994c0ddb1f52a20e600cc2a3f65e7cc10c05053931d749c3003447c373c174e`  
		Last Modified: Thu, 28 Jan 2021 22:39:45 GMT  
		Size: 508.9 KB (508932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a8e706fc35dce4c888ff6a5600c1c4ca890bd470226f86c55f5b870f5716ba`  
		Last Modified: Thu, 28 Jan 2021 22:39:44 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33b7e4e5c37989586a88b9a4437f5db1926f1291aa88ea8692239638804cd9b`  
		Last Modified: Thu, 28 Jan 2021 22:39:44 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.10.20` - linux; ppc64le

```console
$ docker pull composer@sha256:64ec310b74e056c1a829af51d012910446deda6483099ab4fd21431b7c649ebe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (64004945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe32bddbb4094f3cd642c80e9f8dfe9e9fef99cd6cdcfeae23438ad7f483659`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 02:41:43 GMT
ADD file:137e8f98476d5dceaeb2e8359f50eb818dee4c327e4492d16e87fb27d40aa891 in / 
# Fri, 15 Jan 2021 02:41:46 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:17:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:17:44 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:17:56 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:18:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:18:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:18:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:18:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:18:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:18:39 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:18:43 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:18:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:19:07 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:19:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:19:38 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:24:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:33:15 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:33:36 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:33:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:33:47 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:26:03 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:27:01 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:27:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:27:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:27:24 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:28:39 GMT
ENV COMPOSER_VERSION=1.10.20
# Thu, 28 Jan 2021 22:29:02 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:29:09 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:29:17 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:29:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:29:44 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cb0f06c26ffdc2117b9a3467f79e69cdf8d9c677a3c0bacabc8a694a9fe303a8`  
		Last Modified: Fri, 15 Jan 2021 02:42:19 GMT  
		Size: 2.8 MB (2812389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9a7aad5bd113c5dca33b681663b0c58f66e510017e693801a6688a9c4bab60`  
		Last Modified: Sat, 16 Jan 2021 00:14:01 GMT  
		Size: 1.7 MB (1741834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ce1d80ff72759b98cf2f5ad1efa6dd181e5f4343bb0e25cbb4ec9d5d3847f4`  
		Last Modified: Sat, 16 Jan 2021 00:14:01 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48055526d8202af50f6248db9b3cb8938cab9cfec15a1312b4c1e3782f3307c4`  
		Last Modified: Sat, 16 Jan 2021 00:14:02 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7cb5ec22b0cc763855f0481247394a6e312f8f906d232f738fc88a4219bfb1e`  
		Last Modified: Sat, 16 Jan 2021 00:13:58 GMT  
		Size: 10.7 MB (10661716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea93ae862f86d372e01dcb82dbf509e78b3f4e6533f9660f4b63c49471cb4852`  
		Last Modified: Sat, 16 Jan 2021 00:13:57 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7518496c61b651e86a2bdd79ee76e400addfddbafa26db36f7e692520aeebc1e`  
		Last Modified: Sat, 16 Jan 2021 00:14:01 GMT  
		Size: 16.1 MB (16059509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dce1a5a13b51550c7b84a60d64d364686f108d412e4776aae7d7a4922ac1ebd`  
		Last Modified: Thu, 21 Jan 2021 20:03:07 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98df2e2e9c3e105f7ddf5634cc2558ef8a2e569cd7e61121bd1f18c83a96152d`  
		Last Modified: Thu, 21 Jan 2021 20:03:07 GMT  
		Size: 17.5 KB (17538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c3ac64e0e6d2c9f92c30e69ce18c62c2ff9ba34f99a48d00be9b92ccfcf393`  
		Last Modified: Thu, 28 Jan 2021 22:30:18 GMT  
		Size: 32.0 MB (31993881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fb84ebef4906eea3269f759da0902a8097011fb84006aabbd679b5950e0970`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 204.0 KB (204039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8dba6ae992e0605a8d35408b1a00afba44b82e2b40e0fde68e8181c954ff546`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07b7d2523e9bfca30dadee73bb72e48be92fa7ed7446ca26c4c5b6d88513f05`  
		Last Modified: Thu, 28 Jan 2021 22:30:35 GMT  
		Size: 509.0 KB (508958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496694a46b536e391969cc3377192c2d8b5199bb9abb26353c1480f80974425e`  
		Last Modified: Thu, 28 Jan 2021 22:30:35 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c1b4574bc541314a3ac8a8820e41e03672eeb834c9adb4a173c6ffaa7f15c5`  
		Last Modified: Thu, 28 Jan 2021 22:30:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:1.10.20` - linux; s390x

```console
$ docker pull composer@sha256:efb0271bdbdb3b0ed80df63d0ce30144363aff051fc6b1c6b4906535e3ec114b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61503008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3b4d800099b7a2589dff69a16ce36042ebdbb9f8aa76310d0167fcd872e1b7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:51:34 GMT
ADD file:3ba807ca8ed73ca14224dd26a883f2399031fa32430f035cc5ae97b5e6db0ca7 in / 
# Fri, 15 Jan 2021 01:51:35 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 22:57:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 22:57:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 22:57:13 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 22:57:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 22:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 22:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:57:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:57:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 22:57:17 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 22:57:17 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 22:57:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 22:57:18 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 22:57:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 22:57:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:02:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:54:10 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:54:13 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:54:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:54:14 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:42:35 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:42:53 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:42:54 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:42:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:42:54 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:43:05 GMT
ENV COMPOSER_VERSION=1.10.20
# Thu, 28 Jan 2021 22:43:07 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:43:07 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:43:07 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:43:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:43:08 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:3997176601fb5d5ac06922718668ede4acac00a5c0daef8a9099fd76ce93047f`  
		Last Modified: Fri, 15 Jan 2021 01:52:40 GMT  
		Size: 2.6 MB (2601720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497e79d9095f9ba4812f1150c33ad07d399f559fea8e3c4fe8553e02f2cf8b6a`  
		Last Modified: Fri, 15 Jan 2021 23:39:10 GMT  
		Size: 1.8 MB (1756352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99527660904ffc5aed1d27bb86166f189e04b5df76d7becf74efffb1836eaf5e`  
		Last Modified: Fri, 15 Jan 2021 23:39:10 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9b51111e1ef5a5156e505d6369bb2d4e21354a1203636fca6f26de34df9c15`  
		Last Modified: Fri, 15 Jan 2021 23:39:10 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3c721a3fef9acf0bac166c45ff18e2485752ef7b86447284b7b710646d40df`  
		Last Modified: Fri, 15 Jan 2021 23:38:47 GMT  
		Size: 10.7 MB (10661723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e676c2ca01980f72daf35a53dae36e4fe10945de76af81d54618066f5204c598`  
		Last Modified: Fri, 15 Jan 2021 23:38:48 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90c350aff0df72bb91eaa20306afe2218ac1d50242eb213d4e481f65b2a9f60`  
		Last Modified: Fri, 15 Jan 2021 23:38:48 GMT  
		Size: 14.4 MB (14364644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c91dec7c10d367e01e4907cb6c2d00b3e5b7390545c8c9499eaac3c35986507`  
		Last Modified: Thu, 21 Jan 2021 20:05:24 GMT  
		Size: 2.3 KB (2269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63e510378e653ab6ff71c58fc15e869877848171131d614af01c250d7a36e31`  
		Last Modified: Thu, 21 Jan 2021 20:05:20 GMT  
		Size: 17.5 KB (17541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4079b673c2155f6fc765bd4b8d683a2326dd552affe882edccb45c657534ed18`  
		Last Modified: Thu, 28 Jan 2021 22:43:28 GMT  
		Size: 31.4 MB (31389182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdeafc632059b12ff488232684da09d9c34de98941c5f6ff69c471274af7602`  
		Last Modified: Thu, 28 Jan 2021 22:43:22 GMT  
		Size: 197.8 KB (197815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f475e4a4966b8ce4d7561e4c7a2e4961201d5b118193c3525421174abaaa14e5`  
		Last Modified: Thu, 28 Jan 2021 22:43:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01db2c98c35df2890d6f5c065108d858de37de4b58a8af30d6830c024634d31`  
		Last Modified: Thu, 28 Jan 2021 22:43:38 GMT  
		Size: 509.0 KB (508952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807d3d6110e2b559a85eaf8fe97082ffeabdb11b432aafad723ba63a79f58746`  
		Last Modified: Thu, 28 Jan 2021 22:43:37 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd86330f0fa7ed84623e7652846606dff7efb38d5a5079076613ec22a547429f`  
		Last Modified: Thu, 28 Jan 2021 22:43:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `composer:2`

```console
$ docker pull composer@sha256:f8dfdbaac5983fe7698848442d1d0a39753ef72715391bdbd4553d0b2636020d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `composer:2` - linux; amd64

```console
$ docker pull composer@sha256:005d4a50002fcf58eb93b749345b73441cb615644f0790844538d0990cc3ce20
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62417362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e0bd4ead1c9c98e491c19a4b10307760a1a5060996f40e5f5229bd6882b578`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 02:23:51 GMT
ADD file:edbe213ae0c825a5bfbe569928cf20f683f334f93a093ccd0a3a014b7428e760 in / 
# Fri, 15 Jan 2021 02:23:51 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:43:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:43:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:43:26 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:43:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:43:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:43:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:43:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:43:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:43:30 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:43:30 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:43:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:43:31 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:43:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:43:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:51:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 20:17:47 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 20:17:50 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 20:17:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 20:17:51 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:32:03 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:32:24 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:32:24 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:32:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:32:25 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:32:25 GMT
ENV COMPOSER_VERSION=2.0.9
# Thu, 28 Jan 2021 22:32:27 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:32:27 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:32:28 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:32:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:32:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:596ba82af5aaa3e2fd9d6f955b8b94f0744a2b60710e3c243ba3e4a467f051d1`  
		Last Modified: Fri, 15 Jan 2021 02:08:10 GMT  
		Size: 2.8 MB (2810825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af74f285bb27c6623f2b5c8c3a2e487603c7dd5c51859fd6e13859542f4310c3`  
		Last Modified: Sat, 16 Jan 2021 01:00:24 GMT  
		Size: 1.7 MB (1694838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab8440e5667ccb2ffd4e62ed905a106742dfdd7dd3167d9d64b4bdeed8a4945`  
		Last Modified: Sat, 16 Jan 2021 01:00:20 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64889fa545ec919e6fe392c368b8cb41a10e7834c1ba4d4d96fd9ee2e3405cc1`  
		Last Modified: Sat, 16 Jan 2021 01:00:20 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94168e6487351b04d28db6aabb22e0c68ad3582533cf8d7e00322078720f8081`  
		Last Modified: Sat, 16 Jan 2021 01:00:19 GMT  
		Size: 10.7 MB (10661716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3898f14298ef25ab2005e9025a88f553003a83a1b6a61765e93d78879441aa36`  
		Last Modified: Sat, 16 Jan 2021 01:00:18 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3747e5f21671eba796a4b76a6abc180c60b0ef9414e9a80b325b31aeaa1f6ca`  
		Last Modified: Sat, 16 Jan 2021 01:00:21 GMT  
		Size: 15.3 MB (15318011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3df0f8088890764041d8dbfe574cd5bdf020400801b0b108cd6b7f965aab3a`  
		Last Modified: Thu, 21 Jan 2021 20:28:34 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f6ddeaf0bdcf495df2e7c8d72852796c1bae3d9f8ef8260058fdb43b995163`  
		Last Modified: Thu, 21 Jan 2021 20:28:34 GMT  
		Size: 17.5 KB (17539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29338fcaf9eb090ba02397a08616210ac758731039ac2d2a5db97288090a1845`  
		Last Modified: Thu, 28 Jan 2021 22:32:55 GMT  
		Size: 31.2 MB (31158400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a0bf379d52ae6a08ffd2313828e5738aa1cfd2a934c2403e6065ae7f94ba05`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 198.3 KB (198274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a346beb5e7dfc07424d1d661858912a89fab48a63bd89492e0c97c3cf1a6c75`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e86daf479799f96a49bc265571da38b2be4344f28a6b8ed4a0a18cb1dafae08`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 552.8 KB (552794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048afd2f48877072346dfbc095e6883b2ccc828164f17723d6e95d230c798b83`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad27987395f1263b907d761fc5f4b5a356869262f62cd2b055f7c8bb050317ac`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 90.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2` - linux; arm variant v6

```console
$ docker pull composer@sha256:8555fcdcc559af5253afc8400e8f2f92937211b20947c2b1d231b3ab2a703663
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58265639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d766a7469442cfbfeb325a177218e32152d532c8efaec2dd15a2fd56020467`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 28 Jan 2021 23:49:59 GMT
ADD file:c197324e4979e2a7b257ad683d20dd9cbdae525a076bd68fe6aa0e0b126875df in / 
# Thu, 28 Jan 2021 23:49:59 GMT
CMD ["/bin/sh"]
# Fri, 29 Jan 2021 00:33:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 29 Jan 2021 00:33:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 29 Jan 2021 00:33:59 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 29 Jan 2021 00:34:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 29 Jan 2021 00:34:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 29 Jan 2021 00:34:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 29 Jan 2021 00:34:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 29 Jan 2021 00:34:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 29 Jan 2021 00:34:08 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 29 Jan 2021 00:34:11 GMT
ENV PHP_VERSION=8.0.1
# Fri, 29 Jan 2021 00:34:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 29 Jan 2021 00:34:13 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 29 Jan 2021 00:34:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 29 Jan 2021 00:34:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 29 Jan 2021 00:37:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 29 Jan 2021 00:37:35 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 29 Jan 2021 00:37:38 GMT
RUN docker-php-ext-enable sodium
# Fri, 29 Jan 2021 00:37:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 29 Jan 2021 00:37:40 GMT
CMD ["php" "-a"]
# Fri, 29 Jan 2021 02:11:29 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 29 Jan 2021 02:11:49 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 29 Jan 2021 02:11:51 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 29 Jan 2021 02:11:51 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 29 Jan 2021 02:11:52 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 29 Jan 2021 02:11:52 GMT
ENV COMPOSER_VERSION=2.0.9
# Fri, 29 Jan 2021 02:11:55 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 29 Jan 2021 02:11:56 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 29 Jan 2021 02:11:57 GMT
WORKDIR /app
# Fri, 29 Jan 2021 02:11:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 29 Jan 2021 02:11:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a66f440da051140fefcb0a520bdeb69d763b1eb4fd1b2ed46b4c0a168e335108`  
		Last Modified: Thu, 28 Jan 2021 23:50:33 GMT  
		Size: 2.6 MB (2621759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa34846effbef1e901021c65a67535efc29a1aa39b259a4c29559d1439f4131`  
		Last Modified: Fri, 29 Jan 2021 01:05:52 GMT  
		Size: 1.7 MB (1684855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba088c5e0e1fb4c64a8b59354bedcae82636c10a93fe3790125bec5c1e841299`  
		Last Modified: Fri, 29 Jan 2021 01:05:51 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b10584422ada7d37ac091eae04bcee5df4cee5b93cd86068ce55c7ab085ae62`  
		Last Modified: Fri, 29 Jan 2021 01:05:51 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd2125b643842a0b1fb7799c57d504cb3ea72f1cdaac6d48b6d3ee2fa033d39`  
		Last Modified: Fri, 29 Jan 2021 01:05:50 GMT  
		Size: 10.7 MB (10661723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370c8d7d436fffa9dd306db82b4a90f7b25ae1d68c658dac4c195ec6a921976e`  
		Last Modified: Fri, 29 Jan 2021 01:05:49 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c1bd9522799773adb723d78cef494168d851dd759ef42bdf230e3518c9888d`  
		Last Modified: Fri, 29 Jan 2021 01:05:54 GMT  
		Size: 13.6 MB (13571709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60b70fa5215a21be024094dd917f70d206590186d21137fcb75d1fb68a887a2`  
		Last Modified: Fri, 29 Jan 2021 01:05:49 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733b25bcaba65cbff9b151c9ab65d005350d890d7728bfe14024f5f4bd9ca890`  
		Last Modified: Fri, 29 Jan 2021 01:05:49 GMT  
		Size: 17.5 KB (17531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dda7886eea28b54dfe2eea50537d02027bbbcda31bb0d081dff700b99290584`  
		Last Modified: Fri, 29 Jan 2021 02:12:41 GMT  
		Size: 29.0 MB (28956651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90907b51293338df699b9f07cbb70441610fa8f2924e32d21967026449fe4064`  
		Last Modified: Fri, 29 Jan 2021 02:12:28 GMT  
		Size: 193.5 KB (193490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85552216f6bbc21bc776e9622f10a51b96b9a92310894072d91339b4fe625b1e`  
		Last Modified: Fri, 29 Jan 2021 02:12:28 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277406688472a6794691f5e4a67b9a1fff148488bd3592f46c1ff32c50b9e712`  
		Last Modified: Fri, 29 Jan 2021 02:12:28 GMT  
		Size: 552.8 KB (552840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31adf754bdf3aa207b3395bac818c602ae3326449c8eef1d435c2deefb3a2dd0`  
		Last Modified: Fri, 29 Jan 2021 02:12:29 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d326c954a1dde2641329fe23cd34f82ea22e784961b8e5e3098ea38e58e06bf`  
		Last Modified: Fri, 29 Jan 2021 02:12:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2` - linux; arm variant v7

```console
$ docker pull composer@sha256:269f67fe496ec79ec849b998dff19dd47f34368253361860e8c85cdc3fe60289
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56107193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929093143b6d7781fa9c2240f279fcb895b68e0ff527e64b6cd13779c07c5f9d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:58:27 GMT
ADD file:718d7c24a8d6ff0feb2843cf8c3ca4b7ef1fb523a45dea568404259a7b4e6f10 in / 
# Fri, 15 Jan 2021 01:58:29 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:04:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:04:05 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:04:07 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:04:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:04:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:04:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:04:13 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:04:14 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:04:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:04:15 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:04:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:04:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:07:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:10:13 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:10:16 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:10:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:10:18 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 21:57:49 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 21:58:13 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 21:58:15 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 21:58:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 21:58:17 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 21:58:17 GMT
ENV COMPOSER_VERSION=2.0.9
# Thu, 28 Jan 2021 21:58:21 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 21:58:21 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 21:58:22 GMT
WORKDIR /app
# Thu, 28 Jan 2021 21:58:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 21:58:24 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:0f34ce5da94097b8c334f6b2065a010aced9855c3532e4462e9bd1b0a4c4b3f6`  
		Last Modified: Fri, 15 Jan 2021 01:59:13 GMT  
		Size: 2.4 MB (2422744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cecec77a7b5b50913bcb9f7bfe0c5fdcebb948b947747285290197c13902be91`  
		Last Modified: Fri, 15 Jan 2021 23:42:36 GMT  
		Size: 1.6 MB (1555130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0496082b3c55009a50b47ce80bf27dd7451aaa7e13b5b4ccbe886a780c614dd1`  
		Last Modified: Fri, 15 Jan 2021 23:42:33 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af351861d88fff830659b71d51e45b8e623d31cb86c764fab107e6c39ca5a717`  
		Last Modified: Fri, 15 Jan 2021 23:42:33 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11aa9107e62f7893b45936388317768641833b4f6b1937989fcbfc5845e1c698`  
		Last Modified: Fri, 15 Jan 2021 23:42:32 GMT  
		Size: 10.7 MB (10661711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739d880e478996d44b501dcc056bf9f5f25909c929d579ba0c02f123be170522`  
		Last Modified: Fri, 15 Jan 2021 23:42:30 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed2a0f0dbdad0b49284a158baa86126c2b2a794ee53b82c4181378520555f1d`  
		Last Modified: Fri, 15 Jan 2021 23:42:36 GMT  
		Size: 13.1 MB (13070133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b9ed4df09ec14031c338ad506ba7fcc76ab6a07fc32432ad75d94867ae04d9`  
		Last Modified: Thu, 21 Jan 2021 19:23:58 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500dd1602efbacb91e481ac3e868dadb7bca74fb6b4f73d41fb2ec82cab72f22`  
		Last Modified: Thu, 21 Jan 2021 19:23:59 GMT  
		Size: 17.5 KB (17536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b52f140a609f714bafc66c167ec2b6c04c8962153f406e1ac18bac7b669c61`  
		Last Modified: Thu, 28 Jan 2021 21:59:15 GMT  
		Size: 27.6 MB (27635729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cb9e5e751c90392752772de98a302d52a12f4ea2dcf08223098a5cb41c1fd4`  
		Last Modified: Thu, 28 Jan 2021 21:58:57 GMT  
		Size: 186.3 KB (186294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964a5881822f5f5e182f7b8d8fef32582177380aff1c392f68c3c5f908be31d4`  
		Last Modified: Thu, 28 Jan 2021 21:58:57 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174e82ce233fe45d2052d89f8f6ceb309742ffa529fff02fe0a3bf4f0dc2680e`  
		Last Modified: Thu, 28 Jan 2021 21:58:58 GMT  
		Size: 552.8 KB (552840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea9421b9b2b639e1f21013f53e1e2cb09a3ec7f0dd823ee954f9244314cf5f8`  
		Last Modified: Thu, 28 Jan 2021 21:58:57 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f226ced10a6383ba65f01fbbba9c1e769fd7453d057d027dfca14e3fabb41e70`  
		Last Modified: Thu, 28 Jan 2021 21:58:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:130052d528820f06b656c3894131122517ca768a3631d480fe30ad0c5ff17726
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61979559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f614517de9bbe4432cf2dd955bf7b9c7c3ab8d99fe944f7ba233d58a98f67a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:47:51 GMT
ADD file:95be2cec37537b3fd70aeb1d4eb3479fc4a56b00ad7180788ddd7fa772ca65e7 in / 
# Fri, 15 Jan 2021 01:47:52 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:04:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:04:28 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:04:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:04:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:04:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:04:39 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:04:40 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:04:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:04:41 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:04:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:04:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:09:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:51:20 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:51:27 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:51:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:51:31 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:39:49 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:40:10 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:40:12 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:40:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:40:14 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:40:14 GMT
ENV COMPOSER_VERSION=2.0.9
# Thu, 28 Jan 2021 22:40:17 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:40:18 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:40:19 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:40:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:40:20 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:30d5333d20a68dd6ea3689e2c5692d7071f2d68e72c06f0b3b4c7e213df454e2`  
		Last Modified: Fri, 15 Jan 2021 01:48:29 GMT  
		Size: 2.7 MB (2710904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72077bc47778707d4c51904bf6932e44a09d9a5a37f1bac45ef59fe94bc54e1`  
		Last Modified: Fri, 15 Jan 2021 23:49:43 GMT  
		Size: 1.7 MB (1694577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bfc628cf72db6285835ff062834a15ee7c9067f6b7ccb55fad0a8bb0f292be`  
		Last Modified: Fri, 15 Jan 2021 23:49:41 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ab015e378a2ad2e4c345884006fc6b1678a0ebba44214fbc5e9dcb48ef7bb2`  
		Last Modified: Fri, 15 Jan 2021 23:49:41 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d24a448de09dec3ceb6bc305d0c17be120e79f5611f1e4054850e11526133cc8`  
		Last Modified: Fri, 15 Jan 2021 23:49:39 GMT  
		Size: 10.7 MB (10661733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8079f19e688581d52496f1937db9dc33ef25e597b149eb517633043678bd61d2`  
		Last Modified: Fri, 15 Jan 2021 23:49:39 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978c3da5ab542fa26ea4333b9b5c608d2ee68fa98cbf1e0d05df83ece9439e24`  
		Last Modified: Fri, 15 Jan 2021 23:49:45 GMT  
		Size: 14.8 MB (14764647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1043bb484cdf4818387523cb0c703d862e1c50b54ebe62f605c0d3b74837f39`  
		Last Modified: Thu, 21 Jan 2021 20:05:13 GMT  
		Size: 2.3 KB (2269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c953f678545439a3b425e1dd037e3e5d5b8092e37adb1a63cb110a0a888b5300`  
		Last Modified: Thu, 21 Jan 2021 20:05:12 GMT  
		Size: 17.6 KB (17550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f77742777349432a5c810bb823719115d594ef2d7e0d79d11fdccf49b1c298`  
		Last Modified: Thu, 28 Jan 2021 22:41:08 GMT  
		Size: 31.4 MB (31376168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20f98fa3077571418cb9ac1f3ceb60436f9c6bcda79d861d68e9c48787403d1`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 196.1 KB (196059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899d29da6e7af774384acf87f4eea2a9876f6bff3365b1486ecb6738a8e95143`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021c1a2b1a0c143edd7a90b286aadd175b31efbab95350d145d59b1b0cc1740c`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 552.8 KB (552841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0494b560b93a7d7e5bec8bd6817755005fb72e254367b206700c500a1fcd9fac`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f103a78f14a331ed6ca557b26ebf9efaf424f463cc7ef659dd83935e1863c665`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2` - linux; 386

```console
$ docker pull composer@sha256:d1366c8963cfab30a01f8eaf0c86def4785d85fcd67616b0325ad4e4e4633832
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63702654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af66081ead599dedc0d793ecd53ecd5631d90a00ce2dfb71be5d837044975ac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:38:28 GMT
ADD file:d8723c02f1eb0efa4dadc6480a753d18d7e28d9815bff96a92ff09ff55a92b11 in / 
# Fri, 15 Jan 2021 01:38:29 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 22:42:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 22:42:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 22:42:23 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 22:42:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 22:42:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 22:42:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:42:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:42:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 22:42:24 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 22:42:25 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 22:42:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 22:42:25 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 22:42:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 22:42:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 22:49:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:44:48 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:44:51 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:44:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:44:51 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:38:41 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:38:56 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:38:57 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:38:57 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:38:57 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:38:57 GMT
ENV COMPOSER_VERSION=2.0.9
# Thu, 28 Jan 2021 22:38:59 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:39:00 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:39:00 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:39:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:39:00 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9e6a151110e36daa7a487250f98425289313f856e3a586d89d82bafc1bf322c3`  
		Last Modified: Fri, 15 Jan 2021 01:39:01 GMT  
		Size: 2.8 MB (2817152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b194694eae0c8525a66d3c56796eb37a9e263d63f03eaecf6bc83d2ab3f7c9`  
		Last Modified: Fri, 15 Jan 2021 23:50:55 GMT  
		Size: 1.8 MB (1793505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a9a95dec7f2cd3bcf6903d006a870fa7113f6a974d30ec6634ab82b0a0a792`  
		Last Modified: Fri, 15 Jan 2021 23:50:52 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ad687f5cfc54121cc70af5ff69cb844177c4325a2c14efcd144cb096ecfba2`  
		Last Modified: Fri, 15 Jan 2021 23:50:54 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ae4debbbbc31db383a639e6a7df85ebf9c2f15905a9ec2df4fb8a3998dec90`  
		Last Modified: Fri, 15 Jan 2021 23:50:56 GMT  
		Size: 10.7 MB (10661677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900efcbd73b95b91ec42e946efd16fa2e312e57beba40e9aac2b0699baa90d1d`  
		Last Modified: Fri, 15 Jan 2021 23:50:51 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c042850cc5dcebe86c931da9e6014fe607a6c507fe5a61059ba47003a80cac2`  
		Last Modified: Fri, 15 Jan 2021 23:51:00 GMT  
		Size: 15.3 MB (15348857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a592432a0a1e356653687e23dd3c8f953d0fc904db0377fa898de0c851be229d`  
		Last Modified: Thu, 21 Jan 2021 19:55:39 GMT  
		Size: 2.3 KB (2270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3b6898b8d491988e64358ef661f654c98cbec8cc3e36edeedea25334aae60e`  
		Last Modified: Thu, 21 Jan 2021 19:55:40 GMT  
		Size: 17.5 KB (17525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fcd335e71480482247bfd7863baa60db887184f8227377b99d22f61dc2a4d6`  
		Last Modified: Thu, 28 Jan 2021 22:39:38 GMT  
		Size: 32.3 MB (32292342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f574926dca5384453b345a61350707cbf2753926b84e8c685a1899bbe6ff5b`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 213.8 KB (213825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25022b6f8e9b3bd588f8db12caab7e929709dcb604f7f84786e3a7d54f6bd2f4`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383490e188660eeea8b6c894366164f4300f53b351efbc251fa34ccd12a24504`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 552.8 KB (552799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7647a67da25834616edba6106817cca07fa93408500bf11d4aaa476837b4bcb1`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91eedfded7d6e258e16f2eec203d90eaa4b9de30b187ba609ee65940bf265403`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2` - linux; ppc64le

```console
$ docker pull composer@sha256:f6885d88746bfdfba04dfbaccf1d47d9e46a0130f5a0e904f581ffb380ea7403
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (64048836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc955ccd3e71ac5325e45e1cced0cff964d9c6039532c739122eb9d7fa9bc3e7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 02:41:43 GMT
ADD file:137e8f98476d5dceaeb2e8359f50eb818dee4c327e4492d16e87fb27d40aa891 in / 
# Fri, 15 Jan 2021 02:41:46 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:17:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:17:44 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:17:56 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:18:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:18:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:18:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:18:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:18:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:18:39 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:18:43 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:18:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:19:07 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:19:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:19:38 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:24:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:33:15 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:33:36 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:33:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:33:47 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:26:03 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:27:01 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:27:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:27:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:27:24 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:27:35 GMT
ENV COMPOSER_VERSION=2.0.9
# Thu, 28 Jan 2021 22:27:52 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:27:55 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:28:00 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:28:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:28:20 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cb0f06c26ffdc2117b9a3467f79e69cdf8d9c677a3c0bacabc8a694a9fe303a8`  
		Last Modified: Fri, 15 Jan 2021 02:42:19 GMT  
		Size: 2.8 MB (2812389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9a7aad5bd113c5dca33b681663b0c58f66e510017e693801a6688a9c4bab60`  
		Last Modified: Sat, 16 Jan 2021 00:14:01 GMT  
		Size: 1.7 MB (1741834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ce1d80ff72759b98cf2f5ad1efa6dd181e5f4343bb0e25cbb4ec9d5d3847f4`  
		Last Modified: Sat, 16 Jan 2021 00:14:01 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48055526d8202af50f6248db9b3cb8938cab9cfec15a1312b4c1e3782f3307c4`  
		Last Modified: Sat, 16 Jan 2021 00:14:02 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7cb5ec22b0cc763855f0481247394a6e312f8f906d232f738fc88a4219bfb1e`  
		Last Modified: Sat, 16 Jan 2021 00:13:58 GMT  
		Size: 10.7 MB (10661716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea93ae862f86d372e01dcb82dbf509e78b3f4e6533f9660f4b63c49471cb4852`  
		Last Modified: Sat, 16 Jan 2021 00:13:57 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7518496c61b651e86a2bdd79ee76e400addfddbafa26db36f7e692520aeebc1e`  
		Last Modified: Sat, 16 Jan 2021 00:14:01 GMT  
		Size: 16.1 MB (16059509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dce1a5a13b51550c7b84a60d64d364686f108d412e4776aae7d7a4922ac1ebd`  
		Last Modified: Thu, 21 Jan 2021 20:03:07 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98df2e2e9c3e105f7ddf5634cc2558ef8a2e569cd7e61121bd1f18c83a96152d`  
		Last Modified: Thu, 21 Jan 2021 20:03:07 GMT  
		Size: 17.5 KB (17538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c3ac64e0e6d2c9f92c30e69ce18c62c2ff9ba34f99a48d00be9b92ccfcf393`  
		Last Modified: Thu, 28 Jan 2021 22:30:18 GMT  
		Size: 32.0 MB (31993881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fb84ebef4906eea3269f759da0902a8097011fb84006aabbd679b5950e0970`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 204.0 KB (204039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8dba6ae992e0605a8d35408b1a00afba44b82e2b40e0fde68e8181c954ff546`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a807025eeb4eee2fa9e4b73979c81b5c1dcc0e7120dde50a1d3c99484cf82f3`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 552.9 KB (552850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a61464199f95698607ae83201de96ef6080a79661d612accc419b63ea4a42d4`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c480de546173fd553d57ceedac81c7d3a491e179672b29c93ac7bfd2619b3b74`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2` - linux; s390x

```console
$ docker pull composer@sha256:30b6319b9309316189f19f86b8b18dd6cdf31730b5d9f6293ab8e75dcda242bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61546888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13363e884d01029047438b8cf02cdbbf365c7b9df0b95e49e6802a98df33bfde`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:51:34 GMT
ADD file:3ba807ca8ed73ca14224dd26a883f2399031fa32430f035cc5ae97b5e6db0ca7 in / 
# Fri, 15 Jan 2021 01:51:35 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 22:57:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 22:57:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 22:57:13 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 22:57:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 22:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 22:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:57:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:57:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 22:57:17 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 22:57:17 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 22:57:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 22:57:18 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 22:57:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 22:57:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:02:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:54:10 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:54:13 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:54:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:54:14 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:42:35 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:42:53 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:42:54 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:42:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:42:54 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:42:55 GMT
ENV COMPOSER_VERSION=2.0.9
# Thu, 28 Jan 2021 22:42:57 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:42:57 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:42:58 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:42:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:42:59 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:3997176601fb5d5ac06922718668ede4acac00a5c0daef8a9099fd76ce93047f`  
		Last Modified: Fri, 15 Jan 2021 01:52:40 GMT  
		Size: 2.6 MB (2601720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497e79d9095f9ba4812f1150c33ad07d399f559fea8e3c4fe8553e02f2cf8b6a`  
		Last Modified: Fri, 15 Jan 2021 23:39:10 GMT  
		Size: 1.8 MB (1756352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99527660904ffc5aed1d27bb86166f189e04b5df76d7becf74efffb1836eaf5e`  
		Last Modified: Fri, 15 Jan 2021 23:39:10 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9b51111e1ef5a5156e505d6369bb2d4e21354a1203636fca6f26de34df9c15`  
		Last Modified: Fri, 15 Jan 2021 23:39:10 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3c721a3fef9acf0bac166c45ff18e2485752ef7b86447284b7b710646d40df`  
		Last Modified: Fri, 15 Jan 2021 23:38:47 GMT  
		Size: 10.7 MB (10661723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e676c2ca01980f72daf35a53dae36e4fe10945de76af81d54618066f5204c598`  
		Last Modified: Fri, 15 Jan 2021 23:38:48 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90c350aff0df72bb91eaa20306afe2218ac1d50242eb213d4e481f65b2a9f60`  
		Last Modified: Fri, 15 Jan 2021 23:38:48 GMT  
		Size: 14.4 MB (14364644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c91dec7c10d367e01e4907cb6c2d00b3e5b7390545c8c9499eaac3c35986507`  
		Last Modified: Thu, 21 Jan 2021 20:05:24 GMT  
		Size: 2.3 KB (2269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63e510378e653ab6ff71c58fc15e869877848171131d614af01c250d7a36e31`  
		Last Modified: Thu, 21 Jan 2021 20:05:20 GMT  
		Size: 17.5 KB (17541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4079b673c2155f6fc765bd4b8d683a2326dd552affe882edccb45c657534ed18`  
		Last Modified: Thu, 28 Jan 2021 22:43:28 GMT  
		Size: 31.4 MB (31389182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdeafc632059b12ff488232684da09d9c34de98941c5f6ff69c471274af7602`  
		Last Modified: Thu, 28 Jan 2021 22:43:22 GMT  
		Size: 197.8 KB (197815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f475e4a4966b8ce4d7561e4c7a2e4961201d5b118193c3525421174abaaa14e5`  
		Last Modified: Thu, 28 Jan 2021 22:43:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0527c47a0591fb1d627eb0553a148074dc26b3e929f17fe11c70beb29ddc697e`  
		Last Modified: Thu, 28 Jan 2021 22:43:21 GMT  
		Size: 552.8 KB (552833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20581df10571ef1589ab514908ef57a5508e11f388e2022afb5678afc09bdcdb`  
		Last Modified: Thu, 28 Jan 2021 22:43:21 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d915abaf68a0c69e745c6fa8e076f421f760e793935af4022615f2460c3f7cb`  
		Last Modified: Thu, 28 Jan 2021 22:43:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `composer:2.0`

```console
$ docker pull composer@sha256:f8dfdbaac5983fe7698848442d1d0a39753ef72715391bdbd4553d0b2636020d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `composer:2.0` - linux; amd64

```console
$ docker pull composer@sha256:005d4a50002fcf58eb93b749345b73441cb615644f0790844538d0990cc3ce20
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62417362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e0bd4ead1c9c98e491c19a4b10307760a1a5060996f40e5f5229bd6882b578`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 02:23:51 GMT
ADD file:edbe213ae0c825a5bfbe569928cf20f683f334f93a093ccd0a3a014b7428e760 in / 
# Fri, 15 Jan 2021 02:23:51 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:43:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:43:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:43:26 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:43:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:43:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:43:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:43:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:43:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:43:30 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:43:30 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:43:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:43:31 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:43:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:43:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:51:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 20:17:47 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 20:17:50 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 20:17:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 20:17:51 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:32:03 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:32:24 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:32:24 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:32:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:32:25 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:32:25 GMT
ENV COMPOSER_VERSION=2.0.9
# Thu, 28 Jan 2021 22:32:27 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:32:27 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:32:28 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:32:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:32:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:596ba82af5aaa3e2fd9d6f955b8b94f0744a2b60710e3c243ba3e4a467f051d1`  
		Last Modified: Fri, 15 Jan 2021 02:08:10 GMT  
		Size: 2.8 MB (2810825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af74f285bb27c6623f2b5c8c3a2e487603c7dd5c51859fd6e13859542f4310c3`  
		Last Modified: Sat, 16 Jan 2021 01:00:24 GMT  
		Size: 1.7 MB (1694838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab8440e5667ccb2ffd4e62ed905a106742dfdd7dd3167d9d64b4bdeed8a4945`  
		Last Modified: Sat, 16 Jan 2021 01:00:20 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64889fa545ec919e6fe392c368b8cb41a10e7834c1ba4d4d96fd9ee2e3405cc1`  
		Last Modified: Sat, 16 Jan 2021 01:00:20 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94168e6487351b04d28db6aabb22e0c68ad3582533cf8d7e00322078720f8081`  
		Last Modified: Sat, 16 Jan 2021 01:00:19 GMT  
		Size: 10.7 MB (10661716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3898f14298ef25ab2005e9025a88f553003a83a1b6a61765e93d78879441aa36`  
		Last Modified: Sat, 16 Jan 2021 01:00:18 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3747e5f21671eba796a4b76a6abc180c60b0ef9414e9a80b325b31aeaa1f6ca`  
		Last Modified: Sat, 16 Jan 2021 01:00:21 GMT  
		Size: 15.3 MB (15318011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3df0f8088890764041d8dbfe574cd5bdf020400801b0b108cd6b7f965aab3a`  
		Last Modified: Thu, 21 Jan 2021 20:28:34 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f6ddeaf0bdcf495df2e7c8d72852796c1bae3d9f8ef8260058fdb43b995163`  
		Last Modified: Thu, 21 Jan 2021 20:28:34 GMT  
		Size: 17.5 KB (17539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29338fcaf9eb090ba02397a08616210ac758731039ac2d2a5db97288090a1845`  
		Last Modified: Thu, 28 Jan 2021 22:32:55 GMT  
		Size: 31.2 MB (31158400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a0bf379d52ae6a08ffd2313828e5738aa1cfd2a934c2403e6065ae7f94ba05`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 198.3 KB (198274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a346beb5e7dfc07424d1d661858912a89fab48a63bd89492e0c97c3cf1a6c75`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e86daf479799f96a49bc265571da38b2be4344f28a6b8ed4a0a18cb1dafae08`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 552.8 KB (552794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048afd2f48877072346dfbc095e6883b2ccc828164f17723d6e95d230c798b83`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad27987395f1263b907d761fc5f4b5a356869262f62cd2b055f7c8bb050317ac`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 90.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.0` - linux; arm variant v6

```console
$ docker pull composer@sha256:8555fcdcc559af5253afc8400e8f2f92937211b20947c2b1d231b3ab2a703663
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58265639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d766a7469442cfbfeb325a177218e32152d532c8efaec2dd15a2fd56020467`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 28 Jan 2021 23:49:59 GMT
ADD file:c197324e4979e2a7b257ad683d20dd9cbdae525a076bd68fe6aa0e0b126875df in / 
# Thu, 28 Jan 2021 23:49:59 GMT
CMD ["/bin/sh"]
# Fri, 29 Jan 2021 00:33:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 29 Jan 2021 00:33:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 29 Jan 2021 00:33:59 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 29 Jan 2021 00:34:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 29 Jan 2021 00:34:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 29 Jan 2021 00:34:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 29 Jan 2021 00:34:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 29 Jan 2021 00:34:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 29 Jan 2021 00:34:08 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 29 Jan 2021 00:34:11 GMT
ENV PHP_VERSION=8.0.1
# Fri, 29 Jan 2021 00:34:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 29 Jan 2021 00:34:13 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 29 Jan 2021 00:34:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 29 Jan 2021 00:34:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 29 Jan 2021 00:37:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 29 Jan 2021 00:37:35 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 29 Jan 2021 00:37:38 GMT
RUN docker-php-ext-enable sodium
# Fri, 29 Jan 2021 00:37:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 29 Jan 2021 00:37:40 GMT
CMD ["php" "-a"]
# Fri, 29 Jan 2021 02:11:29 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 29 Jan 2021 02:11:49 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 29 Jan 2021 02:11:51 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 29 Jan 2021 02:11:51 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 29 Jan 2021 02:11:52 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 29 Jan 2021 02:11:52 GMT
ENV COMPOSER_VERSION=2.0.9
# Fri, 29 Jan 2021 02:11:55 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 29 Jan 2021 02:11:56 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 29 Jan 2021 02:11:57 GMT
WORKDIR /app
# Fri, 29 Jan 2021 02:11:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 29 Jan 2021 02:11:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a66f440da051140fefcb0a520bdeb69d763b1eb4fd1b2ed46b4c0a168e335108`  
		Last Modified: Thu, 28 Jan 2021 23:50:33 GMT  
		Size: 2.6 MB (2621759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa34846effbef1e901021c65a67535efc29a1aa39b259a4c29559d1439f4131`  
		Last Modified: Fri, 29 Jan 2021 01:05:52 GMT  
		Size: 1.7 MB (1684855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba088c5e0e1fb4c64a8b59354bedcae82636c10a93fe3790125bec5c1e841299`  
		Last Modified: Fri, 29 Jan 2021 01:05:51 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b10584422ada7d37ac091eae04bcee5df4cee5b93cd86068ce55c7ab085ae62`  
		Last Modified: Fri, 29 Jan 2021 01:05:51 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd2125b643842a0b1fb7799c57d504cb3ea72f1cdaac6d48b6d3ee2fa033d39`  
		Last Modified: Fri, 29 Jan 2021 01:05:50 GMT  
		Size: 10.7 MB (10661723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370c8d7d436fffa9dd306db82b4a90f7b25ae1d68c658dac4c195ec6a921976e`  
		Last Modified: Fri, 29 Jan 2021 01:05:49 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c1bd9522799773adb723d78cef494168d851dd759ef42bdf230e3518c9888d`  
		Last Modified: Fri, 29 Jan 2021 01:05:54 GMT  
		Size: 13.6 MB (13571709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60b70fa5215a21be024094dd917f70d206590186d21137fcb75d1fb68a887a2`  
		Last Modified: Fri, 29 Jan 2021 01:05:49 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733b25bcaba65cbff9b151c9ab65d005350d890d7728bfe14024f5f4bd9ca890`  
		Last Modified: Fri, 29 Jan 2021 01:05:49 GMT  
		Size: 17.5 KB (17531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dda7886eea28b54dfe2eea50537d02027bbbcda31bb0d081dff700b99290584`  
		Last Modified: Fri, 29 Jan 2021 02:12:41 GMT  
		Size: 29.0 MB (28956651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90907b51293338df699b9f07cbb70441610fa8f2924e32d21967026449fe4064`  
		Last Modified: Fri, 29 Jan 2021 02:12:28 GMT  
		Size: 193.5 KB (193490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85552216f6bbc21bc776e9622f10a51b96b9a92310894072d91339b4fe625b1e`  
		Last Modified: Fri, 29 Jan 2021 02:12:28 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277406688472a6794691f5e4a67b9a1fff148488bd3592f46c1ff32c50b9e712`  
		Last Modified: Fri, 29 Jan 2021 02:12:28 GMT  
		Size: 552.8 KB (552840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31adf754bdf3aa207b3395bac818c602ae3326449c8eef1d435c2deefb3a2dd0`  
		Last Modified: Fri, 29 Jan 2021 02:12:29 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d326c954a1dde2641329fe23cd34f82ea22e784961b8e5e3098ea38e58e06bf`  
		Last Modified: Fri, 29 Jan 2021 02:12:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.0` - linux; arm variant v7

```console
$ docker pull composer@sha256:269f67fe496ec79ec849b998dff19dd47f34368253361860e8c85cdc3fe60289
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56107193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929093143b6d7781fa9c2240f279fcb895b68e0ff527e64b6cd13779c07c5f9d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:58:27 GMT
ADD file:718d7c24a8d6ff0feb2843cf8c3ca4b7ef1fb523a45dea568404259a7b4e6f10 in / 
# Fri, 15 Jan 2021 01:58:29 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:04:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:04:05 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:04:07 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:04:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:04:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:04:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:04:13 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:04:14 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:04:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:04:15 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:04:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:04:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:07:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:10:13 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:10:16 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:10:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:10:18 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 21:57:49 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 21:58:13 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 21:58:15 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 21:58:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 21:58:17 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 21:58:17 GMT
ENV COMPOSER_VERSION=2.0.9
# Thu, 28 Jan 2021 21:58:21 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 21:58:21 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 21:58:22 GMT
WORKDIR /app
# Thu, 28 Jan 2021 21:58:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 21:58:24 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:0f34ce5da94097b8c334f6b2065a010aced9855c3532e4462e9bd1b0a4c4b3f6`  
		Last Modified: Fri, 15 Jan 2021 01:59:13 GMT  
		Size: 2.4 MB (2422744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cecec77a7b5b50913bcb9f7bfe0c5fdcebb948b947747285290197c13902be91`  
		Last Modified: Fri, 15 Jan 2021 23:42:36 GMT  
		Size: 1.6 MB (1555130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0496082b3c55009a50b47ce80bf27dd7451aaa7e13b5b4ccbe886a780c614dd1`  
		Last Modified: Fri, 15 Jan 2021 23:42:33 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af351861d88fff830659b71d51e45b8e623d31cb86c764fab107e6c39ca5a717`  
		Last Modified: Fri, 15 Jan 2021 23:42:33 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11aa9107e62f7893b45936388317768641833b4f6b1937989fcbfc5845e1c698`  
		Last Modified: Fri, 15 Jan 2021 23:42:32 GMT  
		Size: 10.7 MB (10661711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739d880e478996d44b501dcc056bf9f5f25909c929d579ba0c02f123be170522`  
		Last Modified: Fri, 15 Jan 2021 23:42:30 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed2a0f0dbdad0b49284a158baa86126c2b2a794ee53b82c4181378520555f1d`  
		Last Modified: Fri, 15 Jan 2021 23:42:36 GMT  
		Size: 13.1 MB (13070133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b9ed4df09ec14031c338ad506ba7fcc76ab6a07fc32432ad75d94867ae04d9`  
		Last Modified: Thu, 21 Jan 2021 19:23:58 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500dd1602efbacb91e481ac3e868dadb7bca74fb6b4f73d41fb2ec82cab72f22`  
		Last Modified: Thu, 21 Jan 2021 19:23:59 GMT  
		Size: 17.5 KB (17536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b52f140a609f714bafc66c167ec2b6c04c8962153f406e1ac18bac7b669c61`  
		Last Modified: Thu, 28 Jan 2021 21:59:15 GMT  
		Size: 27.6 MB (27635729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cb9e5e751c90392752772de98a302d52a12f4ea2dcf08223098a5cb41c1fd4`  
		Last Modified: Thu, 28 Jan 2021 21:58:57 GMT  
		Size: 186.3 KB (186294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964a5881822f5f5e182f7b8d8fef32582177380aff1c392f68c3c5f908be31d4`  
		Last Modified: Thu, 28 Jan 2021 21:58:57 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174e82ce233fe45d2052d89f8f6ceb309742ffa529fff02fe0a3bf4f0dc2680e`  
		Last Modified: Thu, 28 Jan 2021 21:58:58 GMT  
		Size: 552.8 KB (552840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea9421b9b2b639e1f21013f53e1e2cb09a3ec7f0dd823ee954f9244314cf5f8`  
		Last Modified: Thu, 28 Jan 2021 21:58:57 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f226ced10a6383ba65f01fbbba9c1e769fd7453d057d027dfca14e3fabb41e70`  
		Last Modified: Thu, 28 Jan 2021 21:58:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.0` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:130052d528820f06b656c3894131122517ca768a3631d480fe30ad0c5ff17726
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61979559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f614517de9bbe4432cf2dd955bf7b9c7c3ab8d99fe944f7ba233d58a98f67a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:47:51 GMT
ADD file:95be2cec37537b3fd70aeb1d4eb3479fc4a56b00ad7180788ddd7fa772ca65e7 in / 
# Fri, 15 Jan 2021 01:47:52 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:04:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:04:28 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:04:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:04:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:04:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:04:39 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:04:40 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:04:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:04:41 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:04:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:04:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:09:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:51:20 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:51:27 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:51:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:51:31 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:39:49 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:40:10 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:40:12 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:40:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:40:14 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:40:14 GMT
ENV COMPOSER_VERSION=2.0.9
# Thu, 28 Jan 2021 22:40:17 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:40:18 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:40:19 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:40:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:40:20 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:30d5333d20a68dd6ea3689e2c5692d7071f2d68e72c06f0b3b4c7e213df454e2`  
		Last Modified: Fri, 15 Jan 2021 01:48:29 GMT  
		Size: 2.7 MB (2710904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72077bc47778707d4c51904bf6932e44a09d9a5a37f1bac45ef59fe94bc54e1`  
		Last Modified: Fri, 15 Jan 2021 23:49:43 GMT  
		Size: 1.7 MB (1694577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bfc628cf72db6285835ff062834a15ee7c9067f6b7ccb55fad0a8bb0f292be`  
		Last Modified: Fri, 15 Jan 2021 23:49:41 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ab015e378a2ad2e4c345884006fc6b1678a0ebba44214fbc5e9dcb48ef7bb2`  
		Last Modified: Fri, 15 Jan 2021 23:49:41 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d24a448de09dec3ceb6bc305d0c17be120e79f5611f1e4054850e11526133cc8`  
		Last Modified: Fri, 15 Jan 2021 23:49:39 GMT  
		Size: 10.7 MB (10661733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8079f19e688581d52496f1937db9dc33ef25e597b149eb517633043678bd61d2`  
		Last Modified: Fri, 15 Jan 2021 23:49:39 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978c3da5ab542fa26ea4333b9b5c608d2ee68fa98cbf1e0d05df83ece9439e24`  
		Last Modified: Fri, 15 Jan 2021 23:49:45 GMT  
		Size: 14.8 MB (14764647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1043bb484cdf4818387523cb0c703d862e1c50b54ebe62f605c0d3b74837f39`  
		Last Modified: Thu, 21 Jan 2021 20:05:13 GMT  
		Size: 2.3 KB (2269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c953f678545439a3b425e1dd037e3e5d5b8092e37adb1a63cb110a0a888b5300`  
		Last Modified: Thu, 21 Jan 2021 20:05:12 GMT  
		Size: 17.6 KB (17550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f77742777349432a5c810bb823719115d594ef2d7e0d79d11fdccf49b1c298`  
		Last Modified: Thu, 28 Jan 2021 22:41:08 GMT  
		Size: 31.4 MB (31376168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20f98fa3077571418cb9ac1f3ceb60436f9c6bcda79d861d68e9c48787403d1`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 196.1 KB (196059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899d29da6e7af774384acf87f4eea2a9876f6bff3365b1486ecb6738a8e95143`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021c1a2b1a0c143edd7a90b286aadd175b31efbab95350d145d59b1b0cc1740c`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 552.8 KB (552841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0494b560b93a7d7e5bec8bd6817755005fb72e254367b206700c500a1fcd9fac`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f103a78f14a331ed6ca557b26ebf9efaf424f463cc7ef659dd83935e1863c665`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.0` - linux; 386

```console
$ docker pull composer@sha256:d1366c8963cfab30a01f8eaf0c86def4785d85fcd67616b0325ad4e4e4633832
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63702654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af66081ead599dedc0d793ecd53ecd5631d90a00ce2dfb71be5d837044975ac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:38:28 GMT
ADD file:d8723c02f1eb0efa4dadc6480a753d18d7e28d9815bff96a92ff09ff55a92b11 in / 
# Fri, 15 Jan 2021 01:38:29 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 22:42:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 22:42:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 22:42:23 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 22:42:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 22:42:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 22:42:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:42:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:42:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 22:42:24 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 22:42:25 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 22:42:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 22:42:25 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 22:42:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 22:42:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 22:49:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:44:48 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:44:51 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:44:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:44:51 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:38:41 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:38:56 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:38:57 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:38:57 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:38:57 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:38:57 GMT
ENV COMPOSER_VERSION=2.0.9
# Thu, 28 Jan 2021 22:38:59 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:39:00 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:39:00 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:39:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:39:00 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9e6a151110e36daa7a487250f98425289313f856e3a586d89d82bafc1bf322c3`  
		Last Modified: Fri, 15 Jan 2021 01:39:01 GMT  
		Size: 2.8 MB (2817152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b194694eae0c8525a66d3c56796eb37a9e263d63f03eaecf6bc83d2ab3f7c9`  
		Last Modified: Fri, 15 Jan 2021 23:50:55 GMT  
		Size: 1.8 MB (1793505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a9a95dec7f2cd3bcf6903d006a870fa7113f6a974d30ec6634ab82b0a0a792`  
		Last Modified: Fri, 15 Jan 2021 23:50:52 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ad687f5cfc54121cc70af5ff69cb844177c4325a2c14efcd144cb096ecfba2`  
		Last Modified: Fri, 15 Jan 2021 23:50:54 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ae4debbbbc31db383a639e6a7df85ebf9c2f15905a9ec2df4fb8a3998dec90`  
		Last Modified: Fri, 15 Jan 2021 23:50:56 GMT  
		Size: 10.7 MB (10661677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900efcbd73b95b91ec42e946efd16fa2e312e57beba40e9aac2b0699baa90d1d`  
		Last Modified: Fri, 15 Jan 2021 23:50:51 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c042850cc5dcebe86c931da9e6014fe607a6c507fe5a61059ba47003a80cac2`  
		Last Modified: Fri, 15 Jan 2021 23:51:00 GMT  
		Size: 15.3 MB (15348857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a592432a0a1e356653687e23dd3c8f953d0fc904db0377fa898de0c851be229d`  
		Last Modified: Thu, 21 Jan 2021 19:55:39 GMT  
		Size: 2.3 KB (2270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3b6898b8d491988e64358ef661f654c98cbec8cc3e36edeedea25334aae60e`  
		Last Modified: Thu, 21 Jan 2021 19:55:40 GMT  
		Size: 17.5 KB (17525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fcd335e71480482247bfd7863baa60db887184f8227377b99d22f61dc2a4d6`  
		Last Modified: Thu, 28 Jan 2021 22:39:38 GMT  
		Size: 32.3 MB (32292342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f574926dca5384453b345a61350707cbf2753926b84e8c685a1899bbe6ff5b`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 213.8 KB (213825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25022b6f8e9b3bd588f8db12caab7e929709dcb604f7f84786e3a7d54f6bd2f4`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383490e188660eeea8b6c894366164f4300f53b351efbc251fa34ccd12a24504`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 552.8 KB (552799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7647a67da25834616edba6106817cca07fa93408500bf11d4aaa476837b4bcb1`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91eedfded7d6e258e16f2eec203d90eaa4b9de30b187ba609ee65940bf265403`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.0` - linux; ppc64le

```console
$ docker pull composer@sha256:f6885d88746bfdfba04dfbaccf1d47d9e46a0130f5a0e904f581ffb380ea7403
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (64048836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc955ccd3e71ac5325e45e1cced0cff964d9c6039532c739122eb9d7fa9bc3e7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 02:41:43 GMT
ADD file:137e8f98476d5dceaeb2e8359f50eb818dee4c327e4492d16e87fb27d40aa891 in / 
# Fri, 15 Jan 2021 02:41:46 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:17:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:17:44 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:17:56 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:18:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:18:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:18:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:18:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:18:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:18:39 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:18:43 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:18:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:19:07 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:19:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:19:38 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:24:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:33:15 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:33:36 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:33:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:33:47 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:26:03 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:27:01 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:27:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:27:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:27:24 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:27:35 GMT
ENV COMPOSER_VERSION=2.0.9
# Thu, 28 Jan 2021 22:27:52 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:27:55 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:28:00 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:28:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:28:20 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cb0f06c26ffdc2117b9a3467f79e69cdf8d9c677a3c0bacabc8a694a9fe303a8`  
		Last Modified: Fri, 15 Jan 2021 02:42:19 GMT  
		Size: 2.8 MB (2812389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9a7aad5bd113c5dca33b681663b0c58f66e510017e693801a6688a9c4bab60`  
		Last Modified: Sat, 16 Jan 2021 00:14:01 GMT  
		Size: 1.7 MB (1741834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ce1d80ff72759b98cf2f5ad1efa6dd181e5f4343bb0e25cbb4ec9d5d3847f4`  
		Last Modified: Sat, 16 Jan 2021 00:14:01 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48055526d8202af50f6248db9b3cb8938cab9cfec15a1312b4c1e3782f3307c4`  
		Last Modified: Sat, 16 Jan 2021 00:14:02 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7cb5ec22b0cc763855f0481247394a6e312f8f906d232f738fc88a4219bfb1e`  
		Last Modified: Sat, 16 Jan 2021 00:13:58 GMT  
		Size: 10.7 MB (10661716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea93ae862f86d372e01dcb82dbf509e78b3f4e6533f9660f4b63c49471cb4852`  
		Last Modified: Sat, 16 Jan 2021 00:13:57 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7518496c61b651e86a2bdd79ee76e400addfddbafa26db36f7e692520aeebc1e`  
		Last Modified: Sat, 16 Jan 2021 00:14:01 GMT  
		Size: 16.1 MB (16059509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dce1a5a13b51550c7b84a60d64d364686f108d412e4776aae7d7a4922ac1ebd`  
		Last Modified: Thu, 21 Jan 2021 20:03:07 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98df2e2e9c3e105f7ddf5634cc2558ef8a2e569cd7e61121bd1f18c83a96152d`  
		Last Modified: Thu, 21 Jan 2021 20:03:07 GMT  
		Size: 17.5 KB (17538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c3ac64e0e6d2c9f92c30e69ce18c62c2ff9ba34f99a48d00be9b92ccfcf393`  
		Last Modified: Thu, 28 Jan 2021 22:30:18 GMT  
		Size: 32.0 MB (31993881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fb84ebef4906eea3269f759da0902a8097011fb84006aabbd679b5950e0970`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 204.0 KB (204039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8dba6ae992e0605a8d35408b1a00afba44b82e2b40e0fde68e8181c954ff546`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a807025eeb4eee2fa9e4b73979c81b5c1dcc0e7120dde50a1d3c99484cf82f3`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 552.9 KB (552850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a61464199f95698607ae83201de96ef6080a79661d612accc419b63ea4a42d4`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c480de546173fd553d57ceedac81c7d3a491e179672b29c93ac7bfd2619b3b74`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.0` - linux; s390x

```console
$ docker pull composer@sha256:30b6319b9309316189f19f86b8b18dd6cdf31730b5d9f6293ab8e75dcda242bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61546888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13363e884d01029047438b8cf02cdbbf365c7b9df0b95e49e6802a98df33bfde`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:51:34 GMT
ADD file:3ba807ca8ed73ca14224dd26a883f2399031fa32430f035cc5ae97b5e6db0ca7 in / 
# Fri, 15 Jan 2021 01:51:35 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 22:57:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 22:57:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 22:57:13 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 22:57:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 22:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 22:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:57:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:57:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 22:57:17 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 22:57:17 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 22:57:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 22:57:18 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 22:57:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 22:57:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:02:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:54:10 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:54:13 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:54:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:54:14 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:42:35 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:42:53 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:42:54 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:42:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:42:54 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:42:55 GMT
ENV COMPOSER_VERSION=2.0.9
# Thu, 28 Jan 2021 22:42:57 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:42:57 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:42:58 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:42:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:42:59 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:3997176601fb5d5ac06922718668ede4acac00a5c0daef8a9099fd76ce93047f`  
		Last Modified: Fri, 15 Jan 2021 01:52:40 GMT  
		Size: 2.6 MB (2601720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497e79d9095f9ba4812f1150c33ad07d399f559fea8e3c4fe8553e02f2cf8b6a`  
		Last Modified: Fri, 15 Jan 2021 23:39:10 GMT  
		Size: 1.8 MB (1756352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99527660904ffc5aed1d27bb86166f189e04b5df76d7becf74efffb1836eaf5e`  
		Last Modified: Fri, 15 Jan 2021 23:39:10 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9b51111e1ef5a5156e505d6369bb2d4e21354a1203636fca6f26de34df9c15`  
		Last Modified: Fri, 15 Jan 2021 23:39:10 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3c721a3fef9acf0bac166c45ff18e2485752ef7b86447284b7b710646d40df`  
		Last Modified: Fri, 15 Jan 2021 23:38:47 GMT  
		Size: 10.7 MB (10661723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e676c2ca01980f72daf35a53dae36e4fe10945de76af81d54618066f5204c598`  
		Last Modified: Fri, 15 Jan 2021 23:38:48 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90c350aff0df72bb91eaa20306afe2218ac1d50242eb213d4e481f65b2a9f60`  
		Last Modified: Fri, 15 Jan 2021 23:38:48 GMT  
		Size: 14.4 MB (14364644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c91dec7c10d367e01e4907cb6c2d00b3e5b7390545c8c9499eaac3c35986507`  
		Last Modified: Thu, 21 Jan 2021 20:05:24 GMT  
		Size: 2.3 KB (2269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63e510378e653ab6ff71c58fc15e869877848171131d614af01c250d7a36e31`  
		Last Modified: Thu, 21 Jan 2021 20:05:20 GMT  
		Size: 17.5 KB (17541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4079b673c2155f6fc765bd4b8d683a2326dd552affe882edccb45c657534ed18`  
		Last Modified: Thu, 28 Jan 2021 22:43:28 GMT  
		Size: 31.4 MB (31389182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdeafc632059b12ff488232684da09d9c34de98941c5f6ff69c471274af7602`  
		Last Modified: Thu, 28 Jan 2021 22:43:22 GMT  
		Size: 197.8 KB (197815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f475e4a4966b8ce4d7561e4c7a2e4961201d5b118193c3525421174abaaa14e5`  
		Last Modified: Thu, 28 Jan 2021 22:43:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0527c47a0591fb1d627eb0553a148074dc26b3e929f17fe11c70beb29ddc697e`  
		Last Modified: Thu, 28 Jan 2021 22:43:21 GMT  
		Size: 552.8 KB (552833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20581df10571ef1589ab514908ef57a5508e11f388e2022afb5678afc09bdcdb`  
		Last Modified: Thu, 28 Jan 2021 22:43:21 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d915abaf68a0c69e745c6fa8e076f421f760e793935af4022615f2460c3f7cb`  
		Last Modified: Thu, 28 Jan 2021 22:43:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `composer:2.0.9`

```console
$ docker pull composer@sha256:f8dfdbaac5983fe7698848442d1d0a39753ef72715391bdbd4553d0b2636020d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `composer:2.0.9` - linux; amd64

```console
$ docker pull composer@sha256:005d4a50002fcf58eb93b749345b73441cb615644f0790844538d0990cc3ce20
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62417362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e0bd4ead1c9c98e491c19a4b10307760a1a5060996f40e5f5229bd6882b578`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 02:23:51 GMT
ADD file:edbe213ae0c825a5bfbe569928cf20f683f334f93a093ccd0a3a014b7428e760 in / 
# Fri, 15 Jan 2021 02:23:51 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:43:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:43:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:43:26 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:43:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:43:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:43:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:43:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:43:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:43:30 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:43:30 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:43:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:43:31 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:43:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:43:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:51:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 20:17:47 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 20:17:50 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 20:17:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 20:17:51 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:32:03 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:32:24 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:32:24 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:32:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:32:25 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:32:25 GMT
ENV COMPOSER_VERSION=2.0.9
# Thu, 28 Jan 2021 22:32:27 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:32:27 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:32:28 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:32:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:32:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:596ba82af5aaa3e2fd9d6f955b8b94f0744a2b60710e3c243ba3e4a467f051d1`  
		Last Modified: Fri, 15 Jan 2021 02:08:10 GMT  
		Size: 2.8 MB (2810825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af74f285bb27c6623f2b5c8c3a2e487603c7dd5c51859fd6e13859542f4310c3`  
		Last Modified: Sat, 16 Jan 2021 01:00:24 GMT  
		Size: 1.7 MB (1694838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab8440e5667ccb2ffd4e62ed905a106742dfdd7dd3167d9d64b4bdeed8a4945`  
		Last Modified: Sat, 16 Jan 2021 01:00:20 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64889fa545ec919e6fe392c368b8cb41a10e7834c1ba4d4d96fd9ee2e3405cc1`  
		Last Modified: Sat, 16 Jan 2021 01:00:20 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94168e6487351b04d28db6aabb22e0c68ad3582533cf8d7e00322078720f8081`  
		Last Modified: Sat, 16 Jan 2021 01:00:19 GMT  
		Size: 10.7 MB (10661716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3898f14298ef25ab2005e9025a88f553003a83a1b6a61765e93d78879441aa36`  
		Last Modified: Sat, 16 Jan 2021 01:00:18 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3747e5f21671eba796a4b76a6abc180c60b0ef9414e9a80b325b31aeaa1f6ca`  
		Last Modified: Sat, 16 Jan 2021 01:00:21 GMT  
		Size: 15.3 MB (15318011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3df0f8088890764041d8dbfe574cd5bdf020400801b0b108cd6b7f965aab3a`  
		Last Modified: Thu, 21 Jan 2021 20:28:34 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f6ddeaf0bdcf495df2e7c8d72852796c1bae3d9f8ef8260058fdb43b995163`  
		Last Modified: Thu, 21 Jan 2021 20:28:34 GMT  
		Size: 17.5 KB (17539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29338fcaf9eb090ba02397a08616210ac758731039ac2d2a5db97288090a1845`  
		Last Modified: Thu, 28 Jan 2021 22:32:55 GMT  
		Size: 31.2 MB (31158400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a0bf379d52ae6a08ffd2313828e5738aa1cfd2a934c2403e6065ae7f94ba05`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 198.3 KB (198274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a346beb5e7dfc07424d1d661858912a89fab48a63bd89492e0c97c3cf1a6c75`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e86daf479799f96a49bc265571da38b2be4344f28a6b8ed4a0a18cb1dafae08`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 552.8 KB (552794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048afd2f48877072346dfbc095e6883b2ccc828164f17723d6e95d230c798b83`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad27987395f1263b907d761fc5f4b5a356869262f62cd2b055f7c8bb050317ac`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 90.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.0.9` - linux; arm variant v6

```console
$ docker pull composer@sha256:8555fcdcc559af5253afc8400e8f2f92937211b20947c2b1d231b3ab2a703663
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58265639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d766a7469442cfbfeb325a177218e32152d532c8efaec2dd15a2fd56020467`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 28 Jan 2021 23:49:59 GMT
ADD file:c197324e4979e2a7b257ad683d20dd9cbdae525a076bd68fe6aa0e0b126875df in / 
# Thu, 28 Jan 2021 23:49:59 GMT
CMD ["/bin/sh"]
# Fri, 29 Jan 2021 00:33:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 29 Jan 2021 00:33:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 29 Jan 2021 00:33:59 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 29 Jan 2021 00:34:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 29 Jan 2021 00:34:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 29 Jan 2021 00:34:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 29 Jan 2021 00:34:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 29 Jan 2021 00:34:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 29 Jan 2021 00:34:08 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 29 Jan 2021 00:34:11 GMT
ENV PHP_VERSION=8.0.1
# Fri, 29 Jan 2021 00:34:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 29 Jan 2021 00:34:13 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 29 Jan 2021 00:34:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 29 Jan 2021 00:34:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 29 Jan 2021 00:37:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 29 Jan 2021 00:37:35 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 29 Jan 2021 00:37:38 GMT
RUN docker-php-ext-enable sodium
# Fri, 29 Jan 2021 00:37:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 29 Jan 2021 00:37:40 GMT
CMD ["php" "-a"]
# Fri, 29 Jan 2021 02:11:29 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 29 Jan 2021 02:11:49 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 29 Jan 2021 02:11:51 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 29 Jan 2021 02:11:51 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 29 Jan 2021 02:11:52 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 29 Jan 2021 02:11:52 GMT
ENV COMPOSER_VERSION=2.0.9
# Fri, 29 Jan 2021 02:11:55 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 29 Jan 2021 02:11:56 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 29 Jan 2021 02:11:57 GMT
WORKDIR /app
# Fri, 29 Jan 2021 02:11:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 29 Jan 2021 02:11:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a66f440da051140fefcb0a520bdeb69d763b1eb4fd1b2ed46b4c0a168e335108`  
		Last Modified: Thu, 28 Jan 2021 23:50:33 GMT  
		Size: 2.6 MB (2621759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa34846effbef1e901021c65a67535efc29a1aa39b259a4c29559d1439f4131`  
		Last Modified: Fri, 29 Jan 2021 01:05:52 GMT  
		Size: 1.7 MB (1684855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba088c5e0e1fb4c64a8b59354bedcae82636c10a93fe3790125bec5c1e841299`  
		Last Modified: Fri, 29 Jan 2021 01:05:51 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b10584422ada7d37ac091eae04bcee5df4cee5b93cd86068ce55c7ab085ae62`  
		Last Modified: Fri, 29 Jan 2021 01:05:51 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd2125b643842a0b1fb7799c57d504cb3ea72f1cdaac6d48b6d3ee2fa033d39`  
		Last Modified: Fri, 29 Jan 2021 01:05:50 GMT  
		Size: 10.7 MB (10661723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370c8d7d436fffa9dd306db82b4a90f7b25ae1d68c658dac4c195ec6a921976e`  
		Last Modified: Fri, 29 Jan 2021 01:05:49 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c1bd9522799773adb723d78cef494168d851dd759ef42bdf230e3518c9888d`  
		Last Modified: Fri, 29 Jan 2021 01:05:54 GMT  
		Size: 13.6 MB (13571709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60b70fa5215a21be024094dd917f70d206590186d21137fcb75d1fb68a887a2`  
		Last Modified: Fri, 29 Jan 2021 01:05:49 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733b25bcaba65cbff9b151c9ab65d005350d890d7728bfe14024f5f4bd9ca890`  
		Last Modified: Fri, 29 Jan 2021 01:05:49 GMT  
		Size: 17.5 KB (17531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dda7886eea28b54dfe2eea50537d02027bbbcda31bb0d081dff700b99290584`  
		Last Modified: Fri, 29 Jan 2021 02:12:41 GMT  
		Size: 29.0 MB (28956651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90907b51293338df699b9f07cbb70441610fa8f2924e32d21967026449fe4064`  
		Last Modified: Fri, 29 Jan 2021 02:12:28 GMT  
		Size: 193.5 KB (193490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85552216f6bbc21bc776e9622f10a51b96b9a92310894072d91339b4fe625b1e`  
		Last Modified: Fri, 29 Jan 2021 02:12:28 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277406688472a6794691f5e4a67b9a1fff148488bd3592f46c1ff32c50b9e712`  
		Last Modified: Fri, 29 Jan 2021 02:12:28 GMT  
		Size: 552.8 KB (552840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31adf754bdf3aa207b3395bac818c602ae3326449c8eef1d435c2deefb3a2dd0`  
		Last Modified: Fri, 29 Jan 2021 02:12:29 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d326c954a1dde2641329fe23cd34f82ea22e784961b8e5e3098ea38e58e06bf`  
		Last Modified: Fri, 29 Jan 2021 02:12:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.0.9` - linux; arm variant v7

```console
$ docker pull composer@sha256:269f67fe496ec79ec849b998dff19dd47f34368253361860e8c85cdc3fe60289
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56107193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929093143b6d7781fa9c2240f279fcb895b68e0ff527e64b6cd13779c07c5f9d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:58:27 GMT
ADD file:718d7c24a8d6ff0feb2843cf8c3ca4b7ef1fb523a45dea568404259a7b4e6f10 in / 
# Fri, 15 Jan 2021 01:58:29 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:04:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:04:05 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:04:07 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:04:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:04:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:04:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:04:13 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:04:14 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:04:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:04:15 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:04:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:04:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:07:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:10:13 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:10:16 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:10:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:10:18 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 21:57:49 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 21:58:13 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 21:58:15 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 21:58:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 21:58:17 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 21:58:17 GMT
ENV COMPOSER_VERSION=2.0.9
# Thu, 28 Jan 2021 21:58:21 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 21:58:21 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 21:58:22 GMT
WORKDIR /app
# Thu, 28 Jan 2021 21:58:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 21:58:24 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:0f34ce5da94097b8c334f6b2065a010aced9855c3532e4462e9bd1b0a4c4b3f6`  
		Last Modified: Fri, 15 Jan 2021 01:59:13 GMT  
		Size: 2.4 MB (2422744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cecec77a7b5b50913bcb9f7bfe0c5fdcebb948b947747285290197c13902be91`  
		Last Modified: Fri, 15 Jan 2021 23:42:36 GMT  
		Size: 1.6 MB (1555130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0496082b3c55009a50b47ce80bf27dd7451aaa7e13b5b4ccbe886a780c614dd1`  
		Last Modified: Fri, 15 Jan 2021 23:42:33 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af351861d88fff830659b71d51e45b8e623d31cb86c764fab107e6c39ca5a717`  
		Last Modified: Fri, 15 Jan 2021 23:42:33 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11aa9107e62f7893b45936388317768641833b4f6b1937989fcbfc5845e1c698`  
		Last Modified: Fri, 15 Jan 2021 23:42:32 GMT  
		Size: 10.7 MB (10661711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739d880e478996d44b501dcc056bf9f5f25909c929d579ba0c02f123be170522`  
		Last Modified: Fri, 15 Jan 2021 23:42:30 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed2a0f0dbdad0b49284a158baa86126c2b2a794ee53b82c4181378520555f1d`  
		Last Modified: Fri, 15 Jan 2021 23:42:36 GMT  
		Size: 13.1 MB (13070133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b9ed4df09ec14031c338ad506ba7fcc76ab6a07fc32432ad75d94867ae04d9`  
		Last Modified: Thu, 21 Jan 2021 19:23:58 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500dd1602efbacb91e481ac3e868dadb7bca74fb6b4f73d41fb2ec82cab72f22`  
		Last Modified: Thu, 21 Jan 2021 19:23:59 GMT  
		Size: 17.5 KB (17536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b52f140a609f714bafc66c167ec2b6c04c8962153f406e1ac18bac7b669c61`  
		Last Modified: Thu, 28 Jan 2021 21:59:15 GMT  
		Size: 27.6 MB (27635729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cb9e5e751c90392752772de98a302d52a12f4ea2dcf08223098a5cb41c1fd4`  
		Last Modified: Thu, 28 Jan 2021 21:58:57 GMT  
		Size: 186.3 KB (186294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964a5881822f5f5e182f7b8d8fef32582177380aff1c392f68c3c5f908be31d4`  
		Last Modified: Thu, 28 Jan 2021 21:58:57 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174e82ce233fe45d2052d89f8f6ceb309742ffa529fff02fe0a3bf4f0dc2680e`  
		Last Modified: Thu, 28 Jan 2021 21:58:58 GMT  
		Size: 552.8 KB (552840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea9421b9b2b639e1f21013f53e1e2cb09a3ec7f0dd823ee954f9244314cf5f8`  
		Last Modified: Thu, 28 Jan 2021 21:58:57 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f226ced10a6383ba65f01fbbba9c1e769fd7453d057d027dfca14e3fabb41e70`  
		Last Modified: Thu, 28 Jan 2021 21:58:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.0.9` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:130052d528820f06b656c3894131122517ca768a3631d480fe30ad0c5ff17726
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61979559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f614517de9bbe4432cf2dd955bf7b9c7c3ab8d99fe944f7ba233d58a98f67a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:47:51 GMT
ADD file:95be2cec37537b3fd70aeb1d4eb3479fc4a56b00ad7180788ddd7fa772ca65e7 in / 
# Fri, 15 Jan 2021 01:47:52 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:04:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:04:28 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:04:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:04:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:04:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:04:39 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:04:40 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:04:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:04:41 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:04:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:04:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:09:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:51:20 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:51:27 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:51:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:51:31 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:39:49 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:40:10 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:40:12 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:40:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:40:14 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:40:14 GMT
ENV COMPOSER_VERSION=2.0.9
# Thu, 28 Jan 2021 22:40:17 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:40:18 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:40:19 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:40:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:40:20 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:30d5333d20a68dd6ea3689e2c5692d7071f2d68e72c06f0b3b4c7e213df454e2`  
		Last Modified: Fri, 15 Jan 2021 01:48:29 GMT  
		Size: 2.7 MB (2710904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72077bc47778707d4c51904bf6932e44a09d9a5a37f1bac45ef59fe94bc54e1`  
		Last Modified: Fri, 15 Jan 2021 23:49:43 GMT  
		Size: 1.7 MB (1694577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bfc628cf72db6285835ff062834a15ee7c9067f6b7ccb55fad0a8bb0f292be`  
		Last Modified: Fri, 15 Jan 2021 23:49:41 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ab015e378a2ad2e4c345884006fc6b1678a0ebba44214fbc5e9dcb48ef7bb2`  
		Last Modified: Fri, 15 Jan 2021 23:49:41 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d24a448de09dec3ceb6bc305d0c17be120e79f5611f1e4054850e11526133cc8`  
		Last Modified: Fri, 15 Jan 2021 23:49:39 GMT  
		Size: 10.7 MB (10661733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8079f19e688581d52496f1937db9dc33ef25e597b149eb517633043678bd61d2`  
		Last Modified: Fri, 15 Jan 2021 23:49:39 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978c3da5ab542fa26ea4333b9b5c608d2ee68fa98cbf1e0d05df83ece9439e24`  
		Last Modified: Fri, 15 Jan 2021 23:49:45 GMT  
		Size: 14.8 MB (14764647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1043bb484cdf4818387523cb0c703d862e1c50b54ebe62f605c0d3b74837f39`  
		Last Modified: Thu, 21 Jan 2021 20:05:13 GMT  
		Size: 2.3 KB (2269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c953f678545439a3b425e1dd037e3e5d5b8092e37adb1a63cb110a0a888b5300`  
		Last Modified: Thu, 21 Jan 2021 20:05:12 GMT  
		Size: 17.6 KB (17550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f77742777349432a5c810bb823719115d594ef2d7e0d79d11fdccf49b1c298`  
		Last Modified: Thu, 28 Jan 2021 22:41:08 GMT  
		Size: 31.4 MB (31376168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20f98fa3077571418cb9ac1f3ceb60436f9c6bcda79d861d68e9c48787403d1`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 196.1 KB (196059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899d29da6e7af774384acf87f4eea2a9876f6bff3365b1486ecb6738a8e95143`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021c1a2b1a0c143edd7a90b286aadd175b31efbab95350d145d59b1b0cc1740c`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 552.8 KB (552841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0494b560b93a7d7e5bec8bd6817755005fb72e254367b206700c500a1fcd9fac`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f103a78f14a331ed6ca557b26ebf9efaf424f463cc7ef659dd83935e1863c665`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.0.9` - linux; 386

```console
$ docker pull composer@sha256:d1366c8963cfab30a01f8eaf0c86def4785d85fcd67616b0325ad4e4e4633832
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63702654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af66081ead599dedc0d793ecd53ecd5631d90a00ce2dfb71be5d837044975ac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:38:28 GMT
ADD file:d8723c02f1eb0efa4dadc6480a753d18d7e28d9815bff96a92ff09ff55a92b11 in / 
# Fri, 15 Jan 2021 01:38:29 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 22:42:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 22:42:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 22:42:23 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 22:42:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 22:42:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 22:42:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:42:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:42:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 22:42:24 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 22:42:25 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 22:42:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 22:42:25 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 22:42:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 22:42:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 22:49:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:44:48 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:44:51 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:44:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:44:51 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:38:41 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:38:56 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:38:57 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:38:57 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:38:57 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:38:57 GMT
ENV COMPOSER_VERSION=2.0.9
# Thu, 28 Jan 2021 22:38:59 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:39:00 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:39:00 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:39:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:39:00 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9e6a151110e36daa7a487250f98425289313f856e3a586d89d82bafc1bf322c3`  
		Last Modified: Fri, 15 Jan 2021 01:39:01 GMT  
		Size: 2.8 MB (2817152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b194694eae0c8525a66d3c56796eb37a9e263d63f03eaecf6bc83d2ab3f7c9`  
		Last Modified: Fri, 15 Jan 2021 23:50:55 GMT  
		Size: 1.8 MB (1793505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a9a95dec7f2cd3bcf6903d006a870fa7113f6a974d30ec6634ab82b0a0a792`  
		Last Modified: Fri, 15 Jan 2021 23:50:52 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ad687f5cfc54121cc70af5ff69cb844177c4325a2c14efcd144cb096ecfba2`  
		Last Modified: Fri, 15 Jan 2021 23:50:54 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ae4debbbbc31db383a639e6a7df85ebf9c2f15905a9ec2df4fb8a3998dec90`  
		Last Modified: Fri, 15 Jan 2021 23:50:56 GMT  
		Size: 10.7 MB (10661677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900efcbd73b95b91ec42e946efd16fa2e312e57beba40e9aac2b0699baa90d1d`  
		Last Modified: Fri, 15 Jan 2021 23:50:51 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c042850cc5dcebe86c931da9e6014fe607a6c507fe5a61059ba47003a80cac2`  
		Last Modified: Fri, 15 Jan 2021 23:51:00 GMT  
		Size: 15.3 MB (15348857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a592432a0a1e356653687e23dd3c8f953d0fc904db0377fa898de0c851be229d`  
		Last Modified: Thu, 21 Jan 2021 19:55:39 GMT  
		Size: 2.3 KB (2270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3b6898b8d491988e64358ef661f654c98cbec8cc3e36edeedea25334aae60e`  
		Last Modified: Thu, 21 Jan 2021 19:55:40 GMT  
		Size: 17.5 KB (17525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fcd335e71480482247bfd7863baa60db887184f8227377b99d22f61dc2a4d6`  
		Last Modified: Thu, 28 Jan 2021 22:39:38 GMT  
		Size: 32.3 MB (32292342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f574926dca5384453b345a61350707cbf2753926b84e8c685a1899bbe6ff5b`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 213.8 KB (213825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25022b6f8e9b3bd588f8db12caab7e929709dcb604f7f84786e3a7d54f6bd2f4`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383490e188660eeea8b6c894366164f4300f53b351efbc251fa34ccd12a24504`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 552.8 KB (552799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7647a67da25834616edba6106817cca07fa93408500bf11d4aaa476837b4bcb1`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91eedfded7d6e258e16f2eec203d90eaa4b9de30b187ba609ee65940bf265403`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.0.9` - linux; ppc64le

```console
$ docker pull composer@sha256:f6885d88746bfdfba04dfbaccf1d47d9e46a0130f5a0e904f581ffb380ea7403
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (64048836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc955ccd3e71ac5325e45e1cced0cff964d9c6039532c739122eb9d7fa9bc3e7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 02:41:43 GMT
ADD file:137e8f98476d5dceaeb2e8359f50eb818dee4c327e4492d16e87fb27d40aa891 in / 
# Fri, 15 Jan 2021 02:41:46 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:17:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:17:44 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:17:56 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:18:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:18:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:18:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:18:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:18:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:18:39 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:18:43 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:18:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:19:07 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:19:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:19:38 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:24:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:33:15 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:33:36 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:33:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:33:47 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:26:03 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:27:01 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:27:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:27:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:27:24 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:27:35 GMT
ENV COMPOSER_VERSION=2.0.9
# Thu, 28 Jan 2021 22:27:52 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:27:55 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:28:00 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:28:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:28:20 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cb0f06c26ffdc2117b9a3467f79e69cdf8d9c677a3c0bacabc8a694a9fe303a8`  
		Last Modified: Fri, 15 Jan 2021 02:42:19 GMT  
		Size: 2.8 MB (2812389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9a7aad5bd113c5dca33b681663b0c58f66e510017e693801a6688a9c4bab60`  
		Last Modified: Sat, 16 Jan 2021 00:14:01 GMT  
		Size: 1.7 MB (1741834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ce1d80ff72759b98cf2f5ad1efa6dd181e5f4343bb0e25cbb4ec9d5d3847f4`  
		Last Modified: Sat, 16 Jan 2021 00:14:01 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48055526d8202af50f6248db9b3cb8938cab9cfec15a1312b4c1e3782f3307c4`  
		Last Modified: Sat, 16 Jan 2021 00:14:02 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7cb5ec22b0cc763855f0481247394a6e312f8f906d232f738fc88a4219bfb1e`  
		Last Modified: Sat, 16 Jan 2021 00:13:58 GMT  
		Size: 10.7 MB (10661716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea93ae862f86d372e01dcb82dbf509e78b3f4e6533f9660f4b63c49471cb4852`  
		Last Modified: Sat, 16 Jan 2021 00:13:57 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7518496c61b651e86a2bdd79ee76e400addfddbafa26db36f7e692520aeebc1e`  
		Last Modified: Sat, 16 Jan 2021 00:14:01 GMT  
		Size: 16.1 MB (16059509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dce1a5a13b51550c7b84a60d64d364686f108d412e4776aae7d7a4922ac1ebd`  
		Last Modified: Thu, 21 Jan 2021 20:03:07 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98df2e2e9c3e105f7ddf5634cc2558ef8a2e569cd7e61121bd1f18c83a96152d`  
		Last Modified: Thu, 21 Jan 2021 20:03:07 GMT  
		Size: 17.5 KB (17538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c3ac64e0e6d2c9f92c30e69ce18c62c2ff9ba34f99a48d00be9b92ccfcf393`  
		Last Modified: Thu, 28 Jan 2021 22:30:18 GMT  
		Size: 32.0 MB (31993881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fb84ebef4906eea3269f759da0902a8097011fb84006aabbd679b5950e0970`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 204.0 KB (204039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8dba6ae992e0605a8d35408b1a00afba44b82e2b40e0fde68e8181c954ff546`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a807025eeb4eee2fa9e4b73979c81b5c1dcc0e7120dde50a1d3c99484cf82f3`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 552.9 KB (552850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a61464199f95698607ae83201de96ef6080a79661d612accc419b63ea4a42d4`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c480de546173fd553d57ceedac81c7d3a491e179672b29c93ac7bfd2619b3b74`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:2.0.9` - linux; s390x

```console
$ docker pull composer@sha256:30b6319b9309316189f19f86b8b18dd6cdf31730b5d9f6293ab8e75dcda242bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61546888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13363e884d01029047438b8cf02cdbbf365c7b9df0b95e49e6802a98df33bfde`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:51:34 GMT
ADD file:3ba807ca8ed73ca14224dd26a883f2399031fa32430f035cc5ae97b5e6db0ca7 in / 
# Fri, 15 Jan 2021 01:51:35 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 22:57:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 22:57:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 22:57:13 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 22:57:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 22:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 22:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:57:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:57:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 22:57:17 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 22:57:17 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 22:57:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 22:57:18 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 22:57:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 22:57:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:02:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:54:10 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:54:13 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:54:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:54:14 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:42:35 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:42:53 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:42:54 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:42:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:42:54 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:42:55 GMT
ENV COMPOSER_VERSION=2.0.9
# Thu, 28 Jan 2021 22:42:57 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:42:57 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:42:58 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:42:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:42:59 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:3997176601fb5d5ac06922718668ede4acac00a5c0daef8a9099fd76ce93047f`  
		Last Modified: Fri, 15 Jan 2021 01:52:40 GMT  
		Size: 2.6 MB (2601720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497e79d9095f9ba4812f1150c33ad07d399f559fea8e3c4fe8553e02f2cf8b6a`  
		Last Modified: Fri, 15 Jan 2021 23:39:10 GMT  
		Size: 1.8 MB (1756352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99527660904ffc5aed1d27bb86166f189e04b5df76d7becf74efffb1836eaf5e`  
		Last Modified: Fri, 15 Jan 2021 23:39:10 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9b51111e1ef5a5156e505d6369bb2d4e21354a1203636fca6f26de34df9c15`  
		Last Modified: Fri, 15 Jan 2021 23:39:10 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3c721a3fef9acf0bac166c45ff18e2485752ef7b86447284b7b710646d40df`  
		Last Modified: Fri, 15 Jan 2021 23:38:47 GMT  
		Size: 10.7 MB (10661723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e676c2ca01980f72daf35a53dae36e4fe10945de76af81d54618066f5204c598`  
		Last Modified: Fri, 15 Jan 2021 23:38:48 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90c350aff0df72bb91eaa20306afe2218ac1d50242eb213d4e481f65b2a9f60`  
		Last Modified: Fri, 15 Jan 2021 23:38:48 GMT  
		Size: 14.4 MB (14364644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c91dec7c10d367e01e4907cb6c2d00b3e5b7390545c8c9499eaac3c35986507`  
		Last Modified: Thu, 21 Jan 2021 20:05:24 GMT  
		Size: 2.3 KB (2269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63e510378e653ab6ff71c58fc15e869877848171131d614af01c250d7a36e31`  
		Last Modified: Thu, 21 Jan 2021 20:05:20 GMT  
		Size: 17.5 KB (17541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4079b673c2155f6fc765bd4b8d683a2326dd552affe882edccb45c657534ed18`  
		Last Modified: Thu, 28 Jan 2021 22:43:28 GMT  
		Size: 31.4 MB (31389182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdeafc632059b12ff488232684da09d9c34de98941c5f6ff69c471274af7602`  
		Last Modified: Thu, 28 Jan 2021 22:43:22 GMT  
		Size: 197.8 KB (197815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f475e4a4966b8ce4d7561e4c7a2e4961201d5b118193c3525421174abaaa14e5`  
		Last Modified: Thu, 28 Jan 2021 22:43:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0527c47a0591fb1d627eb0553a148074dc26b3e929f17fe11c70beb29ddc697e`  
		Last Modified: Thu, 28 Jan 2021 22:43:21 GMT  
		Size: 552.8 KB (552833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20581df10571ef1589ab514908ef57a5508e11f388e2022afb5678afc09bdcdb`  
		Last Modified: Thu, 28 Jan 2021 22:43:21 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d915abaf68a0c69e745c6fa8e076f421f760e793935af4022615f2460c3f7cb`  
		Last Modified: Thu, 28 Jan 2021 22:43:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `composer:latest`

```console
$ docker pull composer@sha256:f8dfdbaac5983fe7698848442d1d0a39753ef72715391bdbd4553d0b2636020d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `composer:latest` - linux; amd64

```console
$ docker pull composer@sha256:005d4a50002fcf58eb93b749345b73441cb615644f0790844538d0990cc3ce20
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62417362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e0bd4ead1c9c98e491c19a4b10307760a1a5060996f40e5f5229bd6882b578`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 02:23:51 GMT
ADD file:edbe213ae0c825a5bfbe569928cf20f683f334f93a093ccd0a3a014b7428e760 in / 
# Fri, 15 Jan 2021 02:23:51 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:43:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:43:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:43:26 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:43:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:43:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:43:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:43:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:43:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:43:30 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:43:30 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:43:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:43:31 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:43:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:43:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:51:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 20:17:47 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 20:17:50 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 20:17:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 20:17:51 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:32:03 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:32:24 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:32:24 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:32:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:32:25 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:32:25 GMT
ENV COMPOSER_VERSION=2.0.9
# Thu, 28 Jan 2021 22:32:27 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:32:27 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:32:28 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:32:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:32:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:596ba82af5aaa3e2fd9d6f955b8b94f0744a2b60710e3c243ba3e4a467f051d1`  
		Last Modified: Fri, 15 Jan 2021 02:08:10 GMT  
		Size: 2.8 MB (2810825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af74f285bb27c6623f2b5c8c3a2e487603c7dd5c51859fd6e13859542f4310c3`  
		Last Modified: Sat, 16 Jan 2021 01:00:24 GMT  
		Size: 1.7 MB (1694838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab8440e5667ccb2ffd4e62ed905a106742dfdd7dd3167d9d64b4bdeed8a4945`  
		Last Modified: Sat, 16 Jan 2021 01:00:20 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64889fa545ec919e6fe392c368b8cb41a10e7834c1ba4d4d96fd9ee2e3405cc1`  
		Last Modified: Sat, 16 Jan 2021 01:00:20 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94168e6487351b04d28db6aabb22e0c68ad3582533cf8d7e00322078720f8081`  
		Last Modified: Sat, 16 Jan 2021 01:00:19 GMT  
		Size: 10.7 MB (10661716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3898f14298ef25ab2005e9025a88f553003a83a1b6a61765e93d78879441aa36`  
		Last Modified: Sat, 16 Jan 2021 01:00:18 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3747e5f21671eba796a4b76a6abc180c60b0ef9414e9a80b325b31aeaa1f6ca`  
		Last Modified: Sat, 16 Jan 2021 01:00:21 GMT  
		Size: 15.3 MB (15318011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3df0f8088890764041d8dbfe574cd5bdf020400801b0b108cd6b7f965aab3a`  
		Last Modified: Thu, 21 Jan 2021 20:28:34 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f6ddeaf0bdcf495df2e7c8d72852796c1bae3d9f8ef8260058fdb43b995163`  
		Last Modified: Thu, 21 Jan 2021 20:28:34 GMT  
		Size: 17.5 KB (17539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29338fcaf9eb090ba02397a08616210ac758731039ac2d2a5db97288090a1845`  
		Last Modified: Thu, 28 Jan 2021 22:32:55 GMT  
		Size: 31.2 MB (31158400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a0bf379d52ae6a08ffd2313828e5738aa1cfd2a934c2403e6065ae7f94ba05`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 198.3 KB (198274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a346beb5e7dfc07424d1d661858912a89fab48a63bd89492e0c97c3cf1a6c75`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e86daf479799f96a49bc265571da38b2be4344f28a6b8ed4a0a18cb1dafae08`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 552.8 KB (552794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048afd2f48877072346dfbc095e6883b2ccc828164f17723d6e95d230c798b83`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad27987395f1263b907d761fc5f4b5a356869262f62cd2b055f7c8bb050317ac`  
		Last Modified: Thu, 28 Jan 2021 22:32:49 GMT  
		Size: 90.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:8555fcdcc559af5253afc8400e8f2f92937211b20947c2b1d231b3ab2a703663
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58265639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d766a7469442cfbfeb325a177218e32152d532c8efaec2dd15a2fd56020467`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 28 Jan 2021 23:49:59 GMT
ADD file:c197324e4979e2a7b257ad683d20dd9cbdae525a076bd68fe6aa0e0b126875df in / 
# Thu, 28 Jan 2021 23:49:59 GMT
CMD ["/bin/sh"]
# Fri, 29 Jan 2021 00:33:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 29 Jan 2021 00:33:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 29 Jan 2021 00:33:59 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 29 Jan 2021 00:34:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 29 Jan 2021 00:34:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 29 Jan 2021 00:34:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 29 Jan 2021 00:34:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 29 Jan 2021 00:34:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 29 Jan 2021 00:34:08 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 29 Jan 2021 00:34:11 GMT
ENV PHP_VERSION=8.0.1
# Fri, 29 Jan 2021 00:34:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 29 Jan 2021 00:34:13 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 29 Jan 2021 00:34:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 29 Jan 2021 00:34:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 29 Jan 2021 00:37:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 29 Jan 2021 00:37:35 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 29 Jan 2021 00:37:38 GMT
RUN docker-php-ext-enable sodium
# Fri, 29 Jan 2021 00:37:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 29 Jan 2021 00:37:40 GMT
CMD ["php" "-a"]
# Fri, 29 Jan 2021 02:11:29 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 29 Jan 2021 02:11:49 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 29 Jan 2021 02:11:51 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 29 Jan 2021 02:11:51 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 29 Jan 2021 02:11:52 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 29 Jan 2021 02:11:52 GMT
ENV COMPOSER_VERSION=2.0.9
# Fri, 29 Jan 2021 02:11:55 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 29 Jan 2021 02:11:56 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 29 Jan 2021 02:11:57 GMT
WORKDIR /app
# Fri, 29 Jan 2021 02:11:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 29 Jan 2021 02:11:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a66f440da051140fefcb0a520bdeb69d763b1eb4fd1b2ed46b4c0a168e335108`  
		Last Modified: Thu, 28 Jan 2021 23:50:33 GMT  
		Size: 2.6 MB (2621759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa34846effbef1e901021c65a67535efc29a1aa39b259a4c29559d1439f4131`  
		Last Modified: Fri, 29 Jan 2021 01:05:52 GMT  
		Size: 1.7 MB (1684855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba088c5e0e1fb4c64a8b59354bedcae82636c10a93fe3790125bec5c1e841299`  
		Last Modified: Fri, 29 Jan 2021 01:05:51 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b10584422ada7d37ac091eae04bcee5df4cee5b93cd86068ce55c7ab085ae62`  
		Last Modified: Fri, 29 Jan 2021 01:05:51 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd2125b643842a0b1fb7799c57d504cb3ea72f1cdaac6d48b6d3ee2fa033d39`  
		Last Modified: Fri, 29 Jan 2021 01:05:50 GMT  
		Size: 10.7 MB (10661723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370c8d7d436fffa9dd306db82b4a90f7b25ae1d68c658dac4c195ec6a921976e`  
		Last Modified: Fri, 29 Jan 2021 01:05:49 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c1bd9522799773adb723d78cef494168d851dd759ef42bdf230e3518c9888d`  
		Last Modified: Fri, 29 Jan 2021 01:05:54 GMT  
		Size: 13.6 MB (13571709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60b70fa5215a21be024094dd917f70d206590186d21137fcb75d1fb68a887a2`  
		Last Modified: Fri, 29 Jan 2021 01:05:49 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733b25bcaba65cbff9b151c9ab65d005350d890d7728bfe14024f5f4bd9ca890`  
		Last Modified: Fri, 29 Jan 2021 01:05:49 GMT  
		Size: 17.5 KB (17531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dda7886eea28b54dfe2eea50537d02027bbbcda31bb0d081dff700b99290584`  
		Last Modified: Fri, 29 Jan 2021 02:12:41 GMT  
		Size: 29.0 MB (28956651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90907b51293338df699b9f07cbb70441610fa8f2924e32d21967026449fe4064`  
		Last Modified: Fri, 29 Jan 2021 02:12:28 GMT  
		Size: 193.5 KB (193490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85552216f6bbc21bc776e9622f10a51b96b9a92310894072d91339b4fe625b1e`  
		Last Modified: Fri, 29 Jan 2021 02:12:28 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277406688472a6794691f5e4a67b9a1fff148488bd3592f46c1ff32c50b9e712`  
		Last Modified: Fri, 29 Jan 2021 02:12:28 GMT  
		Size: 552.8 KB (552840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31adf754bdf3aa207b3395bac818c602ae3326449c8eef1d435c2deefb3a2dd0`  
		Last Modified: Fri, 29 Jan 2021 02:12:29 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d326c954a1dde2641329fe23cd34f82ea22e784961b8e5e3098ea38e58e06bf`  
		Last Modified: Fri, 29 Jan 2021 02:12:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:269f67fe496ec79ec849b998dff19dd47f34368253361860e8c85cdc3fe60289
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56107193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929093143b6d7781fa9c2240f279fcb895b68e0ff527e64b6cd13779c07c5f9d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:58:27 GMT
ADD file:718d7c24a8d6ff0feb2843cf8c3ca4b7ef1fb523a45dea568404259a7b4e6f10 in / 
# Fri, 15 Jan 2021 01:58:29 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:04:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:04:05 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:04:07 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:04:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:04:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:04:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:04:13 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:04:14 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:04:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:04:15 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:04:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:04:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:07:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:10:13 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:10:16 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:10:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:10:18 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 21:57:49 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 21:58:13 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 21:58:15 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 21:58:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 21:58:17 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 21:58:17 GMT
ENV COMPOSER_VERSION=2.0.9
# Thu, 28 Jan 2021 21:58:21 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 21:58:21 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 21:58:22 GMT
WORKDIR /app
# Thu, 28 Jan 2021 21:58:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 21:58:24 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:0f34ce5da94097b8c334f6b2065a010aced9855c3532e4462e9bd1b0a4c4b3f6`  
		Last Modified: Fri, 15 Jan 2021 01:59:13 GMT  
		Size: 2.4 MB (2422744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cecec77a7b5b50913bcb9f7bfe0c5fdcebb948b947747285290197c13902be91`  
		Last Modified: Fri, 15 Jan 2021 23:42:36 GMT  
		Size: 1.6 MB (1555130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0496082b3c55009a50b47ce80bf27dd7451aaa7e13b5b4ccbe886a780c614dd1`  
		Last Modified: Fri, 15 Jan 2021 23:42:33 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af351861d88fff830659b71d51e45b8e623d31cb86c764fab107e6c39ca5a717`  
		Last Modified: Fri, 15 Jan 2021 23:42:33 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11aa9107e62f7893b45936388317768641833b4f6b1937989fcbfc5845e1c698`  
		Last Modified: Fri, 15 Jan 2021 23:42:32 GMT  
		Size: 10.7 MB (10661711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739d880e478996d44b501dcc056bf9f5f25909c929d579ba0c02f123be170522`  
		Last Modified: Fri, 15 Jan 2021 23:42:30 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed2a0f0dbdad0b49284a158baa86126c2b2a794ee53b82c4181378520555f1d`  
		Last Modified: Fri, 15 Jan 2021 23:42:36 GMT  
		Size: 13.1 MB (13070133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b9ed4df09ec14031c338ad506ba7fcc76ab6a07fc32432ad75d94867ae04d9`  
		Last Modified: Thu, 21 Jan 2021 19:23:58 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500dd1602efbacb91e481ac3e868dadb7bca74fb6b4f73d41fb2ec82cab72f22`  
		Last Modified: Thu, 21 Jan 2021 19:23:59 GMT  
		Size: 17.5 KB (17536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b52f140a609f714bafc66c167ec2b6c04c8962153f406e1ac18bac7b669c61`  
		Last Modified: Thu, 28 Jan 2021 21:59:15 GMT  
		Size: 27.6 MB (27635729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cb9e5e751c90392752772de98a302d52a12f4ea2dcf08223098a5cb41c1fd4`  
		Last Modified: Thu, 28 Jan 2021 21:58:57 GMT  
		Size: 186.3 KB (186294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964a5881822f5f5e182f7b8d8fef32582177380aff1c392f68c3c5f908be31d4`  
		Last Modified: Thu, 28 Jan 2021 21:58:57 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174e82ce233fe45d2052d89f8f6ceb309742ffa529fff02fe0a3bf4f0dc2680e`  
		Last Modified: Thu, 28 Jan 2021 21:58:58 GMT  
		Size: 552.8 KB (552840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea9421b9b2b639e1f21013f53e1e2cb09a3ec7f0dd823ee954f9244314cf5f8`  
		Last Modified: Thu, 28 Jan 2021 21:58:57 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f226ced10a6383ba65f01fbbba9c1e769fd7453d057d027dfca14e3fabb41e70`  
		Last Modified: Thu, 28 Jan 2021 21:58:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:130052d528820f06b656c3894131122517ca768a3631d480fe30ad0c5ff17726
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61979559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f614517de9bbe4432cf2dd955bf7b9c7c3ab8d99fe944f7ba233d58a98f67a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:47:51 GMT
ADD file:95be2cec37537b3fd70aeb1d4eb3479fc4a56b00ad7180788ddd7fa772ca65e7 in / 
# Fri, 15 Jan 2021 01:47:52 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:04:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:04:28 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:04:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:04:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:04:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:04:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:04:39 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:04:40 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:04:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:04:41 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:04:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:04:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:09:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:51:20 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:51:27 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:51:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:51:31 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:39:49 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:40:10 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:40:12 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:40:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:40:14 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:40:14 GMT
ENV COMPOSER_VERSION=2.0.9
# Thu, 28 Jan 2021 22:40:17 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:40:18 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:40:19 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:40:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:40:20 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:30d5333d20a68dd6ea3689e2c5692d7071f2d68e72c06f0b3b4c7e213df454e2`  
		Last Modified: Fri, 15 Jan 2021 01:48:29 GMT  
		Size: 2.7 MB (2710904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72077bc47778707d4c51904bf6932e44a09d9a5a37f1bac45ef59fe94bc54e1`  
		Last Modified: Fri, 15 Jan 2021 23:49:43 GMT  
		Size: 1.7 MB (1694577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bfc628cf72db6285835ff062834a15ee7c9067f6b7ccb55fad0a8bb0f292be`  
		Last Modified: Fri, 15 Jan 2021 23:49:41 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ab015e378a2ad2e4c345884006fc6b1678a0ebba44214fbc5e9dcb48ef7bb2`  
		Last Modified: Fri, 15 Jan 2021 23:49:41 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d24a448de09dec3ceb6bc305d0c17be120e79f5611f1e4054850e11526133cc8`  
		Last Modified: Fri, 15 Jan 2021 23:49:39 GMT  
		Size: 10.7 MB (10661733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8079f19e688581d52496f1937db9dc33ef25e597b149eb517633043678bd61d2`  
		Last Modified: Fri, 15 Jan 2021 23:49:39 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978c3da5ab542fa26ea4333b9b5c608d2ee68fa98cbf1e0d05df83ece9439e24`  
		Last Modified: Fri, 15 Jan 2021 23:49:45 GMT  
		Size: 14.8 MB (14764647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1043bb484cdf4818387523cb0c703d862e1c50b54ebe62f605c0d3b74837f39`  
		Last Modified: Thu, 21 Jan 2021 20:05:13 GMT  
		Size: 2.3 KB (2269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c953f678545439a3b425e1dd037e3e5d5b8092e37adb1a63cb110a0a888b5300`  
		Last Modified: Thu, 21 Jan 2021 20:05:12 GMT  
		Size: 17.6 KB (17550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f77742777349432a5c810bb823719115d594ef2d7e0d79d11fdccf49b1c298`  
		Last Modified: Thu, 28 Jan 2021 22:41:08 GMT  
		Size: 31.4 MB (31376168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20f98fa3077571418cb9ac1f3ceb60436f9c6bcda79d861d68e9c48787403d1`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 196.1 KB (196059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899d29da6e7af774384acf87f4eea2a9876f6bff3365b1486ecb6738a8e95143`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021c1a2b1a0c143edd7a90b286aadd175b31efbab95350d145d59b1b0cc1740c`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 552.8 KB (552841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0494b560b93a7d7e5bec8bd6817755005fb72e254367b206700c500a1fcd9fac`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f103a78f14a331ed6ca557b26ebf9efaf424f463cc7ef659dd83935e1863c665`  
		Last Modified: Thu, 28 Jan 2021 22:40:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; 386

```console
$ docker pull composer@sha256:d1366c8963cfab30a01f8eaf0c86def4785d85fcd67616b0325ad4e4e4633832
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63702654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af66081ead599dedc0d793ecd53ecd5631d90a00ce2dfb71be5d837044975ac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:38:28 GMT
ADD file:d8723c02f1eb0efa4dadc6480a753d18d7e28d9815bff96a92ff09ff55a92b11 in / 
# Fri, 15 Jan 2021 01:38:29 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 22:42:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 22:42:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 22:42:23 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 22:42:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 22:42:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 22:42:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:42:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:42:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 22:42:24 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 22:42:25 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 22:42:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 22:42:25 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 22:42:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 22:42:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 22:49:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:44:48 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:44:51 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:44:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:44:51 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:38:41 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:38:56 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:38:57 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:38:57 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:38:57 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:38:57 GMT
ENV COMPOSER_VERSION=2.0.9
# Thu, 28 Jan 2021 22:38:59 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:39:00 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:39:00 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:39:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:39:00 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9e6a151110e36daa7a487250f98425289313f856e3a586d89d82bafc1bf322c3`  
		Last Modified: Fri, 15 Jan 2021 01:39:01 GMT  
		Size: 2.8 MB (2817152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b194694eae0c8525a66d3c56796eb37a9e263d63f03eaecf6bc83d2ab3f7c9`  
		Last Modified: Fri, 15 Jan 2021 23:50:55 GMT  
		Size: 1.8 MB (1793505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a9a95dec7f2cd3bcf6903d006a870fa7113f6a974d30ec6634ab82b0a0a792`  
		Last Modified: Fri, 15 Jan 2021 23:50:52 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ad687f5cfc54121cc70af5ff69cb844177c4325a2c14efcd144cb096ecfba2`  
		Last Modified: Fri, 15 Jan 2021 23:50:54 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ae4debbbbc31db383a639e6a7df85ebf9c2f15905a9ec2df4fb8a3998dec90`  
		Last Modified: Fri, 15 Jan 2021 23:50:56 GMT  
		Size: 10.7 MB (10661677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900efcbd73b95b91ec42e946efd16fa2e312e57beba40e9aac2b0699baa90d1d`  
		Last Modified: Fri, 15 Jan 2021 23:50:51 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c042850cc5dcebe86c931da9e6014fe607a6c507fe5a61059ba47003a80cac2`  
		Last Modified: Fri, 15 Jan 2021 23:51:00 GMT  
		Size: 15.3 MB (15348857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a592432a0a1e356653687e23dd3c8f953d0fc904db0377fa898de0c851be229d`  
		Last Modified: Thu, 21 Jan 2021 19:55:39 GMT  
		Size: 2.3 KB (2270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3b6898b8d491988e64358ef661f654c98cbec8cc3e36edeedea25334aae60e`  
		Last Modified: Thu, 21 Jan 2021 19:55:40 GMT  
		Size: 17.5 KB (17525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fcd335e71480482247bfd7863baa60db887184f8227377b99d22f61dc2a4d6`  
		Last Modified: Thu, 28 Jan 2021 22:39:38 GMT  
		Size: 32.3 MB (32292342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f574926dca5384453b345a61350707cbf2753926b84e8c685a1899bbe6ff5b`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 213.8 KB (213825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25022b6f8e9b3bd588f8db12caab7e929709dcb604f7f84786e3a7d54f6bd2f4`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383490e188660eeea8b6c894366164f4300f53b351efbc251fa34ccd12a24504`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 552.8 KB (552799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7647a67da25834616edba6106817cca07fa93408500bf11d4aaa476837b4bcb1`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91eedfded7d6e258e16f2eec203d90eaa4b9de30b187ba609ee65940bf265403`  
		Last Modified: Thu, 28 Jan 2021 22:39:28 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; ppc64le

```console
$ docker pull composer@sha256:f6885d88746bfdfba04dfbaccf1d47d9e46a0130f5a0e904f581ffb380ea7403
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (64048836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc955ccd3e71ac5325e45e1cced0cff964d9c6039532c739122eb9d7fa9bc3e7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 02:41:43 GMT
ADD file:137e8f98476d5dceaeb2e8359f50eb818dee4c327e4492d16e87fb27d40aa891 in / 
# Fri, 15 Jan 2021 02:41:46 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 23:17:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 23:17:44 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 23:17:56 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 23:18:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 23:18:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 23:18:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:18:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 23:18:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 23:18:39 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 23:18:43 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 23:18:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 23:19:07 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 23:19:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 23:19:38 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:24:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:33:15 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:33:36 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:33:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:33:47 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:26:03 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:27:01 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:27:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:27:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:27:24 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:27:35 GMT
ENV COMPOSER_VERSION=2.0.9
# Thu, 28 Jan 2021 22:27:52 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:27:55 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:28:00 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:28:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:28:20 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cb0f06c26ffdc2117b9a3467f79e69cdf8d9c677a3c0bacabc8a694a9fe303a8`  
		Last Modified: Fri, 15 Jan 2021 02:42:19 GMT  
		Size: 2.8 MB (2812389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9a7aad5bd113c5dca33b681663b0c58f66e510017e693801a6688a9c4bab60`  
		Last Modified: Sat, 16 Jan 2021 00:14:01 GMT  
		Size: 1.7 MB (1741834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ce1d80ff72759b98cf2f5ad1efa6dd181e5f4343bb0e25cbb4ec9d5d3847f4`  
		Last Modified: Sat, 16 Jan 2021 00:14:01 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48055526d8202af50f6248db9b3cb8938cab9cfec15a1312b4c1e3782f3307c4`  
		Last Modified: Sat, 16 Jan 2021 00:14:02 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7cb5ec22b0cc763855f0481247394a6e312f8f906d232f738fc88a4219bfb1e`  
		Last Modified: Sat, 16 Jan 2021 00:13:58 GMT  
		Size: 10.7 MB (10661716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea93ae862f86d372e01dcb82dbf509e78b3f4e6533f9660f4b63c49471cb4852`  
		Last Modified: Sat, 16 Jan 2021 00:13:57 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7518496c61b651e86a2bdd79ee76e400addfddbafa26db36f7e692520aeebc1e`  
		Last Modified: Sat, 16 Jan 2021 00:14:01 GMT  
		Size: 16.1 MB (16059509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dce1a5a13b51550c7b84a60d64d364686f108d412e4776aae7d7a4922ac1ebd`  
		Last Modified: Thu, 21 Jan 2021 20:03:07 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98df2e2e9c3e105f7ddf5634cc2558ef8a2e569cd7e61121bd1f18c83a96152d`  
		Last Modified: Thu, 21 Jan 2021 20:03:07 GMT  
		Size: 17.5 KB (17538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c3ac64e0e6d2c9f92c30e69ce18c62c2ff9ba34f99a48d00be9b92ccfcf393`  
		Last Modified: Thu, 28 Jan 2021 22:30:18 GMT  
		Size: 32.0 MB (31993881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fb84ebef4906eea3269f759da0902a8097011fb84006aabbd679b5950e0970`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 204.0 KB (204039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8dba6ae992e0605a8d35408b1a00afba44b82e2b40e0fde68e8181c954ff546`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a807025eeb4eee2fa9e4b73979c81b5c1dcc0e7120dde50a1d3c99484cf82f3`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 552.9 KB (552850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a61464199f95698607ae83201de96ef6080a79661d612accc419b63ea4a42d4`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c480de546173fd553d57ceedac81c7d3a491e179672b29c93ac7bfd2619b3b74`  
		Last Modified: Thu, 28 Jan 2021 22:30:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; s390x

```console
$ docker pull composer@sha256:30b6319b9309316189f19f86b8b18dd6cdf31730b5d9f6293ab8e75dcda242bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61546888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13363e884d01029047438b8cf02cdbbf365c7b9df0b95e49e6802a98df33bfde`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 15 Jan 2021 01:51:34 GMT
ADD file:3ba807ca8ed73ca14224dd26a883f2399031fa32430f035cc5ae97b5e6db0ca7 in / 
# Fri, 15 Jan 2021 01:51:35 GMT
CMD ["/bin/sh"]
# Fri, 15 Jan 2021 22:57:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Jan 2021 22:57:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 15 Jan 2021 22:57:13 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Jan 2021 22:57:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Jan 2021 22:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 Jan 2021 22:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:57:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Jan 2021 22:57:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 Jan 2021 22:57:17 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 15 Jan 2021 22:57:17 GMT
ENV PHP_VERSION=8.0.1
# Fri, 15 Jan 2021 22:57:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 15 Jan 2021 22:57:18 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 15 Jan 2021 22:57:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 15 Jan 2021 22:57:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 Jan 2021 23:02:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 21 Jan 2021 19:54:10 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:54:13 GMT
RUN docker-php-ext-enable sodium
# Thu, 21 Jan 2021 19:54:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Jan 2021 19:54:14 GMT
CMD ["php" "-a"]
# Thu, 28 Jan 2021 22:42:35 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Thu, 28 Jan 2021 22:42:53 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Thu, 28 Jan 2021 22:42:54 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Thu, 28 Jan 2021 22:42:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 Jan 2021 22:42:54 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 28 Jan 2021 22:42:55 GMT
ENV COMPOSER_VERSION=2.0.9
# Thu, 28 Jan 2021 22:42:57 GMT
RUN set -eux;   curl --silent --fail --location --retry 3 --output /tmp/keys.dev.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub;   curl --silent --fail --location --retry 3 --output /tmp/keys.tags.pub --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub;   curl --silent --fail --location --retry 3 --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       unlink('/tmp/installer.php');       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }";   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 28 Jan 2021 22:42:57 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 28 Jan 2021 22:42:58 GMT
WORKDIR /app
# Thu, 28 Jan 2021 22:42:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Jan 2021 22:42:59 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:3997176601fb5d5ac06922718668ede4acac00a5c0daef8a9099fd76ce93047f`  
		Last Modified: Fri, 15 Jan 2021 01:52:40 GMT  
		Size: 2.6 MB (2601720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497e79d9095f9ba4812f1150c33ad07d399f559fea8e3c4fe8553e02f2cf8b6a`  
		Last Modified: Fri, 15 Jan 2021 23:39:10 GMT  
		Size: 1.8 MB (1756352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99527660904ffc5aed1d27bb86166f189e04b5df76d7becf74efffb1836eaf5e`  
		Last Modified: Fri, 15 Jan 2021 23:39:10 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9b51111e1ef5a5156e505d6369bb2d4e21354a1203636fca6f26de34df9c15`  
		Last Modified: Fri, 15 Jan 2021 23:39:10 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3c721a3fef9acf0bac166c45ff18e2485752ef7b86447284b7b710646d40df`  
		Last Modified: Fri, 15 Jan 2021 23:38:47 GMT  
		Size: 10.7 MB (10661723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e676c2ca01980f72daf35a53dae36e4fe10945de76af81d54618066f5204c598`  
		Last Modified: Fri, 15 Jan 2021 23:38:48 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90c350aff0df72bb91eaa20306afe2218ac1d50242eb213d4e481f65b2a9f60`  
		Last Modified: Fri, 15 Jan 2021 23:38:48 GMT  
		Size: 14.4 MB (14364644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c91dec7c10d367e01e4907cb6c2d00b3e5b7390545c8c9499eaac3c35986507`  
		Last Modified: Thu, 21 Jan 2021 20:05:24 GMT  
		Size: 2.3 KB (2269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63e510378e653ab6ff71c58fc15e869877848171131d614af01c250d7a36e31`  
		Last Modified: Thu, 21 Jan 2021 20:05:20 GMT  
		Size: 17.5 KB (17541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4079b673c2155f6fc765bd4b8d683a2326dd552affe882edccb45c657534ed18`  
		Last Modified: Thu, 28 Jan 2021 22:43:28 GMT  
		Size: 31.4 MB (31389182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdeafc632059b12ff488232684da09d9c34de98941c5f6ff69c471274af7602`  
		Last Modified: Thu, 28 Jan 2021 22:43:22 GMT  
		Size: 197.8 KB (197815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f475e4a4966b8ce4d7561e4c7a2e4961201d5b118193c3525421174abaaa14e5`  
		Last Modified: Thu, 28 Jan 2021 22:43:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0527c47a0591fb1d627eb0553a148074dc26b3e929f17fe11c70beb29ddc697e`  
		Last Modified: Thu, 28 Jan 2021 22:43:21 GMT  
		Size: 552.8 KB (552833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20581df10571ef1589ab514908ef57a5508e11f388e2022afb5678afc09bdcdb`  
		Last Modified: Thu, 28 Jan 2021 22:43:21 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d915abaf68a0c69e745c6fa8e076f421f760e793935af4022615f2460c3f7cb`  
		Last Modified: Thu, 28 Jan 2021 22:43:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
